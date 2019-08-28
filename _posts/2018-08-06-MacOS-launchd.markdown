---
layout: post
title: "맥 OS launchd 사용기"
cover: "MacOS launchd" 
date: 2018-08-06 23:44:00 +0900
description: stock bot을 돌리고 싶다 # Add post description (optional)
img: 2018-08-06.JPG # Add image post (optional)
tags: [Study, MacOS, launchd]
categories: study
author: DUBUHOLIC # Add name author (optional)
---

텔레그램 봇에 특정 주식의 주가 정보를 open, close 시간에만 받아 보고 싶어서 python으로 하나 작성했는데..   
이걸 계속 실행 시키고 싶다.   
혹시나 해서 맥북에어에 crontab되나 찾아봤더니 있단다. 오오오 바로 등록!! 했으나   
맥북을 덮어두고 가면 sleep 모드라 실행이 안되나 보다   
뒤적뒤적.. 개선된 "launchd"가 있고 하위 호환용으로 crontab을 남겨 두었다고 한다.    
launchd를 사용해 보자 ~~crontab 이랑 비슷하겠지~~

디렉토리 이동   
cd ~/Library/LaunchAgents    

파일 생성 아 바로 vi 해도 되지만.. 습관   
touch stock.bot.plist    

파일 편집   
vi stock.bot.plist    

vi 편집법은 간단하게 i 를 누르면 insert      
저장할땐 esc -> :wq ~~(write & quit)~~    
저장안하고 나갈땐 esc -> :q!    

오전 9시 오후 3시 30분 두번 알림을 받고 싶다   
> <key>StartCalendarInterval</key>   
                <array>   
                        <dict>   
                                <key>Hour</key>     
                                <integer>9</integer>    
                                <key>Minute</key>     
                                <integer>0</integer>    
                        </dict>    
                        <dict>     
                                <key>Hour</key>     
                                <integer>15</integer>     
                                <key>Minute</key>    
                                <integer>30</integer>     
                        </dict>      
                </array>     

python 프로그램이라 argument형식으로 실행시켜야 한다 (python 실행파일명.py)    
> <key>ProgramArguments</key>    
        <array>    
                <string>/Users/Jinny/anaconda/bin/python</string>    
                <string>/Users/Jinny/Desktop/tofuholic/telegramBot/tofu_stock_bot.py</string>     
        </array>      

schedule을 걸려면 KeepAlive가 아닌 OnDemand로 하자!   
<key>OnDemand</key>    
<true/>    

이제 작성한 파일을 load 시키자    
launchctl load ~/Library/LaunchAgents/stock.bot.plist   
파일을 수정하고 다시 load시킬땐 unload후에 다시 load하면 된다!    
launchctl unload ~/Library/LaunchAgents/stock.bot.plist    
launchctl load ~/Library/LaunchAgents/stock.bot.plist     

잘 실행되고 있는지가 궁금하다 시스템 로그를 trace 해보자    
tail -f /var/log/system.log     

음 .. 너무 큰 기대였다 맥북을 켜놓고 다니기엔.. 흠.. 서버를 임대하자 ~~AWS~~ 허허허

참고 사이트 http://www.launchd.info/


<div class="page-last-image">
        <img src="/assets/img/2018-08-06.JPG" alt="제주 함덕 호랑이 바&펍 딱새우 파스타" style="width: 100%; height: auto;">   
        <p>제주 함덕 [호랑이 바&펍] 딱새우 파스타</p>
</div>

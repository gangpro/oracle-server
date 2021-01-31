# Net Manager
> Oracle 소프트웨어 설치 : 11gWS1 교재 3장<br>

> 개발환경<br> 
> OS : Macbook Pro, macOS Mojave, version 10.14.3<br>
> VirtualBox : Version 6.0.4<br>
> 가상환경 : Enterprise Linux, Oracle 11g

## Net 매니저 실행
* 터미널 실행
###
    [orcl:Disk1]$  netmgr
   
<img width="570" alt="Screen Shot 2019-04-05 at 3 55 54 PM" src="https://user-images.githubusercontent.com/46523571/55670098-1c64af80-58bb-11e9-8ad2-7ec97dbc433c.png">

* Oracle Net Configuration - Local - Linsteners 왼쪽 + 버튼 클릭
<img width="384" alt="Screen Shot 2019-04-05 at 3 58 12 PM" src="https://user-images.githubusercontent.com/46523571/55670102-2edee900-58bb-11e9-85a5-fdd1749195df.png">

* Choose Listener Name : LISTENER - OK
<img width="385" alt="Screen Shot 2019-04-05 at 3 59 34 PM" src="https://user-images.githubusercontent.com/46523571/55670113-57ff7980-58bb-11e9-9fc4-8bf1766992e2.png">

## Listening Locations 추가
* 상단 Listening Locations 클릭 후 Host 및 Port 체크 - Add Address 버튼 클릭
<img width="385" alt="Screen Shot 2019-04-05 at 4 00 13 PM" src="https://user-images.githubusercontent.com/46523571/55670114-57ff7980-58bb-11e9-801d-4c4e06691b9e.png">

## Database Services 추가
* 상단 Database Services 클릭 후 Global Database name/Oracle Home Directory/SID 체크 - Add Database 버튼 클릭
<img width="384" alt="Screen Shot 2019-04-05 at 4 02 00 PM" src="https://user-images.githubusercontent.com/46523571/55670115-58981000-58bb-11e9-90f4-c6bc0ef5787a.png">

## 저장
* File - Save Network Configuration 후 종료
<img width="381" alt="Screen Shot 2019-04-05 at 4 02 25 PM" src="https://user-images.githubusercontent.com/46523571/55670116-58981000-58bb-11e9-9f91-b588780b645c.png">

## 리스너 상태 확인
* 터미널 실행
###
    [orcl:Disk1]$ vi $ORACLE_HOME/network/admin/listener.ora
<img width="572" alt="Screen Shot 2019-04-05 at 4 05 20 PM" src="https://user-images.githubusercontent.com/46523571/55670156-fe4b7f00-58bb-11e9-9c07-72e6b607e886.png">
* 현재 내 listener는 LISTENER, L2 2개
<img width="573" alt="Screen Shot 2019-04-05 at 4 04 58 PM" src="https://user-images.githubusercontent.com/46523571/55670173-06a3ba00-58bc-11e9-9d76-d8d27328911c.png">

## 리스너 시작
* 터미널 실행
###
    [orcl:Disk1]$ lsnrctl start
<img width="573" alt="Screen Shot 2019-04-05 at 4 12 14 PM" src="https://user-images.githubusercontent.com/46523571/55670157-fe4b7f00-58bb-11e9-9f96-9e8507befb48.png">








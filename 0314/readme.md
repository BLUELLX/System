System programming 02  

<기본 명령어 사용>  
날짜 및 시간 확인   
입력:$ date      출력->2022. 01. 01. (토) 12:26:10 kst

<시스템 정보 확인>  
$ hostname   
linux.sookmyung.ac.kr  
$ uname  
Linux  
$ uname -a  
Linux Ubuntu 5.11.0-31-generic #33-Ubuntu SMP Wed Aug 11   
13:19:04 UTC 2021 x86_64 x86_64 x86_64 GNU/Linu  

<패스워드 변경>  
$ passwd  
passwd: chang용 암호를 변경하는 중  
기존 로그인 암호를 입력하십시오:  
새 암호:  
새 암호를 다시 입력하십시오:  
passwd: 암호(chang용)가 성공적으로 변경되었습니다  

<파일의 종류>  
일반 파일(ordinary file)  
 데이터를 가지고 있으면서 디스크에 저장된다.   
 텍스트 파일, 이진 파일  
 디렉터리(directory) 또는 폴더(folder)   
 파일들을 계층적으로 조직화하는 데 사용되는 일종의 특수 파일  
 디렉터리 내에 파일이나 서브디렉토리들이 존재한다.   
 장치 파일(device special file)  
 물리적인 장치에 대한 내부적인 표현  
 키보드(stdin), 모니터(stdout), 프린터 등도 파일처럼 사용  
 심볼릭 링크 파일  
 어떤 파일을 가리키는 또 하나의 경로명을 저장하는 파일  

<명령어 경로 확인-which>  
$ which ls  
/bin/ls  
$ which pwd  
/bin/pwd  
$ which passwd  
/bin/passwd  

<디렉터리 이동-cd>  
$ cd   
$ cd ~  
$ cd 바탕화면  
$ pwd  
/home/chang/바탕화면  
$ cd .. // 부모 디렉터리로 이동  

<디렉터리 생성-mkdir>  
$ cd ~ // 홈 디렉터리로 이동  
$ mkdir test   
$ mkdir test temp   
$ ls -l  
drwxrwxr-x. 2 chang chang 6 5월 12 10:12 temp  
drwxrwxr-x. 2 chang chang 6 5월 12 10:12 test  

<디렉터리 리스트-ls>  
$ ls /
bin dev home lib64 mnt proc run srv tmp var  
boot etc lib media opt root sbin sys usr  
$ ls ~  
test 공개 다운로드 문서 바탕화면 비디오 사진 음악 템플릿  
$ cd test  
$ ls   
cs1.txt   

<1간단한 파일 만들기-cat>  
$ cat > 파일  
표준입력 내용을 모두 파일에 저장한다. 파일이 없으면 새로 만든다  

<2간단한 파일 만들기-touch>  
$ touch 파일  
파일 크기가 0인 이름만 있는 빈 파일을 만들어 준다  

<파일 앞부분 보기-head>  
$ head [–n] 파일*  
파일(들)의 앞부분을 화면에 출력한다. 파일을 지정하지 않으면 표준입력 내용을 대상으로 한다.  

<파일 뒷부분 보기-tail>  
$ tail [-n] 파일*  
파일(들)의 뒷부분을 화면에 출력한다. 파일을 지정하지 않으면 표준입력 내용  
을 대상으로 한다 .  






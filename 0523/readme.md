# 🐧 리눅스 기본 명령어 정리

---

## 1. 파일 및 디렉터리 관리

| 명령어        | 설명                                  | 예시                      |
|---------------|-------------------------------------|---------------------------|
| `ls`          | 현재 디렉터리 파일 및 폴더 목록 출력  | `ls -l` (상세 목록)        |
| `cd`          | 디렉터리 이동                       | `cd /home/user`            |
| `pwd`         | 현재 작업 디렉터리 경로 출력         | `pwd`                     |
| `mkdir`       | 새 디렉터리 생성                    | `mkdir myfolder`           |
| `rmdir`       | 빈 디렉터리 삭제                    | `rmdir myfolder`           |
| `rm`          | 파일 또는 디렉터리 삭제              | `rm file.txt`              |
| `rm -r`       | 디렉터리 및 하위 파일/폴더 삭제       | `rm -r myfolder`           |
| `cp`          | 파일 복사                         | `cp file1.txt file2.txt`   |
| `mv`          | 파일 또는 디렉터리 이동/이름 변경    | `mv old.txt new.txt`       |

---

## 2. 파일 내용 확인 및 편집

| 명령어        | 설명                                  | 예시                      |
|---------------|-------------------------------------|---------------------------|
| `cat`         | 파일 내용 출력                      | `cat file.txt`             |
| `less`        | 페이지 단위로 파일 내용 보기         | `less file.txt`            |
| `head`        | 파일 앞부분 일부 출력               | `head -n 10 file.txt`      |
| `tail`        | 파일 뒷부분 일부 출력               | `tail -n 10 file.txt`      |
| `nano`        | 간단한 텍스트 편집기               | `nano file.txt`            |
| `vi` / `vim`  | 강력한 텍스트 편집기               | `vi file.txt`              |

---

## 3. 시스템 정보 및 관리

| 명령어        | 설명                                  | 예시                      |
|---------------|-------------------------------------|---------------------------|
| `top`         | 실시간 시스템 프로세스 및 자원 사용 정보 | `top`                    |
| `ps`          | 현재 실행 중인 프로세스 목록 보기     | `ps aux`                  |
| `kill`        | 프로세스 종료                       | `kill PID`                |
| `df`          | 디스크 사용량 확인                   | `df -h`                   |
| `du`          | 파일/디렉터리 용량 확인             | `du -sh myfolder`         |
| `free`        | 메모리 사용량 확인                   | `free -h`                 |
| `uname`       | 시스템 정보 출력                    | `uname -a`                |

---

## 4. 권한 및 소유권 관리

| 명령어        | 설명                                  | 예시                      |
|---------------|-------------------------------------|---------------------------|
| `chmod`       | 파일/디렉터리 권한 변경              | `chmod 755 script.sh`      |
| `chown`       | 파일/디렉터리 소유자 변경            | `chown user:group file.txt`|
| `ls -l`       | 권한 및 소유자 정보 확인             | `ls -l`                   |

---

## 5. 네트워크 관련

| 명령어        | 설명                                  | 예시                      |
|---------------|-------------------------------------|---------------------------|
| `ping`        | 네트워크 연결 상태 확인               | `ping google.com`          |
| `ifconfig`    | 네트워크 인터페이스 설정 및 확인      | `ifconfig`                 |
| `netstat`     | 네트워크 연결 및 포트 상태 확인       | `netstat -tuln`            |
| `ssh`         | 원격 서버 접속                      | `ssh user@server.com`      |
| `scp`         | 원격지 파일 복사                    | `scp file.txt user@server:/path` |

---

## 6. 압축 및 아카이브

| 명령어        | 설명                                  | 예시                      |
|---------------|-------------------------------------|---------------------------|
| `tar`         | 아카이브 생성 및 추출                 | `tar -cvf archive.tar folder/`<br>`tar -xvf archive.tar` |
| `gzip`        | 파일 압축                           | `gzip file.txt`            |
| `gunzip`      | gzip 압축 해제                     | `gunzip file.txt.gz`       |
| `zip`         | ZIP 압축                          | `zip archive.zip file.txt` |
| `unzip`       | ZIP 압축 해제                     | `unzip archive.zip`        |

---

## 7. 기타 유용한 명령어

| 명령어        | 설명                                  | 예시                      |
|---------------|-------------------------------------|---------------------------|
| `echo`        | 문자열 출력                         | `echo "Hello World"`       |
| `date`        | 현재 날짜와 시간 출력                | `date`                    |
| `history`     | 이전에 실행한 명령어 기록 확인       | `history`                 |
| `man`         | 명령어 매뉴얼 페이지 보기            | `man ls`                  |
| `grep`        | 텍스트 검색                         | `grep "text" file.txt`     |
| `find`        | 파일 찾기                         | `find /home -name "*.txt"` |

---

## 참고 자료

- [Linux Command Cheat Sheet](https://linuxcommand.org/lc3_learning_the_shell.php)  
- `man` 명령어로 각 명령어의 자세한 사용법 확인 가능  

---

필요하면 특정 명령어에 대한 자세한 설명이나 실습 예제도 추가해드릴게요!

# 유닉스 시스템 프로그래밍: 챕터 7~9 정리

출처: 숙명여대 창병모 교수 유닉스 강의자료

---

## 📡 7장. 인터넷과 서버

### 7.1 네트워크 구성

- **LAN (Local Area Network)**: 근거리 네트워크
- **이더넷 (Ethernet)**: 가장 일반적인 LAN
- **라우터 (Router)**: 네트워크 간 연결 장치
- **게이트웨이 (Gateway)**: LAN과 인터넷 연결
- **WAP**: 무선 장치 연결용

---

### 7.2 인터넷

- **인터넷**: TCP/IP 기반의 전세계 공개 네트워크
- **프로토콜**: 통신 규약

#### IP / TCP

- IP: 주소 지정, 패킷 조립/분해
- TCP: 신뢰성 있는 데이터 전송 보장

---

### 호스트명/IP 확인

```bash
$ hostname       # 호스트명 확인
$ ip addr        # IP 주소 확인

##파일전송
$ ftp 호스트명
$ sftp 호스트명
sftp> get 파일명
sftp> put 파일명

###8장
##8.1 find 명령어
$ find 디렉터리 -name 파일명
$ find . -type d -perm 700
$ find . -name "*.c" -exec ls -l {} \;

##8.2grep명령어
$ grep 패턴 파일
$ grep -n 패턴 파일
$ grep -i -w -v -c 패턴 파일
$ ps -ef | grep ssh


##8.5 파일 분할/합병  
$ split -l 10 file.txt         # 분할
$ cat xaa xab > xmerge.txt     # 병합
$ paste -s xaa xab > xmerge    # 줄 병합

###9장
##at 명령어
$ at 11:45 jan 31
at> sort infile > outfile

##9.3 파일 압축
$ gzip 파일
$ gzip -d 파일.gz


##9.5 AWK 프로그램 예시
BEGIN { print "시작" }
{ print $1, $NF }
END { print "끝" }

# 줄 수와 단어 수
{
  word += NF
}
END {
  print "줄:", NR, "단어:", word
}




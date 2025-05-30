# 시스템 프로그래밍 정리 (Linux System Programming)

출처: 경성대학교 시스템 프로그래밍 수업 자료

---

## 1. 유닉스 커널 구조

- 파일 관리 (File Management)
- 프로세스 관리 (Process Management)
- 메모리 관리 (Memory Management)
- 통신 관리 (Communication Management)
- 주변 장치 관리 (Device Management)

---

## 2. 시스템 호출 (System Call)

- 커널에 서비스를 요청하는 프로그래밍 인터페이스
- 응용 프로그램 → 시스템 호출 → 커널 서비스

### 주요 시스템 호출

| 자원         | 호출 함수 예시                                  |
|--------------|--------------------------------------------------|
| 파일         | `open()`, `close()`, `read()`, `write()`, `dup()`, `lseek()` |
| 프로세스     | `fork()`, `exec()`, `exit()`, `wait()`, `getpid()` |
| 메모리       | `malloc()`, `calloc()`, `free()` *(라이브러리 함수)* |
| 시그널       | `signal()`, `alarm()`, `kill()`, `sleep()`       |
| 프로세스 간 통신 | `pipe()`, `socket()`                            |

---

## 3. 파일 시스템 호출

### `open()`

```c
#include <fcntl.h>

int open(const char *path, int oflag, [mode_t mode]);

##create()
int creat(const char *path, mode_t mode);

##close()
int creat(const char *path, mode_t mode);

##read()
#include <unistd.h>
ssize_t read(int fd, void *buf, size_t nbytes);

##write()
#include <unistd.h>

ssize_t write(int fd, const void *buf, size_t nbytes);

##dup()/dup2()
#include <unistd.h>

int dup(int oldfd);
int dup2(int oldfd, int newfd);

##lseek()
#include <unistd.h>

off_t lseek(int fd, off_t offset, int whence);

##파일 열기 예제
#include <fcntl.h>
#include <stdio.h>

int main(int argc, char *argv[]) {
    int fd = open(argv[1], O_RDWR);
    if (fd == -1)
        printf("파일 열기 오류\n");
    else
        printf("파일 %s 열기 성공 : %d\n", argv[1], fd);
    close(fd);
    return 0;
}

##파일 크기 계산 예제 (fsize.c)
#define BUFSIZE 512
char buffer[BUFSIZE];
int total = 0;
while ((nread = read(fd, buffer, BUFSIZE)) > 0)
    total += nread;


##파일 복사 예제 (copy.c)
while ((n = read(fd1, buf, BUFSIZ)) > 0)
    write(fd2, buf, n);



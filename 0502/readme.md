#!/bin/bash    # <- 반드시 첫 줄에 작성 (쉘 종류 명시)

echo "Hello, Bash!"

  ##변수 사용  
  name="홍길동"
echo "안녕하세요, $name 님"

  ##조건문if  
  if [ $age -ge 20 ]; then
  echo "성인입니다"
else
  echo "미성년자입니다"
fi


##반복문-for  
for i in 1 2 3 4 5
do
  echo "숫자: $i"
done

##반복분-while  
count=1
while [ $count -le 5 ]
do
  echo "count: $count"
  count=$((count+1))
done

  ##스크립트에서 파일 확인  
  filename="test.txt"

if [ -f "$filename" ]; then
  echo "$filename 파일이 존재합니다."
else
  echo "$filename 파일이 없습니다."
fi

  ###1. 💾 프로그램 작성과 컴파일  
  ##c프로그램 예시  
  #include <stdio.h>

int main() {
    printf("Hello, World!\n");
    return 0;
}

  ##컴파일 과정  
gcc hello.c -o hello
./hello

  ###2. ⚙️ 자동 빌드 도구 (Makefile)  
  CC=gcc
CFLAGS=-Wall

all: main

main: main.o
	$(CC) $(CFLAGS) -o main main.o

main.o: main.c
	$(CC) $(CFLAGS) -c main.c

clean:
	rm -f *.o main

  

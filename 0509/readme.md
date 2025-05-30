###1. 🧱 파일 시스템이란?  
데이터를 저장하고 조직하는 구조

리눅스는 계층적 디렉터리 구조 사용

모든 것(디바이스 포함)이 "파일"로 취급됨  

###2. 📄 파일 상태 정보와 i-node  
📌 i-node(Inode)
파일의 메타데이터를 저장하는 구조체

파일 내용은 포함하지 않음  

##확인 명령어  
ls -li filename
stat filename

###3. 📁 디렉터리  
디렉터리는 특수한 파일로, 내부에 다른 파일이나 디렉터리의 이름과 i-node 번호를 매핑함

루트 디렉터리는 /

상대 경로(../, ./)와 절대 경로(/home/user/file) 구분  

###4. 🔗 링크의 구현    
##하드 링크 (Hard Link)
동일한 i-node를 가리킴 (동일한 파일에 별칭 부여)

파일이 삭제되어도 하드 링크가 존재하면 데이터는 유지됨
##심볼릭 링크 (Soft Link / Symlink)
다른 파일의 경로를 저장하는 특수한 파일

원본 파일이 삭제되면 깨짐

###5. 📥 파일 입출력 (File I/O)  
#include <fcntl.h>
#include <unistd.h>

int main() {
    int fd = open("file.txt", O_RDONLY);
    char buf[100];
    read(fd, buf, 100);
    close(fd);
    return 0;
}

  

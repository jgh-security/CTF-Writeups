# file-download-1

## 문제 정보
- 플랫폼: Dreamhack
- 분야: 웹해킹
- 난이도: Beginner

## 문제 설명
File Download 취약점이 존재하는 웹 서비스
flag.py를 다운로드 받으면 플래그 획득

## 풀이 과정
1. 서버 접속 - 메모 업로드 서비스 확인
![메인 화면](images/file-download_1.png)

2. app.py 코드 분석
   - 업로드(/upload)할 때만 `..` 검사
   - 읽기(/read)할 때는 검증 없음
![취약점 코드](images/file-download_2.png)

3. read 엔드포인트에 경로 조작으로 flag.py 요청
   - URL: `/read?name=../flag.py`
![flag 획득](images/file-download_3.png)

## 취약점
read 함수에서 filename 입력값 검증 없음
→ 경로 조작(Path Traversal)으로 상위 폴더 파일 접근 가능

## 배운 점
- 파일 읽기/쓰기 모든 곳에서 경로 검증 필요
- `..` 는 상위 디렉토리를 의미함
- 업로드만 막고 읽기를 안 막으면 취약점 발생

## Flag
DH{...}

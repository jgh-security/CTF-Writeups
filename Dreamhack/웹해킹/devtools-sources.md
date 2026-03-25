# devtools-sources

## 문제 정보
- 플랫폼: Dreamhack
- 분야: 웹해킹
- 난이도: Beginner

## 문제 설명
개발자 도구의 Sources 탭 기능을 활용해 플래그를 찾는 문제다.

## 풀이 과정
1. 문제 파일을 다운로드 후 index.html을 브라우저로 연다.

2. F12 → Sources 탭을 클릭한다.

3. Ctrl+Shift+F로 전체 검색한다.
   - 검색어: DH{

4. main.3da94fde.css 파일 4146번 줄에서 flag를 발견한다.
   - WEBPACK FOOTER 주석 안에 숨겨져 있다.

## 취약점
소스코드(CSS/JS) 파일 안에 민감한 정보가 노출되어 있다.
개발자 도구로 누구나 확인할 수 있다.

## 배운 점
- 클라이언트 사이드 파일에는 절대 민감한 정보를 포함하면 안 된다.
- 개발자 도구 Sources 탭으로 모든 소스코드를 확인할 수 있다.

## Flag
DH{...}

# cookie

## 문제 정보
- 플랫폼: Dreamhack
- 분야: 웹해킹
- 난이도: Level 1

## 문제 설명
쿠키를 이용한 인증 우회 문제

## 풀이 과정
1. app.py 코드 분석
   - 로그인 시 username을 쿠키에 저장
   - 쿠키의 username이 admin이면 flag 반환
   
2. guest / guest로 로그인

3. 개발자 도구(F12) → Application → Cookies
   - username 값을 guest → admin으로 변경

4. 새로고침 → flag 획득

## 취약점
쿠키 값을 서버에서 검증하지 않아
클라이언트에서 임의로 변조 가능

## 배운 점
- 쿠키는 클라이언트에서 변조 가능
- 인증은 반드시 서버에서 검증해야 함

## Flag
DH{...}
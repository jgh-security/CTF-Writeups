# cookie

## 문제 정보
- 플랫폼: Dreamhack
- 분야: 웹해킹
- 난이도: Beginner

## 문제 설명
쿠키를 이용한 인증 상태를 관리하는 간단한 로그인 서비스다.
admin 계정으로 로그인에 성공하면 플래그를 획득할 수 있다.

## 풀이 과정
1. app.py 코드 분석
   - 로그인 시 username을 쿠키에 저장한다.
   - 쿠키의 username이 admin이면 flag를 반환한다.

2. guest / guest로 로그인한다.

3. 개발자 도구(F12) → Application → Cookies
   - username 값을 guest → admin으로 변경한다.

4. 새로고침 후 flag를 획득한다.

## 취약점
쿠키 값을 서버에서 검증하지 않아
클라이언트에서 임의로 변조할 수 있다.

## 배운 점
- 쿠키는 클라이언트에서 변조 가능하다.
- 인증은 반드시 서버에서 검증해야 한다.

## Flag
DH{...}

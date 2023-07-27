# Shell Programming
## 환경 변수
+ Shell 환경 변수란?
  + 동작 되는 프로그램에게 영향을 주는 변수
+ 환경 변수 선언: export varName=value(대문자 관례)
  + $ export NAME=lee
  + $ echo $NAME
+ 시스템에 적용된 환경 변수 확인: $ env
+ 기억해야할 환경변수
  + PATH: 명령어 탐색 경로
  + HOME: 홈디렉토리의 경로. cd 명령 실행시 적용
  + USER: 로그인 사용자 이름
  + SHELL: 로그인 shell의 이름

## Quoting Rule
+ Metacharacters
  + Shell에서 특별히 의미를 정해 놓은 문자들
  + | ? () $ ... % {} [] 등
+ Quoting Rule: 메타문자의 의미를 제거하고 단순 문자로 변경
    + Backslash(\): 바로 뒤의 메타 문자는 특별한 의미를 제거
    + Double Quotes(""): "" 내의 모든 메타문자의 의미를 제거. (단 $, ` 제외)
    + Single Quotes(''): '' 내의 모든 메타만자의 의미를 제거
+ Nesting Command: 명령어의 실행 결과를 치환하여 명령을 실행
    + $(command) or `command`
    + $ echo "Today is $(date)" or $ echo "Today is `date`"

## Alias
+ alias
  + Shell의 명령에 새로운 이름을 부여
  + 명령들을 조합하여 새로운 이름의 명령을 생성
  + alias 등록: alias name='command'
  + alias 확인: alias or alias name
  + alias 삭제: unalias name

## Redirection
+ Redirection

| Communication channels | Redirection characters |                   의 미                   |
|------------------------|------------------------|-------------------------------------------|
|         STDIN          |     "0<"     "0<<"     | 입력을 키보드가 아닌 파일을 통해 받음      |
|         STOUT          |     "1>"     "1>>"     |  표준 출력을 터미널이 아닌 파일로 출력     |
|         STDERR         |     "2>"     "2>>"     | 표준 에러 출력을 터미널이 아닌 파일로 출력 | 

">>" 사용시 기존 내용에 추가  
0, 1은 생략 가능  
ERROR!! 2> /dev/null  

## Pipeline
+ Pipeline
    + 명령의 실행결과를 다음 명령의 입력으로 전달
    + 리눅스의 명령어를 조합하여 사용
    + 기호: command1 | command2 | command3

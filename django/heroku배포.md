# Heroku 배포

1. Heroku 회원가입

2. Heroku CLI 설치

3. 환경변수 적용
    - DEBUG = (os.environ.get('DEBUG', 'True') != 'False')
  
4. .gitignore 파일 적용

   - gitignore .io 에서 Django 선택 후 '생성' 클릭
   - 페이지에 나온 텍스트를 모두 복사후 .gitignore 파일로 저장
  
5. Heroku 용 파일 작성

   - Procfile 이라는 파일을 만들어 아래 내용 작성
 
        web: gunicorn 프로젝트명.wsgi --log-file -

    - runtime.txt 파일에 아래 내용 작성

        python-3.9.1

6. 필요한 Dependency 설치

7. setting-py 수정

    - Whitenois 설치

   - MIDDLEWARE 에서 제일 SecurityMikddleware 바로 아래 내용 추가

       whitenois.middleware.WhiteNoiseMiddleware'.

   - ALLOWED_HOSTS 수정


    - ALLOWED_HOSTS=[] 를 ALLOW_HOSTS=['*']로 수정
  
   - DB 관련 코드 수정

    - settings .py 제일 밑에 아래 내용 추가

------

1. requriements.txt생성
   
   - git에 수정된 파일들 추가
   - Heroku 관련 명령어 실행
   - Heroku에서 환경 변수 설정
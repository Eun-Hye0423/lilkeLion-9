# Docker이란?

## docker 이미지

    - 장고 앱 파일, 설정 등을 저장
    - os에 따라 차이에 무관하게 동일한 환경에서 실행 가능

## 이미지 생성

    1. Gitpod.io 계정

    2. Gitpod 설정 수정
        - Gitpod > Settings
            - Feature Preview > Enable Feature Preview 체크
            - Default IDE 선택

    3. Gitpod 인스턴스 생성

        - 레포지토리 주소 앞에 gitpod.io/#을 붙임
    
    4. DockerHub 계정 생성

2. requirements 설치

    - pip install -r requirements.txt

3. Whitenoise 설치
4. Gunicorn 설치
5. Dockerfile 생성

# docker로 배포하기

1. 준비사항

    - EC2 인스턴스 (AWS EC2 전반부 참고)
    - Docker Hub에 등록된 이미지

2. 서버 세팅
   - Docker 설치
    - Docker Compose 설치
    - 앱 설치 폴더 지정
    - docker-compose.yml 생성

1. .env 파일 생성
   - DB 최초로 실행
   - 잘 작동 되는지 테스트
   - 백그라운드 모드로 전환

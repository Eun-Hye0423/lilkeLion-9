# Ubuntu 배포

1. EC2 인스턴스 만들기

     - https://console.aws.amazon.com/

    - 우측 상단 지역이 Seoul 인지 확인

    - EC2 검색

    - Instances > Launch Instances

    - Ubuntu Server 20.04 LTS (64-bit x86)

    - t2.micro 

    - Storage 설정 

    - Security Group > Add Rule

        - HTTP
        - HTTPS
        - Custom -> TCP -> 8000 ->0.0.0.0/0, ::/0

    - Review and Launch > Launch

    - Elastic IP 받기

        - Network & Security > Elastic IPs
        - Allocate Elastic IP address
        - Allocate
        - Associate Elastic IP address
        - Instance > 아까 생성된 인스턴스 선택
        - Associate

    - SSH 연결하기

    - 필요한 패키지 설치
    - 패키지 설치파는 동안 settings. py 수정
    - 매번 하던것들
  
        - python3 -m venv venv
        - git clone 내_GitHub_레포지토리 django-app
        - cd django-app
        - source ../venv/bin/activate
        - pip install -r requirements.txt
        - python manage .py runserver 0.0.0.0:8000
        - http://내_Elastic_IP:8000 로 접속해서 Django 화면이 표시되는지 확인

    - PostgreSQL 설치
    - settings .py 에 DB 설정
    - 
  
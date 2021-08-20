# Temlpate 상속

-> 코드의 중복을 한번의 코드 작성으로 해결할 수 있게해주는 기능

1. base.html에 상속할 코드를 작성한다.
2. base.html의 body안에 
        
        <div class="container"> 
        {% block content %}
        {% endblock %}
        </div>

3. 상속받을 파일에 코드 기입

        {% extends 'base/html' %}
        {% block content %}
        {% endblock %}
 
 4. settings. py의 DIRS에 추가
   
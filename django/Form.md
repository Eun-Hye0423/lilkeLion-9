# Form
1. templates파일에 form. py 파일 생성

2. forms 사용 코드 작성

         from django import forms
        from .models import Blog

        class BlogForm(forms.ModelForm):
          class Meta:
          model = Blog
          fields = ['models.py 내에 put_date를 제외한 모든 클래스 변수' ]

3. views .py
   
        from .forms import BlogForm

# USER 확장과 인증

user테이블

-> 사용자에 대한 정보를

 auth

-> 사용자가 회원가입 요청하고, 로그인 요청

로그인/회원가입/로그아웃

#paginator

->블로그 객체를 잘라서 보내주는 기능

        from django.core.paginator import Paginator

        paginator = Paginator(blogs, 3) 
        page = request.GET.get('page')  
        blogs = paginator.get_page(page)


objects.order_by('-pub_date') 

->  최신글부터 보여줌

.objects.filer(writer=author) 

-> 조건에 만족하는 값을 반환

.objects.exlude(writer=author) 

-> 조건에 만족하지 않는 값을 반환

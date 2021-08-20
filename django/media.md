# media
1. setting. py에 
 
        MEDIA_ROOT = os.path.join(BASE_DIR, 'media')
        MEDIA_URL = '/media/'

2. urls.py에
   
       from django.conf import settings
        from django.conf.urls.static import static

3. models.py설정
   
-> 업로드할 사진에 대한 코드를 작성.

4. pip install pillow
5. 업로드 구현
6. views. py 
7. detaol.html
   
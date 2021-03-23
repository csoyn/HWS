# Django_hw6

> Static & Media



### 1. static 파일 기본 설정
개발자가 작성한 CSS 파일이나 미리 업로드한 이미지 파일 등이 Django 프로젝트 폴더(my_ pjt) 내부 assets 폴더에 있다 . 이처럼 기존 static 파일 경로 외에 추가 경로를 정의해야할 경우 settings.py 에 추가해야 하는 설정과 값을 작성하시오

**답) **

```python
STATICFILES_DIRS = [
    BASE_DIR / 'my_pjt' / 'assets',
]
```



### 2. media 파일 기본 설정

사용자가 업로드 파일의 저장치를 Django 프로젝트 폴더 (my_pjt) 내부 uploaded_files 폴더 로 지정하고자 한다 . 이 때 , settings.py 에 작성해야 하는 설정과 값을 모두 작성하시오.

**답)**

```python
# my_pjt /urls.py
urlpatterns = [
    path('admin/', admin.site.urls),
    path('articles/', include('articles.urls')),
] + static(settings.MEDIA_URL, document_root=settings.MEDIA_ROOT)
```

```python
# my_p
#~/media/실제파일이름
MEDIA_URL = '/media/'

# 프로젝트에서 미디어 파일이 저장되는 공간
MEDIA_ROOT = BASE_DIR / 'media'
```



### 3. Serving files uploaded by user during development
settings.py에 MEDIA_URL 값이 작성되어 프로젝트에 사용자가 업로드한 파일이 업로드 될 수 있게 되었다. 하지만 사용자가 실제 웹 페이지 내에서 이 파일을 조회 할 수 있도록 하기 위해선 업로드 된 파일에 대한 URL을 생성 해주는 설정이 필요하다. 빈칸 __(a)__, __(b)__, __(c)__, __(d)__에 들어 갈 코드를 작성하시오.

![image-20210318112420808](django_hw6.assets/image-20210318112420808.png)

**답)**

(a) - settings /  (b) - django.conf.urls.static  / (c) - static / (d) - settings.MEDIA_URL, document_root=settings.MEDIA_ROOT
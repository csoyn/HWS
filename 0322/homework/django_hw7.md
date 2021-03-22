# Django_hw7

> Static File



### 1. Compiled Bootstrap

CSS, JS 파일을 다운로드 받아 Django 프로젝트에 Static 파일로 추가하시오. 부트스트랩이 적용되기 위해 작성해야 할 코드를 제출하시오

프로젝트 폴더 - static 폴더 생성 / app폴더 - static / 앱 이름 폴더 생성 / 그 밑에 이미지 등 폴더

```python
# 프로젝트 / settings.py

STATIC_URL = '/static/'

STATICFILES_DIRS = [
    # base.html에서 static을 사용하기!
    BASE_DIR / '프로젝트이름' / 'static',
]
```

```html
{# base.html #}

{% load static %}

  <link rel="stylesheet" href="{% static 'stylesheets/style.css' %}">
  {% block css %}
  {% endblock css %}
...

{# 앱templates의 .html #}
{% extends 'base.html' %}
{% load static %}

{% block css %}
<link rel="stylesheet" href="{% static 'articles/stylesheets/style.css' %}">
{% endblock css %}

{% block content %}
...


```


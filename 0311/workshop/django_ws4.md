# Django ws04

> Django CRUD

### 1) READ

<img src="django_ws4.assets/image-20210315213253060.png" alt="image-20210315213253060" style="zoom:67%;" />

```python
# urls patterns
path('', views.index, name='index')
# views
def index(request):
    articles = Article.objects.all()
    context = {
        'articles': articles,
    }
    return render(request, 'articles/index.html', context)
```

```html
% extends 'base.html' %}
{% block content %}
<a class="nav-link" href="{% url 'articles:create' %}">NEW</a>
  <table class="table">
    <thead>
      <tr>
        <th scope="col">제목</th>
        <th scope="col">내용</th>
      </tr>
    </thead>
    <tbody>
      {% for article in articles %}
        <tr>
          <td><a href="{% url 'articles:detail' article.pk %}">{{ article.title }}</a></td>
          <td>{{ article.content}}</td>
        </tr>
      {% endfor %}
    </tbody>
  </table>
{% endblock content %}
```

### 2) Create

<img src="django_ws4.assets/image-20210315213412564.png" alt="image-20210315213412564" style="zoom:67%;" />

```python
# urls
path('create/', views.create, name='create'),
# views
def create(request):
    return render(request, 'articles/create.html')
```

```html
{% extends 'base.html' %}

{% block content %}
<h1>New</h1>
<form method="POST">
  {% csrf_token %}
  <div class="mb-3">
    <label for="title" class="form-label">TITLE: </label>
    <input type="text" name="title" class="form-control" id="title" aria-describedby="emailHelp" maxlength="10">
  </div>
  <div class="mb-3">
    <label for="content" class="form-label">CONTENT:</label>
    <textarea name="content" id="content" class="form-control" cols="30" rows="10"></textarea>
  </div>
  <button>작성</button>
  <div>
  <a href="{% url 'articles:index' %}">BACK</a>

  </div>
</form>
{% endblock content %}
```



### 3) Detail

![image-20210316010626416](django_ws4.assets/image-20210316010626416.png)

```python
#urls
path('<int:pk>/', views.detail, name='detail'),\
#views
def detail(request, pk):
    article = Article.objects.get(pk=pk)
    context = {
        'article': article
    }
    return render(request, 'articles/detail.html', context)

```

```html
{% extends 'base.html' %}
{% block content %}
<h1>DETAIL</h1>
<hr>
<h3>{{ article.title }}</h3>
<p>{{ article.content }}</p>
<p>작성일 : {{ article.created_at }}</p>
<p>수정일 : {{ article.updated_at }}</p>
<button> 삭제 </button>
<p><a href="{% url 'articles:update' article.pk %}">EDIT</a></p>
{% comment %} <a href="{% url 'articles:delete' %}">DELETE</a> {% endcomment %}
<a href="{% url 'articles:index' %}">BACK</a>
{% endblock content %}
```

### 4) Update

![image-20210316010839489](django_ws4.assets/image-20210316010839489.png)

```python
#urls
path('<int:pk>/update/', views.update, name='update'),
#views
def update(request, pk):
    article = Article.objects.get(pk=pk)
    article.title = request.GET.get('title')
    article.overview = article.GET.get('content')
    article.save()
    return redirect('article:detail', pk)
```

```html
{% extends 'base.html' %}
{% block content %}
<h1>EDIT</h1>
<form method="POST">
  <div class="mb-3">
    <label for="title" class="form-label">TITLE: </label>
    <input type="text" name="title" class="form-control" id="title" aria-describedby="emailHelp" maxlength="10" value = {{article.title}}>
  </div>
  <div class="mb-3">
    <label for="content" class="form-label">CONTENT:</label>
    <textarea name="content" id="content" class="form-control" cols="30" rows="10">{{article.content}}</textarea>
  </div>
  <button>수정</button>
  <div>
  <a href="{% url 'articles:index' %}">BACK</a>
  </div>
</form>
{% endblock content %}
```


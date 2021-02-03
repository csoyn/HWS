# Homework03

> Bootstrap

https://getbootstrap.com/ 공식문서
1) 각  이미지는 현재 lab.ssafy.com에서 사용중인 components이다.  제시된 요소에 사용된 Bootstrap Component가 무엇인지 작성하시오.
2) 위에서 답한 Bootstrap Component를 사용하여 제시된 요소와 유사한 형태가 되도록 코드를 작성하시오.

### 1.

![image-20210203165906056](web_03_homework.assets/image-20210203165906056.png)

**Answer**

1) buttons

Use Bootstrap’s custom button styles for actions in forms, dialogs, and more with support for multiple sizes, states, and more. https://getbootstrap.com/docs/5.0/components/buttons/

2)  html 코드 & 결과

```html
<!DOCTYPE html>
<html lang="en"><head><meta charset="UTF-8"> <meta name="viewport" content="width=
  , initial-scale=1.0">
  <title>Document  </title>
  <link href=cdn불러오기>
</head><style>
  .box{
    width: 500px;    height: 50px;    border-radius: 5px;    text-align: center;  }
</style><body>
  <div class="box p-3 mb-2 bg-success text-white m-4">Sign in</div>
</body></html>
```

![image-20210203172733753](web_03_homework.assets/image-20210203172733753.png)



### 2.

![image-20210203165923914](web_03_homework.assets/image-20210203165923914.png)

**Answer**

1) Navbarp

Documentation and examples for Bootstrap’s powerful, responsive navigation header, the navbar. Includes support for branding, navigation, and more, including support for our collapse plugin.

https://getbootstrap.com/docs/5.0/components/navbar/

2) html 코드와 결과 사진

```html
<body>
  <nav class="navbar navbar-light bg-dark">
    <div class="container-fluid">
      <a class="navbar-brand text-light"> <img src="ssafy.PNG">프로젝트</a>
      <a class="navbar-brand text-light"> 그룹들</a>
      <a class="navbar-brand text-light"> 활동</a>
      <a class="navbar-brand text-light"> 마일스톤</a>
      <a class="navbar-brand text-light"> 스니펫</a>
    </div>
  </nav></body>
```

![image-20210203190558127](web_03_homework.assets/image-20210203190558127.png)

### 3.

![image-20210203165938256](web_03_homework.assets/image-20210203165938256.png)

1) Button group

Group a series of buttons together on a single line or stack them in a vertical column.

 Pagination

Documentation and examples for showing pagination to indicate a series of related content exists across multiple pages.

2)

```html
 <div class="btn-group" role="group" aria-label="Basic radio toggle button group">
    <input type="radio" class="btn-check" name="btnradio" id="btnradio1" autocomplete="off" >
    <label class="btn btn-outline-dark" for="btnradio1">Prev</label>
    <input type="radio" class="btn-check" name="btnradio" id="btnradio1" autocomplete="off" checked>
    <label class="btn btn-outline-dark" for="btnradio1">1</label>
    <input type="radio" class="btn-check" name="btnradio" id="btnradio1" autocomplete="off" >
    <label class="btn btn-outline-dark" for="btnradio1">2</label>
    <input type="radio" class="btn-check" name="btnradio" id="btnradio2" autocomplete="off">
    <label class="btn btn-outline-dark" for="btnradio2">3</label>
    <input type="radio" class="btn-check" name="btnradio" id="btnradio3" autocomplete="off">
    <label class="btn btn-outline-dark" for="btnradio3">4</label>
    <input type="radio" class="btn-check" name="btnradio" id="btnradio3" autocomplete="off">
    <label class="btn btn-outline-dark" for="btnradio3">Next</label>  </div>
```

![image-20210203191051359](web_03_homework.assets/image-20210203191051359.png)

```html
  <nav aria-label="...">    <ul class="pagination">      <li class="page-item disabled">
        <a class="page-link " href="#" tabindex="-1" aria-disabled="true">Prev</a>
      </li>
      <li class="page-item"><a class="page-link" href="#">1</a></li>
      <li class="page-item active" aria-current="page">
        <a class="page-link" href="#">2</a>
      </li>
      <li class="page-item"><a class="page-link" href="#">3</a></li>
      <li class="page-item"><a class="page-link" href="#">4</a></li>
      <li class="page-item">
        <a class="page-link" href="#">Next</a>
      </li>    </ul>  </nav>
```

![image-20210203191550442](web_03_homework.assets/image-20210203191550442.png)



### 4.



### 4. ![image-20210203165953261](web_03_homework.assets/image-20210203165953261.png)
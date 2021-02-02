# Workshop 02.

> Understand for layout , CSS property



## Problem . Semantic Tag

제시된 semantic.html 과 semantic.css 를 수정하여 다음 이미지와 같은 형태가 되도록 코드를 작성하시오

CSS

```css
/* 1. article 태그는 white로 나머지 시멘틱 태그는 lightgrey로 배경색을 바꿔주세요. */
/* 2. 모든 시멘틱 태그의 margin과 padding을 4px로 만들어주세요. */
.header{
  background-color: lightgray;
  height: 40px;
  text-align: center;
  margin: 4px ;
  padding: 4px ;
  border-radius: 4px; }
.nav{
  background-color: lightgray;
  height: 35px;
  margin: 4px ;
  padding: 4px ;
  text-align: left;
  margin: 4px ;
  padding: 4px ;
  border-radius: 4px; }  

/* 3. h1 태그를 중앙 정렬 시켜주세요. */
h1 {
  text-align: center;}
h2 {
  font-size: 20px;
  border-radius: 4px; }

/* 4. section과 aside 태그의 display를 inline-block으로 바꿔주세요. */
/* 5. section 태그는 width 482px height 300px, aside 태그는 width 280px height 300px로 만들어주세요.*/
/* 6. aside 태그에 vertical-align속성의 값을 top으로 적용해주세요.*/
/* 7. 모든 semantic 태그의 border 모서리 반경을 4px로 만들어주세요. */
.section {
  background-color: lightgray;
  width: 482px;
  height: 300px;
  margin: 4px ;
  padding: 4px ;
  border-radius: 4px;
  display: inline-block;
}
 .article {
  background-color: white;
  width: 450px;
  height: 100px;
  margin: 4px ;
  padding: 4px ;
  border-radius: 4px;
} 

.aside{
  width: 280px;
  height: 300px;
  vertical-align: top;
  background-color: lightgray;
  margin: 4px ;
  padding: 4px ;
  border-radius: 4px;
  display: inline-block;
  
}
.footer {
  background-color: lightgray;
  height: 35px;
  margin: 4px ;
  padding: 4px ;
  text-align: left;
  margin: 4px ;
  padding: 4px ;
  border-radius: 4px;}
```

HTML

```html
<body>
  <header>
    <h1 class = "header">header</h1> </div>
  </header>
  <nav>
    <h2 class = "nav">nav</h2>
  </nav>
  <section class = "section">
    <h2>section</h2>
    <article  class="article">
      <h3>article1</h3>
      <h3>article2</h3>
    </article>
  </section>
  <aside class = "aside">
    <h2>aside</h2>
  </aside>
  <footer class="footer">
    <h2>footer</h2>
  </footer>
</body>
```

결과 

![image-20210202175438884](web_02_workshop.assets/image-20210202175438884.png)
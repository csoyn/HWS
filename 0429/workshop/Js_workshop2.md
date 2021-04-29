# JavaScript Workshop2

> DOM 조작에 대한 이해

![image-20210429222517768](Js_workshop2.assets/image-20210429222517768.png)

```html
<body>
  <form action="/todos/">
    <input type="text">
    <button>Todo</button>
  </form>
  <ul></ul>

<script>
  const form = document.querySelector('form')

  function addTodo (event) {
    // 이벤트를 취소한다.
    event.preventDefault()

    // input element와 input element의 value 값을 저장한다.  
    const input = document.querySelector('input')
    const content = input.value

    // li element를 생성 후 input element의 value 값을 데이터로 저장한다
    const li = document.createElement('li')
    li.innerText = content

    // ul 태그의 자식 태그로 위에서 생성한 li element를 넣는다.
    const ul = document.querySelector('ul')
    ul.appendChild(li)

    // // 삭제 버튼을 생성 후 li 태그의 자식 태그로 넣는다.
    const newButton = document.createElement('button')
    const newButtonText = document.createTextNode('삭제')
    newButton.appendChild(newButtonText)
    li.appendChild(newButton)

    // 삭제 버튼을 클릭하면 해당 li element를 삭제한다
    newButton.addEventListener('submit', function (event) {
      const thing = event.target.parentNode
      thing.remove()
    })

    // li element를 클릭하면 취소선이 토글된다.
    li.addEventListener('click', function (event) {
     li.style.setProperty('text-decoration', 'line-through')
  })
  }
  form.addEventListener('submit', addTodo)
</script>
</body>
</html>
```

![image-20210429222612262](Js_workshop2.assets/image-20210429222612262.png)


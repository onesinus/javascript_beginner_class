## Localstorage
```javascript
localStorage.setItem("slebew", "Aku adalah programmer")
localStorage.setItem("student_id", "0901930910392")
localStorage.setItem("teacher_id", 0901930910392)

localStorage.getItem("slebew")
// 'Aku adalah programmer'

localStorage.getItem("wkkwkwwk")
// null

localStorage.getItem("student_id")
// '0901930910392'

localStorage.getItem("teacher_id")
// null

localStorage.setItem("data-object", JSON.stringify({id: 12}))

localStorage.getItem("data-object")
// '{"id":12}'

// JSON.parse(localStorage.getItem("data-object"))
// {id: 12}
```
# TodoList

-코드 리뷰

1번
```javascript
let todos = [];
```
//배열,객체는 let 변수보다는 const를 사용하는 것을 권장

2번
모듈화 권장

3번
if-else문 보다는 삼항 연산자를 사용하는 게 더 좋음 (굳이 return할 필요가 없음)
예) 
```javascript
todos = todos.map(originalTodo => {
            if (originalTodo.id === todo.id) 
            originalTodo.isCompleted = !originalTodo.isCompleted;
            return originalTodo;
        }) ```
   
       
   ```todos = todos.map(originalTodo => originalTodo.id === todo.id ?originalTodo.isCompleted = !originalTodo.isCompleted : originalTodo
   ```
   사용
    
4번
```
const doTrimValue = (val) =>{ 
    const trimVal = String(val).trim(); // string으로 형 변환 후, 공백 제거
    if( trimVal !== ''){ // 빈 문자열이 아니면
        pushTodos(trimVal); // pushTodos()로 todos 배열에 추가하기
    }
    else{ // 빈 문자열이면
        alert("내용을 입력 후 클릭하세요"); // alert 창
    }
    todoInputElement.value = ""; // input의 value 없애기
};
```
여기서 trimVal !== '' 보다는 length로 비교하는 게 더 좋은 것 같음 value가 0이 아니라면!으로

5번
업데이트 기능 구현해보기

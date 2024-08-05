### Late Variables

> `late`는 `var`나 `final` 앞에 붙여줄 수 있는 수식어   
> 초기 데이터없이 변수를 선언할 수 있도록 해준다.

```javascript
void main() {
    late final String name;
    // 여기서 API 처리, API에서 데이터를 받아서 변수에 넣어줌
    name = '갱쥬';
    // 불가능! 여전히 final 변수고, 딱 한번만 할당 가능하기 때문에
    name = '갱쥬당';
}
```

- 아래 코드는 `null safety` 예시
```javascript
void main() {
    late final String name;
    // 에러!
    print(name); // name이 late 변수이기 때문에 값을 넣기 전에는 접근 ❌ 
}
```

> `late`는 API 작업할 때 유용하게 사용!

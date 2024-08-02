### The Var Keyword

> 변수를 사용하는 방법은 두가지이다.

#### 1. `var` 사용하기

```javascript
// var 사용하기
void main() 
{
    var name = '갱쥬'; // String 으로 인식!
    name = '갱쥬다'; // 작동 ⭕️
    name = 1; // 작동 ❌, 1은 int!
}
```

#### 2. 명시적으로 타입 지정해주기

```javascript
void main() 
{
    String name = '갱쥬';
    name = '갱쥬다';
}
```

- 함수나 메소드 내부에 지역 변수를 선언할 때에는 `var`를 사용
- `class`나 `property`를 선언할 때에는 타입 지정  
- 함수 안에서 지역변수를 선언하거나, 메소드 안에서 지역변수를 선언하는 상황이라면 `var`를 사용!

### Dynamic Type

> `dynamic`은 여러가지 타입을 가질 수 있는 변수에 쓰는 키워드다.

- 아래 코드처럼 변수에 아무것도 지정하지 않으면, 타입은 `dynamic`
```javascript
void main()
{
    var name;
    name = '갱주';
    name = 1;
    name = true;
}
```

- `dynamic`으로 변수 사용 방법
```javascript
void main()
{
    dynamic name;
    
    if(name is String) {
     // 이렇게 작성하면, name 을 String 으로 인식    
    }
    
    if(name is int) {
    // 이렇게 작성하면, name 을 int 로 인식    
    }
    
    // 여기서 name의 type 은 dynamic!
}
```

> `dynamic`은 정말로 필요할때만 사용하기 🙆🏻‍♀️

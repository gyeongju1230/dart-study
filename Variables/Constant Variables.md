### Constant Variables

> `const`는 `compile-time`이 알고있는 값이어야 한다.

- dart 의 `const`는 JavaScript 나 TypeScript 와 다르다.   
- JavaScript 나 TypeScript 의 `const`는 dart 의 `final` 과 같다.

```javascript
void main() {
    // const는 앱스토어에 올리기 전에 이미 알고 있는 값을 다룰 때 사용!
    const max_allowed_price = 120;
}
``` 
- 만약, 앱스토어에 올라가기 전에 값을 미리 알고있다면 = `const`
- 어떤 값인지 모르거나 그 값이 API 로 부터 온다거나, 사용자가 화면에서 입력해야 하는 값이라면 = `final` or `var`


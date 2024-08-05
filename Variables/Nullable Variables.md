### Nullable Variables

> 개발자가 `null` 값을 참조할 수 없도록 하는 것!

```javascript
// NoSuchMethodError 발생
bool isEmpty(String string) => string.length == 0;

main() {
    isEmpty(null);
}

// null safety 사용
void main() {
    // '?' 로 String 이 될 수도, null 이 될 수도 있음을 표시할 수 있음
    String? name = 'name';
    name = null;

    // name 이 null 이 아니라면 isNotEmpty 속성을 줘!
    if (name != null) {
        name.isNotEmpty;
    } 
    
    name?.isNotEmpty; // 위 코드를 간단하게 작성
}
```

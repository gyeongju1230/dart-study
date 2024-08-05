### Recap

#### 변수를 만드는 두 가지 방법

```javascript
void main() {
    String name = '갱쥬'; // Type을 선언
    var name = '갱쥬'; // var 사용
    name = '갱쥬당당'; // 수정 가능
}
```

- 위처럼 만든 변수는 수정이 가능
- 대신, `Type`이 맞아야함! `int`면 `int`, `String`이면 `String`
- dart 스타일 가이드에 따르면, 메소드나 작은 함수 안에서 지역 변수를 선언할 때에는 `var`를 사용하는 게 권장됨
- 타입을 사용하는 방식은 `class`의 `property`를 작성할 때 사용하는 게 권장됨
- 

#### 값을 재할당하지 못하는 변수를 만드는 방법

```javascript
void main() {
    final name = '갱쥬';
    name = '갱쥬당당'; // 에러 발생, 재할당 불가
}
```

- 변수의 값을 수정하지 못하도록, 값을 딱 한 번만 할당하고 싶을 때 `final` 사용


#### 어떤 데이터가 들어올지 모를 때, 변수를 만드는 방법

```javascript
void main() {
    dynamic name;
    name = '갱쥬당당'; // String 일수도 있고
    name = 12; // number 일수도 있고
    name = true; // boolean 일수도 있고
}
```

- 위 코드처럼 작성하면 위험함, dart 의 보호를 받기 위해 아래 코드처럼 작성

```javascript
void main() {
    dynamic name;
    if (name is String) {
        // String 으로 할 수 있는 것들에 접근
    } // 확인
}
```

#### 컴파일 할 때 값을 알고있는 변수를 만드는 방법

- 앱을 컴파일하고 앱스토어에 올릴 때 그 값을 알고있다면, `const`사용
- `const`는 `compile-time` 상수니까!
```javascript
void main() {
    const api_key = '1212';
    api_key = '2121'; // 수정 불
}
```

- `const`와 `final`의 차이점은, `const`의 값은 컴파일 전에 알고있어야 하고(앱스토어에 올리기 전), `final`은 런타임 중에 만들어질 수 있다는 것

#### null 값을 참조하지 못하도록 막아주는 방법

```javascript
void main() {
    String name = '갱쥬';
    name = null; // null이 될 수 없음
}
```
- null safety
- 기본적으로, dart 의 모든 변수는 `nullable` 이 아니다.
- 즉, `null`이 될 수 없음!!

```javascript
void main() {
    String? name = '갱쥬'; 
    
    name.isEmpty; // 에러 발생, name이 null 일수도 있다고 알고있음
    
    // 올바른 사용 예 1
    name?.isEmpty;
    
    // 올바른 사용 예 2
    if (name != null) {
        name.isEmpty;
    }
    
}
```

- 만약, null이 될 수도 있음을 열려주고싶으면 `?` 추가

#### 아직 어떤 데이터가 올지 모를 때 알려주는 방법 

- `late`를 사용해서 dart 한테 어떤 데이터가 올지 모른다고 알리기
- `final`, `var`, `String` 앞에 써줄 수 있는 수식어

```javascript
void main() {
    late final name;
    late final String name;
    // 이렇게 변수를 선언하면, 사용하기 전에 데이터가 꼭 들어가야함
    name = '갱쥬';
    print(name); // name에 데이터가 들어가기전에는 사용 못함
}
```

- `late`는 API 에서 데이터를 가져올 때 사용

# Arrow function

---

```javascript
// 화살표 함수 구문
const myFnc = () => { // 키워드 function을 생략하였음
    ...
}
```

화살표 함수의 장점 및 필요성 -> this로 인해 생기는 많은 문제들을 해결해 줄 수 있음

화살표 함수 안에 this를 사용하면 항상 정의한 객체를 나타내고, 실행 중에 갑자기 바뀌지 않음

**연습**

```javascript
// 일반적인 함수 생성
function printMyName(myName) {
    console.log(myName);
}

printMyName('Max'); // Max
```

위의 예시를 arrow function으로 바꾸어 보면?

```javascript
// 화살표 함수
const printMyName = (myName) => { // function 키워드 생략 가능, 받는 인자가 하나일 경우 -> 괄호를 없앨 수 있음. 그 외의 경우엔 괄호 필수
    console.log(myName);
}

printMyName('Max'); // Max

//

const multiply = (number) => {
    return number * 2; // 함수의 본문에서 할 일이 return 해주는 것 뿐이라면? -> 중괄호랑 return 부분 제거하고 간단히 줄여 쓸 수 있음
}

console.log(multiply(3)); // 6

// 이렇게

const multiply = number => number * 2;
```

일반적으로 정의된 함수와 arrow function 사이의 비교

```javascript
// 일반적인 함수
function multiply(number) {
    return number * 2;
}

// arrow function
const multiply = number => number * 2; // 진짜 간단하게 쓸 수 있음
```


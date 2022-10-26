# js 숫자: 소수점, parseInt, NaN...

## 소수점

50000 = 5e4

0.0005 = 5e-4

이진법: 0b붙이

7 = 0b111

팔진법: 0 / 0o 붙이면

73 = 0111

16진법: 0x 붙이면

417 = 0x1a1

typeof 에서도 number로 인식

### 1. Math의 ceil(), floor(), round(): 소수점 이하 올림, 버림, 반올림 <a href="#1-math-ceil-floor-round" id="1-math-ceil-floor-round"></a>

* Math.ceil() : 소수점 이하 숫자를 올림하여 정수를 리턴

<pre class="language-javascript"><code class="lang-javascript"><strong>const num1 = 0.1234;
</strong>const num2 = 10.1234;
const num3 = 100.1234;

console.log(Math.ceil(num1));   // 1
console.log(Math.ceil(num2));   // 11
console.log(Math.ceil(num3));   // 101</code></pre>

* Math.floor() : 소수점 이하 숫자를 버림하여 정수를 리턴

```javascript
const num1 = 0.1234;
const num2 = 10.1234;
const num3 = 100.1234;

console.log(Math.floor(num1));   // 0
console.log(Math.floor(num2));   // 10
console.log(Math.floor(num3));   // 100
```

* Math.round() : 소수점 이하 숫자를 반올림하여 정수를 리턴

```javascript
const num1 = 0.1234;
const num2 = 10.1234;
const num3 = 100.5678;

console.log(Math.round(num1));   // 0
console.log(Math.round(num2));   // 10
console.log(Math.round(num3));   // 101
```

### 2. Number.toFixed(): 소수점 자리수 제거(n자리로 반올림) <a href="#2-numbertofixed-n" id="2-numbertofixed-n"></a>

숫자를 소수점 n자리로 반올림. n자리 이후의 숫자를 제거 가능

```javascript
const num1 = 0.1234;
const num2 = 10.1234;
const num3 = 100.5678;

console.log(num1.toFixed(3));   // 0.123
console.log(num2.toFixed(2));   // 10.12
console.log(num3.toFixed(2));   // 100.57
```

### 3. round(): 소수점 n자리 반올림 <a href="#3-round-n" id="3-round-n"></a>

n자리수로 반올림: `10^n` 곱하고 나누기!

```javascript
let num = 8.5678
let result = Math.round(num * 100) / 100;
console.log(result);  // 8.57

num = 10.1234
result = Math.round(num * 100) / 100;
console.log(result);  // 10.12

num = 203.5612
result = Math.round(num * 100) / 100;
console.log(result);  // 203.56
```

### 4. 소수점 n자리 올림 또는 버림 <a href="#4-n" id="4-n"></a>

```javascript
//올
let num = 10.1234
let result = Math.ceil(num * 100) / 100;
console.log(result);  // 10.13

//버림
num = 8.5678
result = Math.floor(num * 100) / 100;
console.log(result);  // 8.56
```

## 연산자 우선순위

| 우선순위 | 연산자(쉼표로 구분)                                                |
| ---- | ---------------------------------------------------------- |
| 20   | ()그룹화                                                      |
| 19   | . \[] new(인수포함) 함수호출()                                     |
| 18   | new(인수없이)                                                  |
| 17   | ++(후위) --(후위)                                              |
| 16   | ! \~ +(단항) -(단항) ++(전위) --(전위) typeof, void, delete, await |
| 15   | \*\*                                                       |
| 14   | \*  /  %                                                   |
| 13   | +(다항)  -(다항)                                               |
| 12   | <<  >>  >>>                                                |
| 11   | <  <=  >  >=  in  instanceof                               |
| 10   | ==  !=  ===  !==                                           |
| 9    | &                                                          |
| 8    | ^                                                          |
| 7    | \|                                                         |
| 6    | &&                                                         |
| 5    | \|\|                                                       |
| 4    | ? :(삼항 연산자)                                                |
| 3    | =  +=  -=  \*\*=  \*=  /=  %=  <<=  >>=  >>>=  &=  ^=  \|= |
| 2    | yield  yield\*                                             |
| 1    | ,(쉼표)                                                      |

## 소수/실수 계산시 조심할 것

실수 연산 시 2진법으로 계산이 되기 때문에&#x20;

0.1 + 0.2 = 0.3이 아

실수계산시 (0.3 \* 10 - 0.1 \* 10) / 10; 해서 계산하는 방법을 사용

## NaN

Not a Number = typeof 에서는 number로 인식

## 문자열 숫자로 변환

perseInt('123') = 문자였던 123이 숫자 123이 된다.&#x20;

// 가진 값에서 숫자를 뽑아 변환 시키거나, parseInt(111, 2)로 사용하면 111을 2진법으로 계산하라는 식으로 사용할 수 있다.(111 = 7이다)

Number('123') = 문자였던 123이 숫자 123이 된다. // 숫자인지 아닌지를 판별

## 문자열 ↔ 정수로 변환

parseInt('3.14') = 3&#x20;

parseFloat('3.14') = 3.14&#x20;

\* parseInt() → 정수로 바꾼다

\* parseFloat() → 소수로 바꾼다.

## 연산자

\+ (더하기), - (빼기), / (나누기), \* (곱하기), % (나머지 구하), \*\*(거듭 제곱)

## 무한 값

숫자를 0으로 나눌 경우 infinity 산출

\-값을 0으로 나눌 경우 -infinity 산

\= typeof에서 숫자로 인

단, 0/0을 나눌 경우 NaN 산

## 형 변환(type casting)

(1) '문자열' + 123 = '문자열123'

문자열과 숫자가 결합, 숫자가 문자열로 변환된&#x20;

(2) - , \* , / 사용

'문자열' - 0 = NaN = Number('문자열') - 0 = NaN&#x20;

'-'는 다른 자료형이 숫자가 된 후 연 진행

단, '숫자' - 0 = 숫자가 나

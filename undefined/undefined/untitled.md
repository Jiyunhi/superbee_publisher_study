# 03. 데이터 타입, data types, let vs var, hoisting

```javascript
//1. Use strict
//added in ES 5
//use this for 바닐라 자바스크립트
'use strict';

//2. Variable(변수): rw(read/write)가 가
// 1) let (added in ES6)
let name= 'ellie';
console.log('name');
name='hello';
console.log(name);
//변수를 정의하게 되면 메모리를 지정해서 이야기할 수 있다는 것
//변수는 변경 가능
//{}:블럭으로 가둬놓을 수 있음 그 안에서만 작동하는 
//{}이 없을 경우 === 파일에 바로 정의하는 것: global scope → 항상 메모리에 탑재되는 것, 최소화하기

// 2) var
var age;
age=4;
//보통은 이렇게 함수를 선언 후 값을 정의해서 나타내지만, 
//var는 그런 것 상관없이 어디에서든 선언, 호출이 가 === var hoisting
//hoisting === 어디서 선언했든 항상 제일 위로 선언을 끌어올려주는 것 입니다.
//block scope이 없음 = 블럭 스콥을 무시하고 작용한다는 것

//3. Constant: read만 가능
const num;
num = 15;
//변하지 않는 상수(변경 불가능=immutable)
//보안상 좋음, thread 안전성

//NOTE!!!!!
//Immutabl(변경 불가능) data types: 
    //premitive types, frozen objects(i.e. object.freeze())
//Mutable data types: all objects by default are mutable in JS
    //favor immutable data type always for a few reasons:
    //- security
    //- thread safety
    //- reduce human mistakes


//4. 데이터 타입 종류
// 1) primitive: 한가지 아이템, 값 자체가 한번에 올라간다.(boolean, 숫자, string, null, undefined, symbol) 
//    object: 한가지 아이템들을 묶은 것, 
//    function: first-class function이 지원 - 변수할당 가능, 함수의 인자, 리턴도 가능
const count = 17;//integer
const size = 17.1;//decimal number
console.log(`value: ${count}, type: ${typeof count}`);
console.log(`value: ${size}, type: ${typeof size}`);

// 2) number - special numberic values: infinity, -infinity, NaN
const infinity = 1 / 0 // +값을 0으로 나눌 경우
const negativeInfinity = -1 / 0 // -값을 0으로 나눌 경우
const nAn ='not a number'/ 2;//'string 값'을 숫자로 나눌 경우
console.log(infinity);
console.log(negativeInfinity);
console.log(nAn);

// 3) bigInt 
//자바스크립트 숫자 범위: -2^53 ~ 2^53까지
const bigInt = 1234567890123456789012345678901234567890n;
console.log(`value: ${bigInt}, type: ${typeof bigInt}`);

// 4) string
const char ='c';
const brendan = 'brendan';
const greeting = 'hello'+brendan;
console.log(`value:${greeting}, type: ${typeof greeting}`);
const helloBob=`hi ${brendan}!`;//template literals(string) 
// `(Backtick)을 붙여서 나타내면 변수의 값이 붙여져서 나온다. 
//예시
console.log(`value:${helloBob}, type: ${typeof helloBob}`);
console.log('value: '+helloBob+' type: '+typeof helloBob);

// 5) boolean
// true: 어떤 수든, true / false: 0, null, undefined, NaN, '비어진 스트링'
const canRead = true;
const test = 3<1; //false
console.log(`value: ${canRead}, type: ${typeof canRead}`);
console.log(`value: ${test}, type: ${typeof test}`);

// 6) null: 명확하게 아무것도 없는 애라고 지정한 
let nothing= null;
console.log(`value: ${nothing}, type: ${typeof nothing}`);

// 7) undefined: 선언은 되었지만 값이 없거나, 찾지 못했을 
let x;
console.log(`value: ${x}, type: ${typeof x}`);

// 8) symbol: 고유한 식별자가 필요하거나 동시에 발생할 수 있는 일에 순서를 주고 싶을 때
const symbol1 = Symbol('id'); 
const symbol2 = Symbol('id');
console.log(symbol1 === symbol2);
//false: 둘은 동일한 식별자래도 고유한 식별자를 만들기에, 다른 값이

const gSymbol1 = Symbol.for('id'); //주어진 식별자와 어울리는 식별자를 만듬
const gSymbol2 = Symbol.for('id');
console.log(gSymbol1 === gSymbol2);//true
console.log(`value: ${symbol1}, type: ${typeof symbol1}`);
// ▲ 오류난다 이러면
console.log(`value: ${symbol1.description}, type: ${typeof symbol1.description}`);
// ▲ 이렇게 해야 오류가 안

//5. 다이나믹 타이핑: 변수 선언시 어떤 타입인지 결정해서 하지 않고 
//   런타임시 할당된 값에 따라서 달라질 수 있다.
let text='hello';
console.log(text.charAt(0));//h, 인덱스는 0부터 시작
console.log(`value: ${text}, type: ${typeof text}`);//스트링 타입
text = 1;
console.log(`value: ${text}, type: ${typeof text}`);//넘버 타
text = '7' + 5;
console.log(`value: ${text}, type: ${typeof text}`);//스트링 + 스트링으로 변환
text = '8' / '2';
console.log(`value: ${text}, type: ${typeof text}`)//넘버 타입으로 변환
console.log(text.charAt(0));//에러 발생 → 타입 스크립트가 등장

//6. object, real-life object, data structure
const ellie = {name:'ellie', age:20};
//코드로 ellie.name/age = 'she'/30; 로 변환은 가능하나 ellie 값을 바꿀 수는 없음


```

# Arrays / Object / Function / Recap / Returns / Conditionals

```javascript
function plus(a, b){//아무거나 넣을 수 있어
    console.log(a + b);//a, b는 function 안에서만 존재하는 것!
}
function divide(a, b){
    console.log(a / b);
}
plus(8, 16);
divide(3, 10);

const player ={
    name: "ji Yun",
    sayHello: function(otherPersonName){
        console.log("hello! "+otherPersonName+" nice to meet you");
    },
};
console.log(player.name);
player.sayHello("lynn");
player.sayHello("Ji yun");

const a = 5;
let isNicoFat = false;
isNicoFat = true;
console.log(a);
console.log(isNicoFat);

const toBuy = ["right", "bottom","top"];
console.log(toBuy);
console.log(toBuy[2]);//top
toBuy[2] = "left";
console.log(toBuy);
toBuy.push("meat");//meat 추가
console.log(toBuy);

const game = {
    player: "nico",
    age: 88,
};
console.log(game, console);
console.log(game.player);
game.player="ji yun";
console.log(game);
game.sexy = "soon";
console.log(game);

function plus(first, second){
    console.log(first + second);
};
plus(8, 8);


// const calculator={
//     add: function(one, two){
//         console.log(one + two);
//     },
//     minus: function(one, two){
//         console.log(one - two);
//     },
//     divide: function(one, two){
//         console.log(one / two);
//     },
//     multiply: function(one, two){
//         console.log(one * two);
//     },
//     powerOf: function(one, two){
//         console.log(one ** two);
//     },
// };
// calculator.add(10,1);
// calculator.minus(3,1);
// calculator.divide(25,5);
// calculator.multiply(65,8);
// calculator.powerOf(2,8);

const age = 96;
function calculateKrAge(ageOfForeigner){
    return ageOfForeigner +2;//function 안에서 바깥으로 소통하는 방식으로 return을 사용한다. 이후 발생하는 코드는 작동하지 않고 return후 코드작동은 멈춘다.
}
const krAge=calculateKrAge(age);
console.log(krAge);

const calculator={
    add: function(one, two){
        return (one + two);
    },
    minus: function(one, two){
        return (one - two);
    },
    divide: function(one, two){
        return (one / two);
    },
    multiply: function(one, two){
        return (one * two);
    },
    powerOf: function(one, two){
        return (one ** two);
    },
};
const plusResult = calculator.add(5,3); //plusResult를 콘솔하면 정의되지 않은 것으로 나옴: function은 그래!
const minusResult = calculator.minus(2,3);
const divideResult = calculator.divide(minusResult,3);
const multiplyResult = calculator.multiply(plusResult,3);
const powerOfResult = calculator.powerOf(2,divideResult);
console.log(plusResult , minusResult , divideResult , multiplyResult);

//string을 number로 바꾸기 : parseInt("string이었던 것")
//const howOldAreYou = prompt("How old are you?");
// 결국 작성하는 모든 string 숫자를 number 숫자로 바꿔주는 것은
const howOldAreYou = parseInt(prompt("How old are you?")); 
console.log(howOldAreYou);

// console.log(typeof howOldAreYou); 이것은 string인지 number인지 알 수 있는 거: typeof
// console.log(typeof "15", typeof parseInt("15"));
// console.log(howOldAreYou, parseInt(howOldAreYou));

const drinkAge = parseInt(prompt("How old are you?"));
console.log(isNaN(drinkAge)); // boolean을 반환, isNaN(e) = e가 숫자인지 알고 싶을 때 사용하는 것 /true = NaN이라는 뜻
console.log(drinkAge);

// if(condition=조건=boolean){
//     //condition === true
            //실행할 코드
// } else{
//     //condition === false
// }

if(isNaN(drinkAge)){
    console.log("Please write a number.");//조건문이라서 true일때 if해당 콘솔이 출력
} else{
    console.log("Thank you for writing your age");//false 일때 출력
}
```

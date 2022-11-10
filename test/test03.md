# test03

````javascript
# test 3회차

<br>

```javascript
{
  // a = 1; b = 2; 일때 a와 b가 같다면 1 , 같지 않다면 -1 을 출력시키세요.

  const a = 1;
  const b = 2;

  if(a==b){
    document.write('1');
  }else{
    document.write('-1');
  }
}
```

<br>

```javascript
{
  // 첫 번째 분수의 분자와 분모를 뜻하는 num0, num1, 
  // 두 번째 분수의 분자와 분모를 뜻하는 num2, num3가 매개변수로 주어집니다. 
  // 두 분수를 더한 값을 기약 분수로 나타냈을 때 분자와 분모를 순서대로 담은 배열을 return하세요.

  // 제한사항
  // 0 < num0, num1 , num2 , num3 < 1,000

  // 입출력 예 num = 0 , num1 = 2, num3 = 3, num4 = 4, result = [5, 4]
  
  let num0 = 1;
  let num1 = 2;
  let num2 = 3;
  let num3 = 4;

  // 분자
  let topNum = num1 * num2 + num0 * num3;
  // 분모
  let botNum = num1 * num3;

  let maxinum = 1;
  // 최소 공배수
  let i = 0;

  for (i = 1; i <= topNum; i++){
    if(topNum % i ===0 && botNum % i ===0){
      maxinum = i;
    }}
  
  document.write(topNum / maxinum + ', ' +  botNum / maxinum );
  
  let answer = [topNum / maxinum,  botNum / maxinum];  
}
```

<br>

```javascript
{
  // 시험성적 A 90 ~ 100점
  // 시험성적 B 70 ~ 89점
  // 시험성적 C 50 ~ 69점
  // 시험성적 D 40 ~ 49점
  // 시험성적 F 그 이하 점수

  // 시험성적은 0 ~ 100 점 까지며
  // 각 상황별로 등급표가 나오게 코드를 작성해주세요
  // 0 ~ 100 외의 값일 경우 "점수를 다시입력해주세요" 를 리턴해주세요.
  let answer = 0;

  let i = 0;

  if( 89 < i <= 100 ){
    document.write('A');
  }else if(69 < i < 90){
    document.write('B');
  }else if(49 < i < 70){
    document.write('C');
  }else if(39 < i < 50){
    document.write('D');
  else if(0 <= i < 40){
    document.write('F');
  }else{
    alert('점수를 다시입력해주세요.');
  }
```
````

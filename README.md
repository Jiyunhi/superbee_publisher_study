# 1\~10과



```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>script</title>
</head>
<body>
    <script>
        // 01. 변수 : 데이터 저장소, 데이터 변경, 데이터 추가
        {
            var x = 100;
            var y = 200;
            var z = 'js';

            document.write('*********** 01. 변수 ***********<br>');
            document.write(x, '<br>');
            document.write(y, '<br>');
            document.write(z, '<br>');
            document.write(x + y, '<br>');
            document.write(x % y, '<br><br>');// 나머지 구하
            document.write(Math.floor(y / x), '<br><br>'); // 몫 구하
        }

        // 02. 변수 : 변하는 데이터
        {
            let x = 100;
            let y = 200;
            let z = 'js';
            
            //재선언 해야
            x = 200;
            y = 300;
            z = 'javascript';

            document.write('*********** 02. 변수 ***********<br>');
            document.write(x, '<br>');
            document.write(y, '<br>');
            document.write(z, '<br>');
            document.write(x + y, '<br>');
            document.write(x % y, '<br><br>');// 나머지 구하
            document.write(Math.floor (y / x), '<br><br>'); // 몫 구하
        }

        // 03. 상수 : 데이터 저장소, 변하지 않는 데이터
        {
            const x = 100;
            const y = 200;
            const z = 'js';
            // 재 선언 재 할당 안됨!
            document.write('*********** 03. 상수 ***********<br>');
            document.write(x, '<br>');
            document.write(y, '<br>');
            document.write(z, '<br>');
            document.write(x + y, '<br>');
            document.write(x % y, '<br><br>'); //나머지 구하기
            document.write(Math.floor (y / x), '<br><br>'); //몫 구하기
        }

        
        // 04. 배열 : 데이터 저장소, 여러개를 저장, 배열 선언1
        {
            const arr1 = new Array();//익명 함수 만드는 것, 처음지정한 함수는 재지정가능
            arr1[0] = 100;
            arr1[1] = 200;
            arr1[2] = 'javascript';

            document.write('*********** 04. 배열 ***********<br>');
            document.write(arr1[0], '<br><br>');
        }

        // 05. 배열 : 데이터 저장소, 여러개를 저장, 배열 선언2
        {
            const arr2 = new Array(100, 200, 'javascript')
            document.write('*********** 05. 배열 ***********<br>');
            document.write(arr2[0], '<br>');
            document.write(arr2[1], '<br>');
            document.write(arr2[2], '<br><br>');
        }

        // 06. 배열 : 데이터 저장소, 여러개를 저장, 배열 선언3
        {
            const arr3 = []
            arr3[0] = 100;
            arr3[1] = 200;
            arr3[2] = 'javascript';
            document.write('*********** 06. 배열 ***********<br>');
            document.write(arr3[0], '<br>');
            document.write(arr3[1], '<br>');
            document.write(arr3[2], '<br><br>');
            //할당은 가능하지만 재 선언은 안
        }

        // 07. 배열 : 데이터 저장소, 여러개를 저장, 배열 선언4
        {
            const arr4 = [100, 200, 'javascript']

            document.write('*********** 07. 배열 ***********<br>');
            document.write(arr4[0], '<br>');
            document.write(arr4[1], '<br>');
            document.write(arr4[2], '<br><br>');
        }

        // 08. 2차 배열
        {
            const arr5 = [100, 200, ['javascript' , 'react'] ];

            document.write('*********** 08. 2차 배열 ***********<br>');
            document.write(arr5[2][1], '<br><br>');//arr5의 3번째의 2번째
        }

        // 09. 배열 갯수
        {
            const arr6 = [100, 200, 300, 400, 500];
            document.write('*********** 09. 배열 갯수 ***********<br>');
            document.write(arr6.length, '<br><br>');
        }

        // 10. 배열 불러오기
        {
            const arr7 = [100, 200, 300, 400, 500];
            document.write('*********** 10. 배열 불러오기 ***********<br>');
            for (let i = 0; i < arr7.length; i++){
                document.write(arr7[i], '<br>');
            }
        }
        
        //최댓값 구하기 - 구글링
        {
            const fruits = ['사과', '체리', '바나나', '자두', '배']
            const amount = fruits.length;// 배열의 길이 반환
            const newStr = fruits.join('/');// 이걸 넣어서 묶는다.
            const newArr = fruits.reverse();// 배열 순서를 반대로 바꿔준다.
            const newArr2 = fruits.sort();// 가나다 순으로 정리해준다.
            const newArr3 = fruits.sort(function(a,b){
                return b-a; 
            });// 가나다 순으로 정리해준다.

            document.write(fruits, '<br>');
            document.write(fruits[0], '<br>');
            document.write(amount, '<br>');
            document.write(newStr, '<br><br>');
            document.write(newArr, '<br><br>');
            document.write(newArr2, '<br><br>');

        }
    </script>
</body>
</html>
```

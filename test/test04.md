# test04

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <ul>
        <li>1</li>
        <li>2</li>
        <li>3</li>
        <li>4</li>
    </ul>
    <style>
    </style>
    <script>
        // 13. 배열 데이터 불러오기(for in문)
        // 반복문 / 배열을 조건으로 적고 배열을 증가값으로 잡음. 초기값과 해당되는 배열안에서만 선정해줌
        {
            const arr10 = [100, 200, 300, 400, 500];

            document.write('*********** 13. 배열 데이터 불러오기(for in문) ***********<br>');
            
            for(let i in arr10){
                document.write(arr10[i], '<br>');
            }
            document.write('<br>');
        }


        // 14. 배열 데이터 불러오기(for of문)
        // 반복문 / 배열을 조건으로 적고 배열을 증가값으로 잡음. 초기값과 해당되는 배열안에서만 선정해줌
        {
            const arr11 = [100, 200, 300, 400, 500];

            document.write('*********** 14. 배열 데이터 불러오기(for of문) ***********<br>');
            
            for(let i of arr11){
                document.write(i, '<br>');
            }
            document.write('<br>');
        }

        {
            // for in 문을 통해 index 번호를 호출하시오
            // 출력 예시 0 1 2 3
            const arr = [100, '100', 200, 300];
            for(i in arr){
                console.log(i);
            }
        }

        {
        // <ul>
            // <li>1</li>
            // <li>2</li>
            // <li>3</li>
            // <li>4</li>
            // </ul>

        // for of 문을 이용하여 3만 출력하시오
        // 3만 출력시키오
        let li = document.querySelectorAll('ul > li');
            for(const i of li){
                console.log(i);
                i.style.display = 'none';
        }li[2].style.display = 'block';
        }
    </script>
</body>
</html>
```

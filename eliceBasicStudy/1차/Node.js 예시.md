## 1. 백준 1152번
* 입력: 한 줄의 공백이 포함된 문자열

   * 앞 뒤에도 공백 존재할 수 있음

* 출력: 단어의 개수

```
const readline = require("readline");

const rl = readline.createInterface({   // rl라는 변수에 input 값을 넣어줌
    input: process.stdin,
    output: process.stdout,
});

let input;

rl.on("line", (line) => {     // 변수 rl에서 1줄씩 값을 받아와 line에 대입
    input = line;             // 선언된 빈 변수에 1줄씩 넣어주기   
    rl.close();
    
}).on("close", function () {
    solution(input);
    process.exit();
});


const solution = (input) => {
    const arr = input.trim().split(" ");
    
    if (arr[0] === "") arr.shift();
    if (arr[arr.length - 1] === "") arr.pop();

    console.log(arr.length);
}
```

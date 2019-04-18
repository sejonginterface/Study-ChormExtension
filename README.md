<h1 align="center">Study ChormExtension</h1>
    
> 크롬확장프로그램 제작 스터디

### 자바스크립트 기초
#### 출력 방식
```javascript
console.log("Hello Javascript");
//콘솔창에 메세지 띄움 > F12 > console

alert("Hello Javascript");
//웹 실행 전 프롬프트 창 띄움 > 단순 확인 버튼 경고창

prompt("Hello Javascript");
//웹 실행 전 사용자에게 입력 받을 수 있는 프롬프트 창 띄움

var val1 = "1", val2 = "2", val3 = "3"
//변수 정의와 초기화

console.log(val1);
alert(val2);
prompt(val3);
```

#### 변수
```javascript
var a = 100;
var b = 3.14;
var c = "안녕하세요";
var d = "a"
var e = true
var f = false

//typeof(변수) => 해당 변수의 자료형 반환
console.log(a,typeof(a)); //number
console.log(b,typeof(b)); //number
console.log(c,typeof(c)); //string
console.log(d,typeof(d)); //string
console.log(e,typeof(e)); //boolean
console.log(f,typeof(f)); //boolean
```

#### 입력 방식
```javascript
var height = prompt("키를 입력해 주세요");
//변수 height에 사용자에게 입력받은 값을 저장

console.log(height, typeof(height));
//prompt로 입력받은 값은 string으로 저장되므로 자료형 변환이 필요함
```

#### 자료형 변환
```javascript
var height_int = parseInt(height);
//parseInt(변수) > 변수 값을 정수로 반환
console.log(height_int, typeof(height_int)) 
//(정수 값) number

var height_float = parseFloat(height);
//parseFloat(변수) > 변수 값을 실수로 반환
console.log(height_float, typeof(height_float));
//(실수 값) number
```

#### prompt에서 입력받은 string이 number 변환 가능할 때
1. "185"          정수형
2. "152.2"        실수형
3. "123 입니다"    수가 앞부터 시작할 때

#### 객체(object)
```javascript
var man = {name:"홍길동", age:20, height:180 };
//객채명 = {속성명:--}

console.log(typeof(man));   //object
console.log(man.name);      //"홍길동"
console.log(man["name"]);   //"홍길동"

//속성 값 변환
man.name = "전우치";
console.log(man.name);     //"전우치"

man["name"] = "이몽룡"
console.log(man.name);     //"이몽룡"

console.log(man);          //객체 man 콘솔 창에 출력
```

#### undefined, NULL
```javascript
var a; //undefined 
typeof(a); //undefined
//변수 값이 정의되지 않은 값

var b = null //NULL
typeof(b); //object
//개발자가 의도적으로 정의하지 않은 값
```

#### 연산자
```javascript
var a = 8;
var b = 7;

console.log(a+b);
console.log(a-b);
console.log(a*b);
console.log(a/b);
console.log(a%b);

console.log(a++); //8
console.log(a);   //9

console.log(++a); //10
console.log(a);   //10

console.log(Math.pow(2,3)); //2의 3승 = 8
console.log(Math.sqrt(16)); //16의 제곱근 = 4
console.log(Math.random()); //0~1사이의 난수
```

#### 함수
```javascript
console.log(test()); //10 반환
//함수 정의
function test(){
    return 10;
}
```
```javascript
function sum(num1,num2){
    return num1+num2;
}

//콘솔 창에서
//sum(1,2); >> 3 반환

```


#### 문자열
```javascript
var str = "Hello";

console.log(str.length);    //5 >> str의 크기
console.log(str["length"]); //5 >> str의 크기

var str2 = " World"
var str3 = str.concat(str2); //str3 = str+str2
console.log(str3);           //"Hello World"

var str4 = "Hello".concat(str2).concat("!");
//str4 = "Hello"+str2+"!"
console.log(str4);          //"Hello World!"

//덧셈 연산자로도 가능
console.log(str + str2);
console.log(str + str2 + "!");

//수 가능
console.log("pi is "+3.14); //"pi is 3.14"
console.log(3.14+" is pi"); //"3.14 is pi"
```

```javascript
var str = "abcdeabcde";
//해당 순서에 있는 문자 반환

str.charAt(0);  //"a"
str.charAt(9);  //"e"
str.charAt(10); //""

str[0];         //"a"
str[9];         //"e"
str[10];        //undefined
```

```javascript
var str = "abcdeabcde";
//해당 서브스트링 반환

str.substring(2,4); //==str[2:4] >> "cd"
str.substring(2);   //==str[2:]  >> "cdeabcde"

str.substr(2,4);    //==str[2:2+4] >> "cdea"
str.substr(2);      //==str[2:]    >> "cdeabcde"
```

```javascript
var str = "abcdeabcde";
//해당 서브스트링의 순서 값 반환

//서브스트링이 나오는 가장 첫번째
str.indexOf("bc"); //1
str.indexOf("e");  //4  

//서브스트링이 나오는 가장 마지막
str.lastIndexOf("bc"); //6
str.lastIndexOf("e");  //9
```


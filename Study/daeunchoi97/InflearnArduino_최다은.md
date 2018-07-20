## 기본 함수
setup() // 한번만 실행  
loop() // 무한 루프  
pinMode( , )// 앞부분은 포트# , 뒷부분에는 INPUT, OUTPUT, INPUTPULL  
digitalWrite ( , )// 뒷부분에 HIGH, LOW  
delay()// 1000 == 1s  

## 시리얼 통신
Serial.begin (9600) // 숫자 넣기-보통은 9600  (setup 함수에 들어감)  
Serial.available() // serial값의 유무  
Serial.println() //  
Serial.read() //  
ex)   Serial.println(Serial.read())// 시리얼을 그대로 출력  
serialEvent() // 시리얼이 돌아가면 무조건 불러와지는 함수   
parseInt() // 시리얼에 12을 입력할 경우 보통 1,2 각각의 아스키 코드를 출력하나 parseInt를 쓰면 원래 숫자로 출력해줌(하지만 너무 큰 값은 쓰레기값으로 출력)
 


## print vs. println 의 차이 
print - 그냥 출력   
println - 출력+"/n" (print line 이라고 읽음 )

## 스위치
INPUT   
OUTPUT  
INPUTPULLUP //내부저항을 이용해서 사용함(저항이 없어도 됨)  
digitalRead()//포트 번호 하나만 넣어주면 그 값을 읽음

-Pullup Pulldown이 이해가 안됨

## LED밝기 조절(PWM)
analogWrite( , )// 포트#, 값  
(LED는 0~255까지만)  
-> 이러한 값같은 거 확인할 떄 Serial.println사용하면 좋음, 하지만 값이 숫자이고 앞에 붙는 말이 string 일 경우 Serial.println("아무말" + (string)값);

## 시리얼을 통해서 밝기 조절
변수에 Serial.parseInt()를 넣어서 analogWrite (pin#,변수);

## LED 밝기를 조절하자 (AnalogIn)
조도센서 이용 - 빛이 많을 수록 저항이 더 커짐


## map함수 이용하기 
analogRead()// 0~1023의 값 (volt값이 들어온다)  
map(value, fromLow, fromHigh, toLow, toHigh) // 

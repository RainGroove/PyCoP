1장  파이썬이란 무엇인가?
====

#### 사칙연산
더하기 +, 빼기- , 나눗셈 / , 곱셈 *		  
1+2 = 3  
2/2 = 1  
7/4 = 1.75  
7//4 = 1 (0.75는 삭제하고 1만 리턴된다)  
7 % 3 = 1 (나눗셈 후 나머지를 반환하는 연산)  
2*2 = 4  

3****2 = 9 제곱은 별두개로 표현한다  


#### 변수(숫자대입)
a = 1  
b = 2  
a + b   
3이 출력됨  

#### 변수(문자대입)
a = "Python"  
print(a)  
Python 출력   

파이썬은 a = "Python"이라고 대입하고  
a를 호출하면  
Pyhon이 출력된다  
즉 Print문을 생략할 수 있다  


#### 조건문 if
 if a > 1 :  
print ("a better than 1")  
a better than 1 가 출력됨  

그러나  
if a < 1 :  
print ("a not better than 1")  
입력하면 반응이 없다  
1보다 크기 때문이다  

#### 반복문 for
for를 이용해서 값을 하나씩 출력함  
for a in [1,2,3]  
print(a)  
파이썬에서 for a in은 배열의 앞부터 하나씩 출력해준다  


#### 반복문 while
while은 ~인 동안 반복이라는 뜻이다.  
i = 0 // 을 정의하고  
while i < 3 : //i가 3보다 작을 때까지  
i = i + 1 // i가 1씩 증가할 때  
print (i) //프린트 i값을 해라  
1  
2  
3  
으로 출력한다  


#### 함수
def는 파이썬에서 함수를 만들때 사용한다.  
add라는 함수를 만들고 (a,b) 로 정의하였다.  

def add(a,b):   
return a+b  
add(3,4)  
7 출력  

def add(a,b,c):  
return a+b-c  
add(1,2,3)  
0 이 출력함  

add라는 함수에 배열을 a,b,c 3개 만들고  
리턴 a+b-c한다  
add (1,2,3)  
을 입력하니까 0이 출력됨  



2장 파이썬 기초 및 자료
====

#### 02-1 숫자형
숫자형이란 (Number)를 말하는 것  
123같은 정수  

13.12.34실수 소수점이 포함된  
4.24e10은 4.24000000000 이다  
4.23 * 10^10을 의미한다  

8진수 0o34, 0o25  
16진수 0x2A, 0xFF  

#### 문제풀이 1
a = 80  
b = 90  
c = 100  

a+b+c  
270  

a+b+c/3  
203.33333333333334  

#### 문제풀이 2 홀짝 구분

1 % 2  
1  
2 % 2  
0  
3 % 2  
1  
4 % 2  
0  
5 % 2  
1  

#### 02-2 문자열자료형
#### 따옴표이용하기  
\n,(행바꿈)  
\t,(수평탭)   
\\, (문자)  
\', (단일 인용부호)  
\" (이중 인용부호) 를 이용한다  

#### 문자열 더하고 곱하기
head = "py"  
tail = "cococ"  
head+tail =   
pycococ 출력  

head * 2  
pypy 출력  

print("=" * 50)  
print("My Program")  
print("=" * 50)  

#### 문자열 길이구하기&인덱싱
a = "life is too short"  
len(a)  
17 // 길이 값이 출력된다  

###### 파이썬은 0부터 숫자를 센다!!!(문자열 인덱싱)
a[번호]를 입력하면  
문자열을 인덱싱 할 수 있다  

문자열 슬라이싱이란?  
한문자만을 뽑아내어 하나로 만드는 것  
b = a[0]+a[1]+a[2]+a[3]  
b를 호출하면  
life 라고 출력됨  

a [0:4]라고 해도 같은 결과를 도출한다  
0부터 4번까지 의미이다.  

가장 많이 사용하는 코드  

a = "2190101Rainy"  
time = a[:8]  
weather = a[8:]  

#### 문자열 포매팅  

1) 숫자바로 대입  
"i eat %d apples" % 3  

2) 문자열 바로대입  
"i eat %s apples" %"five"  

3) 변수로 대입  
number = 3  
"i eat %d apples" %number  

"i eat {0} apples" .format(number)  
format함수를 이용하여 변수로도 입력 가능하다  
"i eat {0} apples {1}" .format(number,number2)  
number, number2 변수를 지정 하면 중복으로가능함  
      


%s 문자열 string  
%d 정수 integer  
%c 문자1개 character  
%f 부동소수 (floating-point)  
%% %퍼센트 자체  
ex) %s%%  

4)소수점 표현  
"%0.4f %3.42134234  
'3.4213'  
0.4는 . 은 쩜을 나타내고 4는 쩜 다음 자리수를 의미함  

#### 문자열 관련 함수들  
1) 문자개수세기(count)  
a= "hell"  
a.count('l')  

2) 위치알려주기(find)  
a = "hell"  
a.find('e') -> 2를 출력  
a.find('b') -> 없는경우 -1을 출력  

3) 위치알려주기(index)  


4) 문자열삽입(join)  
",".join(['a','b']) -> 'a,b' 출력  

5) 소문자를대문자로바꾸기(upper)  
6) 대문자를소문자로바꾸기(lower)  
7) 좌우공백지우기 (lstrip, rstrip, strip)  
8) 문자열 나누기 (split)  


#### 02-3 리스트자료형  
자료형의 하나로 집합을 메모리에 올린 값이다  

리스트명 = [요소1, 요소2, 요소3,,,,,]  
a[]  
b[1,2,3]  
c[1,a,b]  
이처럼 메모리에 null값, 숫자형, 문자열을 정의가능하다  

#### 리스트의 인덱싱  
a = [1,2,3]  
a[0] -> 1을 출력한다  
a[0] +a[2] ->4를 출력한다  

a = [1,2,['a','b']]  
이렇게 0,1,2인 리스트에 2번 메모리 영역에 리스트를 중복하여 지정할 수있다. 3중으로도 쓰지만 복잡해서 잘안쓴다  
a[2] -> []'a','b'] 출력  

#### 리스트의 슬라이딩  
문자열과 동일하다  
a = "12345"  
a[0:2] -> 12 출력  

##### 리스트 연산  
리스트 더하기  
a = [1,2]  
b = [3,4]  
a + b --> [1,2,3,4]  

리스트 반복하기  
a * 3 -> [1,2,1,2,1,2]   

리스트 길이구하기  
len(a) --> 2 출력  


##### 리스트 수정 삭제
값 수정  
a =[1,2]  
a[1] =4  
a --> 1,4  

값 삭제  
del a[1]  
a --> 1  
del 객채 함수를 사용한다.  

##### 리스트 함수
1) 리스트에 요소 추가 (append)  
덧붙이다. 첨부하다는 뜻으로 맨 마지막에 추가한다  
a = [1,2,3]  
a.append(4)  

2) 리스트 정렬 (sort)  
a = [1,4,2,3]  
a.sort()  
하면 1,2,3,4나 문자열은 a,b,c로 정렬한다  

3) 리스트 뒤집기 (reverse)  
sort와 반대로 거꾸로 뒤집는다  
3개라면 가운데는 그대로이다  

4) 리스트 위치반환 (index)  
a.index(3)  
이면 3의 위치를 리턴함  

5) 리스트 삽입 (insert)  
a.insert(3,5)  
리스트 3번에 5를 입력하라는 뜻이다  

6) 리스트 제거 (remove)  
첫번째 위치한 3만 제거됨  
a.remove(3)  


7) 리스트 요소 끄집어내기 (pop)  
a = [1,2,3]  
a.pop()  
3  
a --> 1,2 만 출력됨  
빼면서 호출해주고 삭제한다  


8) 리스트 요소 x 개수 세기 (count)  
리스트내 변수가 몇개 있는지  
a = [1,2,3,1]  
a.count(1)  
2   

9) 리스트 확장 (extend)  
a =[1,2]  
a.extend([3])  
a   
[1,2,3]  


#### 02-4 튜플  
리스트는 값의 생성, 삭제, 수정이 가능하지만  
튜플은 그값을 바끌수 없다  
[]리스트  
()튜플  

#### 02-5 딕셔너리 자료형  
딕셔너리는 연관배열, 해시라고 한다  

dic = {key1:value1, key2:value2.....}  
의구조를 갖고있다  

추가하기  
a = {1:'a'}  
a[2] = 'b'  
{1 : 'a', 2:'b'}  

삭제하기  
del a[1]  

#### 딕셔너리 key를 사용해 value를 얻기  
변수명 key를 이용한다.  
{1 : 'a', 2:'b'}  
a[1] -> 입력하면 'a'라는 value값을 호출함  

##### 딕셔너리 key리스트 만들기(keys)  
key들만 추출할 때 사용  
a.keys()  
dict_keys(['1','2'])  

##### 딕셔너리 values 리스트만들기(values)  
a.values()  
dict_values (['a','b'])  

##### 딕셔너리 모두지우기(clear)
a.clear()  

##### Key로 Value값 얻기(get)  
a.get('1') -->입력하면  
a 가 출력  

##### key가 딕셔너리 안에 있는지 조사하기(in)  
'1' in a  
True 가 출력됨  
3을 입력하면 false  


### 02-6 집합자료형  
set키워드를 통해 만들 수 있다.  
s1 = set([1,2,3])  
s1  
{1,2,3} 이 출력됨  


s2 = set("hello")  
s2  
{'e','h','l','o'} 가 출력됨  

중복을 허용하지 않는다  
순서가 없다 하지만 중복을 제거하기 위한 필터역할을 한다  


##### 교집합  
s1 & s2  

##### 합집합  
s1 | s2  

##### 차집합  
s1 - s2  

##### 추가, 업데이트, 삭제  
s1 = set([1, 2, 3])  

s1.add([4]) 추가한다  

s1.update([4,5,6])  값 여러개 업데이트   

s1.remove(2) 특정 값 제거  

### 02-7 불자료형    
bool이란 True와 False를 나타내는 자료형  

a = [1,2,3,4]  
while a:  
print (a.pop())  

while조건문 :  
수행할 문장  
a가 참인경우 a.pop()을 계속 실행한다  
리스트내에 요소가 없어질때까지 계속 꺼내고 출력한다  


#### 02-8 자료형의 값을 저장하는 공간, 변수  
변수명 = 변수에 저장할 값  

파이썬에서 변수는 객체를 가리키는 것으로도 볼수있다  
a = [1,2,3]  
이라고 입력하면 리스트자료형(객체)가 메모리에 자동으로 생성되고 변수a는 1,2,3 이라는 리스트가 저장된 메모리 주소를 가르키게 된다.  

a = [1,2,3]  
id(a)  
4203040510 처럼 리스트에 주소가 나온다  


3장 제어문
====

#### if문
"돈이 있으면 택시를 타고, 돈이 없으면 걸어간다"  

money = true  
if money :  
   Print("택시를 타자")  
   
   else :  
   print ("뚜벅이")  
   
  택시를 타자  
  
  
  if문의 기본구조  
  if 조건문 : 
   수행할 문장
   
   else:
   수행할 문장
   
#### 들여쓰기
파이썬에서는 들여쓰기가 중요하다

if 조건문:  
    수행할 문장1  
    수행할 문장2  
    수행할 문장3  
    
if 조건문:  
    수행할 문장1  
    수행할 문장2  
 수행할 문장3  
 (에러남) 
  
조건문 다음에는 콜론(:)을 반드시 사용한다  
문장의 끝이 콜론이 들어간다. 다른언어에서는 if문을 {}로 감싸지만, 파이썬에는 들여쓰기로 해결한다  


#### 조건문이란?

if조건문에서 "조건문"이란 참과 거짓을 판단하는 문장을 말한다  
money = True  ( 대소문자 구분해야함!)  
if money:  

>>> money = True  
>>> if money:  
...     print("Taxi TA")   



#### 비교연산자
x < y : x가 y보다 작다  
x > y : x가 y보다 크다  
x == y : x가 y랑 같다  
x != y : x가 y랑 같지않다  
x >= y : x가 y보다 크거나 같다  
x <= y : x가 y보다 작거나 같다  

#### and, or, not
x or y : x와 y둘중에 하나만 참이면 참이다  
x and y : x와 y모두 참이여야 참이다  
not x : x가 거짓이면 참이다  

>>> money = 2000 있다  
>>> card = True  
>>> if money >= 3000 or card:  
     print("택시타")  
     else:  
     print ("걸어가")  
     
     
#### x ins, x not in s

x in 리스트   x not in 리스트  
x in 튜플    x not in 튜플  
x in 문자열   x not in 문자열  

>>>1 in [1,2,3]    
True  

>>> 1 not in [1,2,3]  
False  

>>> 'a' in ('a','b','c')  
True  
     
>>> 'j' not in 'python'  
True  


>>> pocket = ['paper', 'Cellphone', 'money']  
if 'Cellphone' in pocket:  
       print("get phone_number")  
    else :  
       print("Solo")  

get phone_number!  


#### 다양한 조건을 판단하는 elif

"주머니에 돈이있으면 택시를 타고, 주머니에 돈은없지만 카드가 있으면 택시를 타고"  
"돈도없고 카드도 없으면 걸어가라"  

>>> pocket = ['card','cellphone', 'ring']
>>> card = True
>>> if 'money' in pocket:
      print("Taxi")      
    else :
        if card :
           print("taxi")
        else : 
             print("걸어가")
             
             
사실 위에를 현업에서는 많이 쓰는데

poket = ['paper','cellphone']
card = True
if 'money' in poket:
print("택시")
elif card:
print("택시)
else :
print("걸어가라")

elif는 제한없이 사용할 수있다

#### 조건부 표현식

message = "succes" if score => 60 else "failure"


#### While문

반복해서 문장을 수행해야 하는경우 while문을 사용한다.
while <조건문>:
 <수행할 문장1>
 <수행할 문장2>
 
참인 동안 계속 반복한다

열번찍어 안넘어가는 나무 없다

treehit = 0          변수초기화, 나무는 0부터 시작한다
while treehit < 10:    반복한다 트리힛을 10번까지
      treehit = treehit + 1    그리고 트리힛을 한번 돌때마다 1씩 추가한다 
      print ("나무를 %d번 찍었습니다." % treeHit)    프린트 1번(변수)를 찍는다
      if treeHit == 10:           만약 트리힛이 10인가? 1번이다. 다시 와일문으로, 트리힛이 10번인가 나무넘어갑니다 출력
           print ("나무 넘어갑니다")
           
           
           
>>> prompt = """ 프롬프트를 정의한다 아래처럼 프린트함
... 1. Add
... 2. Del
... 3. List
... 4. Quit
...
... Enter number: """
>>>


>>> number = 0      넘버는 0부터
>>> while number != 4:     넘버는 4까지
...     print(prompt)       앞에 정의한 프롬프트 를 호출
...     number = int(input())    넘버를 입력할 수있는 인풋 명령어
...

1. Add
2. Del
3. List
4. Quit

Enter number:

4를 입력하면 최종적으로 나가게 된다

#### while문 강제로 빠져나가기

>>> coffee = 10
>>> money = 300
>>> while money:
...     print("돈을 받았으니 커피를 줍니다.")
...     coffee = coffee -1
...     print("남은 커피의 양은 %d개입니다." % coffee)
...     if coffee == 0:        --> 반복문이 무한으로 도는 상황에서 커피가 0이라면 if를 쓰고 커피없다고하고 break 써서 탈출함
...         print("커피가 다 떨어졌습니다. 판매를 중지합니다.")
...         break
...


#### while 문 맨처음으로 
돌아가기
>>> a = 0   --> 0으로 초기화하고
>>> while a < 10:   --> while a가 10보다 작을 때
...     a = a + 1    --> a는 1 씩 증가하는데
...     if a % 2 == 0: continue    --> 만약, a의 나머지가 0이랑 같다면 컨티뉴, 다시 초기 while문으로 간다
...     print(a)
...


result = 0
a = 1
while a <1000 :
    if a % 3 == 0:
    result += a
    a +=1
    
 print(result)
 
 Aclass = [20,55,67,82,45,33,90,87,100,25]
 result = 0
 while Aclass:
        select = Aclass.pop()
        if select >= 50:
            result += select
            
 print(result)
 
 i= 0
 while True:
     i += 1  --> while 실행시 1씩증가
     if i > 10: break   i값이 10보다 크면 와일문 벗어난다
     print ('*' * i)     i값은 1씩증가할때 * 출력
     
     
#### for문

for문의 기본구조는 다음과 같음
for 변수 in 리스트(튜플, 문자열):
수행할 문장 1
수행할 문장 2


test_list = ['one','two','three']
for i in test_list:
     print(i)
     
one
two
three


a = [(1,2), (3,4), (5,6)]
for (first, last) in a:
     print(first +last)


#### for문의 응용

"총 5명의 학생이 시험을 보았는데 시험점수가 60점 넘으면 합격이고, 그렇지 않으면 불합격"
"합격인지 불합격인지 결과를 보여주시오

marks = [90, 25, 67, 45, 80]

number = 0
for mark in marks:  --> mark라는 변수에 marks의 리스트를 넣는다
    number  = number +1
    if mark >= 60:
       print("%d번의 학생은 합격이다" % number)
    else:
       print("%d번의 학생은 불합격이다" % number)

for문의 continue도 같다
다시 처음단계로 돌린다 이때 변수는 살아있다


#### for문과 range함수
자주 사용되는 경우가 많으며

a = range(10)
a
range (0, 10)
rainge(10)은 0부터 10미만의 숫자를 포함하는 range객체를 만들어준다

range(시작숫자, 끝숫자)
a = range(1,11)
a
range(1,11)


예제)
sum = 0
for i in range(1,11):
       sum = sum + i
print(sum)
55

1+2+3+4+5+6+7+8+9+10+11을 반복하면서 더해준다

marks = [90, 25, 67, 45, 80]
for number in range(len(marks)):

구구단 
for i in range(2,10):
    for j in range(1,10):
        print(i*j, end =" ")
    print('')
    
    
#### 리스트안에 for문 포함이 된다

a = [1,2,3,4]
result = [num * 3 for num in a]
print(result)

[3,6,9,12] 출력됨


#### 연습문제

sum = 0
for i in range(1,100):
       sum = sum + i
print(sum)



Aclass = [70, 60, 55, 75, 95, 90, 80, 80, 85, 100]
total =0
for score in Aclass:
     total += score
average = total / len(Aclass)
print(average)


number = [1,2,3,4,5]
result = [n*2 for n in numbers if n% 2==1]
result
[2,6,10]



함수
====

함수란 붕어빵 틀과 같다.
함수를 사용하는 이유는 반복적으로 사용되는 가치 있는 행위가 필요한 경우이다.

def 함수명(매개변수):
    <수행할 문장1>
    <수행할 문장2>
    ...

def add(a,b):
   return a + b

이 함수의 이름은 add이고 입력으로 a와 b 두개를 받고
결과값은 a와 b를 더하여 출력한다

def add(a,b): # a,b 는 매개변수
    return   a+b

print(add(3,4)) # 3,4는 인수

입력값 --> 함수 --> 리턴값

#### 일반적인 함수

def 함수이름(매개변수):
    <수행할 문장>
    ..
    return 결과값
    
def add(a,b):
   result = a + b
   return result
   
   
>>> a = add(3,4)
>>> print(a)
7

함수는 입력값이 없는 함수가 존재하고 문자열이 들어간다
결과값을 받을 변수 = 함수명()


>>> def add(a, b): 
...     print("%d, %d의 합은 %d입니다." % (a, b, a+b))
이 경우는 프린트문에 정의되었기때문에 리턴값은 없다

>>> result = add(a=3, b=7)  # a에 3, b에 7을 전달
>>> print(result)
10
매개변수 지정하여 호출할 수도 있다

#### 입력값 여러개일 경우

def 함수이름(*매개변수): 
    <수행할 문장>
    ...
    
def add_many(*args):
    result = 0
    for i in args:
        result = result + i
    return result
     
*args로 매개변수앞에 *를 붙이면 전부모아서 튜플로 만들어준다
args는 영어단어닌 arguments의 약자이며 관례적으로 사용한다


>>> result = add_many(1,2,3)
>>> print(result)
6
>>> result = add_many(1,2,3,4,5,6,7,8,9,10)
>>> print(result)
55

중복해서 쓸 수 있다

def add_mul(choice, *args):
    if choice == "add" :
       result = 0
    for i in args:
         result = result + i
    elif choice = "mul" :
         result = 1
         for i in args:
              result = result * i
         return result
         
         
 #### 함수의 결과값은 언제나 하나이다
 >>> def add_and_mul(a,b): 
...     return a+b, a*b

result = add_and_mul(3,4)

result = (7, 12)
즉 결과값을 튜플로 받는다

>>> def add_and_mul(a,b): 
...     return a+b 
...     return a*b  --> 이경우 없는 것이나 마찬가지다 리턴은 1개만 된다

return을 단독으로 써서 함수를 빠져나갈 수 있다


평균값 계산
def avg_value(*args):
    result = 0
    for i in args:
        result = result + i
    return result / len(args)
    
    
    
사용자 입력과 출력
====

사용자입력 -> 처리(프로그램,함수)-> 출력

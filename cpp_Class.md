# Class

클래스와 구조체는 겉으로 보기에 굉장히 닮았다. 참고로 구조체는 클래스의 일종이다.
>클래스
>>구조체

차이점이 있다면 클래스 내 선언한 함수가 아닌 영역에선 클래스 변수를 선언할 수 없다.
```c++
class Car
{
  char gamerID[CAR_CONST::ID_LEN];
  int fuelGauge;
  int curSpeed;

  void ShowCarState(){ }
  void Accel() { }
  void Break() { }
};

int main(void)
{
  Car run99 {"run99", 100, 0};    // 틀린문장이다
}
```

위 클래스변수를 run99 {"run99", 100, 0}; 으로 클래스 내에 선언된 함수가 아닌


다른 영역(여기선 main함수)에서 변수를 초기화 하는것은 불가능하다.

```c++
int main(void)
{
  Car run99;
}
```

우리는 이런 식으로 main함수에서 run99를 생성할 수 있는데 이를 **객체** 라 한다.

물론 객체 내의 변수를 초기화 하려면 클래스 내 함수에서 변수를 선언해야 한다.

## 접근제어 지시자의 종류
- public: 어디서든 접근허용
- protected: 상속관계에 놓여있을 때, 유도 클래스에서의 접근 허용
- private 클래스 내(클래스 내에 정의된 함수)에서만 접근허용

~~아직까지는 상속을 배우지 않아서, protected 설명생략~~

private 는 주로 클래스 내 멤버변수를 선언하는 영역이고

public 은 주로 클래스 내 멤버함수를 선언하는 영역이다.

## 클래스를 사용하는 이유

#### 1. 객체(Object)의 정리에 용이하다.

>게임을 만드는 툴인 유니티를 사용할 때를 생각해보면
>
> 스크립트를 만들면 항상 class 안에 템플릿이 주어진다. GameManager.C# 이라던지, BoardManager.C# 처럼 게임 전반을 아우르는 큰 스크립트도 존재하지만, 대부분 Object
하나에 스크립트 하나를 넣는다.
>
>예를 들어, enemy 하나를 만들면 그 enemy 안에 스크립트를 하나 넣어준다. 그 스크립트는 클래스로 이루어져있고, 멤버변수로 enemy의 걷기 속도, 달리기 속도 등을 지정할 수 있고,
멤버함수로는 player와 접촉 시 player의 HP를 1 감소시키거나, 끊임없이 어느 지점을 배회하게 만들 수 있다.

이렇게 클래스 하나에 객체(enemy)가 가져야 할 변수와 행해야 할 행동을 모아놓는다면, 보기에도 너무 편하다. 만일 객체가 오류가 난다면 다른 곳을 손본 필요 없이 그 객체의 클래스만 확인해주면 되기 때문이다. 이렇게 정리가 빠르고 한눈에 들어온다는 장점이 가장 크다.

#### 2. 정보 은닉
 프로그래머도 인간이기 때문에, 코드 삽입 중 실수를 할 수 있다. 변하면 안되는 값인데, 실수로 변수입력을 잘못해서 원하는 결과와 다른 결과를 이끌어낼 수도 있다.
 >예를 들면, 출금을 30,000원이라 적어야 하는데 실수로 300,000원 이라고 적어서 코드를 돌리면 전혀 예상못한 금액이 나올 수도 있다. 이 실수를 인지못한 개발자가 상용화시킨다면, 큰 손실을 초래하게 될 것이다.

 따라서 프로그래머의 실수에도 대처해야하기 때문에 만들어진 개념이며, 제한된 방법으로의 접근만 허용을 해서 잘못된 값이 저장되지 않도록 도와야 하고, 또 실수를 했을 때, 실수가 쉽게 발견되도록 해야 한다.

클래스 내 정보은닉으로 private 접근제어 지시자를 사용하는 것이 대표적인 예다.

#### 3. 캡슐화
경험 많은 객체지향 프로그래머를 구분하는 첫 번째 기준은 캡슐화이다. 캡슐화는 일관되게 적용할 수 있는 단순한 개념이 아니고, 구현하는 프로그램의 성격과 특성에 따라서 적용하는 범위가 달라지는, 흔히 하는 말로 **정답이란 딱히 없는 개념** 이기 때문이다. 순전히 개발자의 역량에 달려있는 파트이다.

>예를 들면, 드릴을 예로 들자.
>
>드릴로 콘크리트를 뚫을 수도 있고, 철판을 뚫을 수도 있다. 콘크리트용 드릴과 철판용 드릴을 따로 사야 할 필요가 있을까? 하나의 드릴에 그때 그때 상황에 맞는 날로 바꿔서 사용하면 여러모로 다양하게 사용할 수 있을 것이다.
>
>이것이 캡슐화하는 이유인데, 날을 하나의 객체(캡슐)로 본다면, 드릴을 새로 바꾸어도 날은 그대로 사용 가능하고, 반대로 하나의 드릴에 날만 교체하여 사용할 수도 있다. 캡슐화는 개발자 편리하게 사용하기 위해 만들어진 개념이다.
>
>참고자료: https://kin.naver.com/qna/detail.nhn?d1id=1&dirId=1040101&docId=115497254&qb=7KCV67O07J2A64uJ6rO8IOy6oeyKkO2ZlA==&enc=utf8&section=kin&rank=1&search_sort=0&spq=0&pid=T08pxspVuERssslgQ14sssssted-375468&sid=zYDQpBEjXCu3SIwfvWehyw%3D%3D

## 생성자(Constructor)와 소멸자(Destructor)
생성자는 흔히 클래스를 초기화하기 편하게 만들어준 기능이다.

클래스를 사용하여 객체 생성시 딱 한번 호출되는 특징을 가진다.
```C++
class classA
{
private:
  int a;
  char * name;

public:
  classA(int num, char * name) //클래스의 이름과 동일하다(classA)
    :a(num)                    //이 줄을 **멤버 이니셜라이저** 라고 부른다.
  {
    int len = strlen(name) + 1;
    this->name = new char[strlen(len)];
  }

  ~classA()
  {
    delete []name;
  }
}
```

위 코드에서 *classA(int num, char * name){}* 이란 함수를 __생성자__ 라고 부르고

*~classA(){}* 이란 함수를 __소멸자__ 라고 부른다.

또한 중간에 **this** 라는 표현을 찾을 수 있는데 객체 자신을 가르키는 용도로 사용한다.

변수의 이름을 정해주는것은 의외로 귀찮은 일인데, 매개변수와 멤버변수를 둘 다 name으로 받았지만, 멤버변수 name을 가르키는 용도로 this를 사용한 것을 코드로써 확인할 수 있다.

## 복사 생성자
생성자를 알았으니 복사 생성자는 비슷한 단어이므로 비슷한 개념이란 걸 유추할 수 있다.

```c++
class SoSimple{
private:
  //생략
public:
  SoSimple(int n1, int n2) : num1(n1), num2(n2) {}   //생성자

  SoSimple(SoSimple &copy) : num1(copy.num1), num2(copy.num2) {} //복사 생성자
};

int main(void)
{
  SoSimple sim1(15, 30);
  SoSimple sim2 = sim1; // (O) 가능, 복사생성자의 묵시적 호출
}
```
위에 코드에서 볼 수 있듯이 sim2라는 객체의 변수에 sim1라는 객체의 변수를 그대로 채워넣기위해 만들어진 함수가 복사생성자이다. 만일 위의 경우 따로 복사생성자를 만들어 주지 않아도 자동으로 디폴트 복사 생성자가 생긴다. 위의 경우는 **얕은 복사** 이다.

```c++
explicit  SoSimple(SoSimple &copy) : num1(copy.num1), num2(copy.num2) {}
```
위처럼 <u>explicit</u> 을 복사생성자 앞에 붙여주 **Sosimple sim2 = sim1;** 과 같은 복사생성자의 묵시적 호출을 막을 수 있으며, 필히 **Sosimple sim2(sim1)** 라고 적어줘야 한다.

하지만 아래와 같은 경우엔 **깊은 복사** 라 부른다.
```C++
class test
{
private:
  int a;
  char * name;

public:
  test(int num, char * name)
    :a(num)                   
  {
    int len = strlen(name) + 1;
    this->name = new char[strlen(len)];
  }
****************************************
*  test(const test& copy) : a(copy.a)
*  {
*    name = new char[strlen(copy.name) + 1];
*    strcpy(name, copy.name);
*  }
****************************************
};

int main(void)
{
  classA A(3, "taeyoon");
  classA B = A;
}
```

초기화를 할때 main 함수안에 클래스명 B는 사실상 복사가 되지 않는다. 그 이유는 classA생성자 안에 동적할당(new)를 진행하기 때문이다. 따라서, 우리는 별표로 가둔 함수처럼 복사 생성자를 만들어줘야한다. 이를 **깊은 복사** 라고 부른다.

#### Static 변수

>유니티로 게임을 만들 때 궁금했던점이 있었다. 여러 개의 같은 공을 튀긴다고 가정하자. 복사 된 5개의 공이 바닥에 닿을 때마다 스크립트에서 [num++] 식으로 올리고 싶었다. 하지만 5개의 공이 각자의 스크립트를 돌리는 중이라 num은 계속 1, 2, 3 식으로 올라가지 않고 그대로 0, 1 만 반복했다. 그 이유는 모든 공이 같은 스크립트를 공유하지만 각자 스스로 스크립트를 돌리는 중이라 각자 num변수를 난 한번튕겼어! 난 한번튕겼어! 했기 때문이다. 이때 질문을 통해 알았지만, 변수 선언 시, static int num = 0; 이라고 하면 각자가 같은 변수를 공유한다는 것을 알게되었다.

이처럼, static은
- **전역변수에 선언된 static** : 선언된 파일 내에서만 참조 혀용.
- **함수 내에 선언된 static** : 지역변수와 달리 함수를 빠져나가도 소멸되지 않음.

공통된 내용은 사라지지 않게 해준다는 점을 기억하자.


## 상속(Inheritance)
```c++
class Person
{
private:
  char * name;
  int age;     //사람의 이름과 나이를 받는다.
public:
  //생략
};

class univ_student : public Person  //상속
{
private:
  char * schoolname;   //Person객체의 정보를 상속으로 받아왔으며, 대학이름 추가
public:
  //생략
};
```

위와 같이 *univ_student* 라는 클래스 옆에 *: public Person* 이라고 다른 개체의 이름을 적어주는것을 ***상속*** 이라고 한다.

물론 public 이 아니고 protected 와 private 라고 쓰고 Person을 상속시켜도 되는데 거의 필요하지 않은 기능이므로 없다고 생각하는 것이 편하다.

또한 상속은 주로 IS_A 문법을 따르게 만드는게 기본 조건이다. 위의 스크립트를 예를 들면, "univ_student **is a** person" 이라고 할 수 있다. 그 때의 *is a* 를 가르키는 의미로 **IS_A문법** 이라고 한다.

1. Person 클래스를 **상위 클래스, 기초(base) 클래스, 부모 클래스** 라고 부르고,
2. univ_student 클래스를 **하위 클래스, 유도(derived)클래스, 자식 클래스** 라고 부른다.


 접근제어 지시자에서 protected의 설명을 상속을 배우기 전이어서 생략했는데, 지금 설명하자면 private과 public과 같은 의미로 사용된다. private는 클래스 내에서만 접근허용하고, public은 어디서든 접근 허용한다. protected 는 그 중간의 의미로 **유도 클래스에서의 접근을 허용한다.**
 >protected 안에 변수 int num1; 이 있다고 가정하자. num1은 평소에는 private 처럼 행동하며 왠만한 곳에선 접근을 불허하고 클래스 내에서만 접근 가능하다. 하지만 protected를 가진 클래스가 유도 클래스라면, 기초 클래스에서 protected 내의 변수 num1 을 불러내는것은 허용한다.

### Overriding vs Overloading

>유니티를 공부할 때 오버라이딩을 한번 경험해본 적이 있었다. 갈색 좀비를 하나 만들고 안에 스크립트와 콜라이더, 그리고 애니메이션을 넣었다. 그 좀비를 완벽히 만들곤, 녹색 좀비를 만들었다. 녹색 좀비를 갈색 좀비와 똑같이 만들고 싶었다. 물론 복사붙여넣기 해서 넣는것은 맞다. 하지만 애니메이션은 갈색 좀비와 녹색 좀비는 모델이 다르기 때문에 걷는 모션은 둘다 가졌다 해도 다르게 넣어줘야했다. 그때 달리기라는 애니메이션이 있다 라는 상황까지를 만들어주는 툴이 overriding이었다. 똑같은 기능을 각 캐릭터에 넣어줬다.

위에서 설명한 것처럼 다른 것 하나없이 완전히 똑같은 기능을 가진 형태를 또다시 만들어 주는것이 **overriding** 이었다. **overloading** 은 overriding과 굉장히 비슷하게 생겨서 헷갈리기 충분하여 다시 짚겠다. 오버로딩(overloading)은 주로 함수에서 쓰이며 함수 오버로딩이라 주로 부른다.

```c++
int MyFunc(int num)
{
  num++;
  return num;
}

int MyFunc(int a, int b) //오버로딩
{
  return a + b;
}

int main(void)
{
  MyFunc(20);
  MyFunc(30, 40);
  return 0;
}
```

위에서 함수 오버로딩이 사용되었는데, 같은 이름의 함수가 두개 사용되었다. C언어에서는 문제가 되어서 컴파일 실패하였지만, C++에서는 함수 오버로딩을 지원하기 때문에, 매개변수의 개수(인수의 개수 라고도 말할 수 있다.) 로 C++은 분류가 가능하다.

### 상속과 다형성
```c++
class First
{
  //생략
public:
  void MyFunc() {cont<<"first"<<endl; }
};

class Second : public First
{
  //생략
public:
  void MyFunc() {cont<<"second"<<endl; }
};

class Third : public Second
{
  //생략
public:
  void MyFunc() {cont<<"third"<<endl; }
};

int main(void)
{
	Second * temp = new Third;
	temp->MyFunc();
	return 0;
}
```

결과는? second 가 컴파일결과로 화면에 띄워진다.

나는 third클래스의 형태로 저장했고, second 클래스에 저장시켜준것 뿐인데 우리가 원하는 third가 아닌 second가 나왔다. 이유는 MyFunc이라는 함수가 세 개의 클래스 모두 오버라이딩 되어있기 때문.  컴파일러는 포인터의 자료형(__Second *__ temp)을 기준으로 판단하지, 실제 가리키는 객체의 자료형(new __third__)을 기준으로 판단하지 않는다. 구별하기 위해선 앞에 *virtual* 을 붙여주면 된다.
```c++
//생략
  virtual void MyFunc() {cont<<"first"<<endl; }
  //생략
  virtual void MyFunc() {cont<<"second"<<endl; }
  //생략
  virtual void MyFunc() {cont<<"third"<<endl; }
  //생략
```

이런식으로 작성되면
```c++
int main(void)
{
	Second * temp = new Third;
	temp->MyFunc();
	return 0;
}
```
일 때 결과는 third를 내보내게 된다.

실제 가리키는 객체의 자료형에 **오버라이딩 된 가상함수(Virtual Function)** 를 가져올 수 있다. 또한 이렇게 같은 이름의 함수를 여러 곳에 형성되는 성질을 가리켜 ***다형성(Polymorphism)*** 이라고 부른다. 

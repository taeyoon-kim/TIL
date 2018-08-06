# 상속
- Truck __is a__ Car.
- Notebook is __kind of__ computer.

이와 같은 'is a', 'kind of'같은 문법을 ***상속*** 이라고 한다.
```java
public class Bus extends Car {

}
```
extends라는 것 뒤에 붙는 클래스가 넘겨주는 클래스이다. Bus is a Car 이라고 이해해도 좋다.

Bus클래스는 Car의 메서드를 상속받을 수 있다. 하지만 반대로 Car클래스는 Bus클래스의 메서드를 상속 받을 순 없다.

부모가 가지고 있는 메소드외에 추가로 메소드를 선언하는 것을 확장하였다고 표현한다.
- - -
# 접근 제한자
> 클래스 내에서 멤버의 접근을 제한하는 역할

캡슐화 : 남에게 알려도 괜찮은 정보가 있는가 하면, 가족에게만 알려주고싶은 정보도 있고, 나만 알고싶은 정보도 있다. **이러한 관련된 내용을 모아서 가지고 있는 것을 캡슐화라고 함.**

## 접근지정자 종류
- public : 어떤 클래스는 접근 가능
- protected :  같은 패키지인 경우 접근 허용. 하지만, 다른 패키지라도 상속을 받은 경우 접근을 허용
- private : 자기 자신만 접근
- default : 아무것도 쓰지 않은 경우. 자기 자신과 같은 패키지 내에서 접근 허용

접근지정자 : public > protected > default > private
- - -
# 추상클래스
>비둘기, 짜장면___ 어떠한 이미지가 딱 떠오른다. 누구한테나 물어봐도 비슷한 그림을 상상할 수 있다. 하지만, 새, 음식____ 어떤 이미지가 떠오를까? 뭔진 알겠는데 구체적인 구현은 모두 다르다.

이렇게 모호한 단어들을 가진 클래스들은 부모로서의 역할은 수행할 수 있지만, 객체로의 구현은 불가능하다. 객체가 될 수 있는 클래스는 구체적이어야만 한다.
```java
public abstract class Bird {

	public abstract void sing();

	public void fly() {
		System.out.println("날다");
	}
}
```

Bird라는 클래스에 abstract라는 단어가 붙여져있다. 추상적이라는 의미인데 클래스 내에 추상 메서드가 단 하나라도 존재한다면 클래스는 추상클래스로 바뀌어야한다. <u>위에서 sing메서드를 abstract시켰기 때문에 클래스도 abstract시킨 것을 확인할 수 있다.</u>

또한 추상클래스에서는 일반 클래스처럼 일반적인 메서드도 사용 가능하다. <u>위에서 fly메서드를 일반적인 메서드 형식으로 만든 것을 확인할 수 있다.</u>
```java
public class Duck extends Bird {

	@Override //선언만 시켜놓은 메서드 자동으로 튀어나옴
	public void sing() {
		System.out.println("꽥꽥");
	}
}
```
추상클래스를 부모로 이용한 Duck이라는 자식 클래스를 확인할 수 있다. 추상클래스에서 만들어준 추상 메서드는 자식에서 한번 더 작성해줘야 한다.
```java
public class DuckExam {
	public static void main(String[] args) {
		Duck duck = new Duck();
		duck.sing();
		duck.fly();

		//Bird b = new Bird(); //컴파일 에러
	}
}
```
추상클래스를 상속받은 클래스의 객체 생성과 그 객체로서의 매서드 사용은 이때까지 해온 일반적인 사용법과 다르지 않다. 또한 추상클래스를 이용한 객체 생성은 불가능하다.
- - -
# super와 부모생성자

- this : 나를 가리키는 키워드
- super : 부모를 기리키는 키워드

따라서 super();는 부모 생성자를 부르는 코드이다.
- - -
# 오버라이딩

- 부모가 가진 메서드와 똑같은 모양의 메서드를 자식이 가지고 있는 것을 이야기함
- 메서드를 재정의함
>Overriding : 올라타다

부모 클래스에도 run메소드를 정의하고, 자식 클래스에도 완벽히 똑같은 모양의 run메소드를 정의한다. 그 후 다른 클래스에서 자식 클래스를 이용하여 객체를 생성하고 run을 부르면 자식 클래스의 run만 부르게 된다. 부모가 만든 메소드 위에 자식 클래스가 그대로 올라타는 그림을 연상하자.

만일 부모 클래스의 run메소드를 부르고 싶다면, ```super.run();```이라고 적는다.
- - -
# 클래스 형변환
우리는 bus 가 car의 일종이라고 안다. bus가 자식클래스라면 car는 부모클래스이다. 우린 버스를 보고 "버스다" 라고 할 수도 있지만, "차다"라고도 할 수 있다.

버스객체를 Car 타입의 참조변수로 참조할 수 있다. 부모타입으로 자식객체를 참조하게되면 부모가 가지고잇는 메스드만 사용할 수 있다.

부모타입으로 자식을 가리킬 수 있다. 이 경우 부모가 가지고 있는 내용만 사용 가능함.

```java
public class Car {
	public void run() {
		System.out.println("car달려");
	}

  public void yoyo() {
    System.out.println("yoyo");
  }
}
```

```java
public class Truck extends Car {
	public void ppangppang() {
		System.out.println("빵빵");
	}
	public void run() {
		System.out.println("트럭run");
	}
}
```
Car은 부모, Truck은 자식이며 run이 오버라이딩 됨을 알 수 있다.

```java
public class TruckExam {

	public static void main(String[] args) {
		Car c = new Truck(); //부모가 자식을 가리킬 수 있다.
		c.run();
//	c.ppangppang();
    c.yoyo();

		Truck truck = (Truck)c; // c는 car타입인데? bus는 못받아요
		truck.run();
		truck.ppangppang();
	}
}
```

```Car c = new Truck();```에서 보이듯이 Truck형으로 만든 객체를 Car라는 참조 타입으로 받을 수 있다. 다른 말로는, 부모가 자식을 가리킬 수 있다.

부모타입으로 자식객체를 참조하게 되면 부모가 가지고 있는 메소드만 사용 가능하다. run은 부모와 자식 둘 다 가지고 있는 오버라이딩이므로 사용 가능하며, ppangppang은 자식만 가지고 있는 메소드이므로 사용할 수 없다. 부모만 가지고 있는 메소드인 yoyo도 사용 가능하다. __부모가 가진 메소드만이 사용 가능함을 알자.__ 물론 위에서 오버라이딩 된 run은 자식의 메소드가 실행된다.

객체들 끼리의 형변환이 가능한데, 단 상속관계에 있었을 때만 가능하다.

마지막으로 부모타입의 객체를 자식타입으로 참조하게 할때는 명시적으로 형변환 해주어 한다. 단 이렇게 형변환 할때에는 부모가 참조하는 인스턴스가 형변환 하려는 자식타입일 때만 가능하다. _말이 어려우니 코드로 설명하겠다._
```java
public static void main(String[] args) {
      Car c = new Truck();
      Truck truck = (Truck)c; //가능
```
위는 객체 생성 시, 자식클래스로 만들어진 객체를 부모클래스 타입으로 받았다. 이 때는 만들어진 인스턴스 c는 Truck으로 형변환 하는것이 가능하다.
```java
public static void main(String[] args) {
      Car car = new Car();
      //Truck truck = (Truck)car;  //컴파일 에러, 불가능
```
하지만 위의 코드는, 부모클래스로 만든 객체를 부모클래스 타입으로 받았다. 우리가 봤던 가장 일반적인 객체 생성이다. 이 때는 만들어진 인스턴스 car는 Truck으로 형변환하는것이 불가능하다.
- - -
# 인터페이스 만들기
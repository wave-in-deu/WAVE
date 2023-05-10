
1일차 스터디 
자바는 '한번 작성하면 어디서든 실행된다'는 목표를 가지고 만들어진 언어
대문자 소문자 구분을 한다
Hello World라는 프로그램(=애플리케이션)을 구현하기 위해
public class HelloWorldApp{
	public static void main(String args[]) {
		System.out.println("Hello World!!");
	}
}
위와 같은 소스(=코드,언어)를 만들었다.

결과는 Hello World!!

자바의 동작원리
Java Source code. java -> Compile -> Java Application.class -> Run -> Java Virtual Machine -> Run -> computer
사람이 이해할 수 있는 자바 코드를 작성 하고 컴파일 과정을 거치면 class파일로 변경되고 이를 Java Virtual Machine이 읽어서 컴퓨터에서 실행된다.

데스크탑 애플리케이션 만들기

import javax.swing.*;   
import java.awt.Dimension;
import java.awt.Toolkit;
public class HelloWorldGUIApp{
    public static void main(String[] args){
        javax.swing.SwingUtilities.invokeLater(new Runnable() {
            public void run() {
                JFrame frame = new JFrame("HelloWorld GUI");
                frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
                frame.setPreferredSize(new Dimension(800, 300));
                JLabel label = new JLabel("Hello World!!", SwingConstants.RIGHT);
                frame.getContentPane().add(label);
                Dimension dim = Toolkit.getDefaultToolkit().getScreenSize();
                frame.setLocation(dim.width/2-400/2, dim.height/2-300/2);

                frame.pack();
                frame.setVisible(true);
            }
        });
    }
}

소스를 통해 Hello World 글자 위치와 창의 너비를 바꿀 수 있었다. 

안드로이드 애플리케이션 만들기

import com.pi4j.io.gpio.GpioController;
import com.pi4j.io.gpio.GpioFactory;
import com.pi4j.io.gpio.GpioPinDigitalOutput;
import com.pi4j.io.gpio.PinState;
import com.pi4j.io.gpio.RaspiPin;

public class HelloWorldRaspberryPi {

	public static void main(String[] args) throws InterruptedException {

		final GpioController gpio = GpioFactory.getInstance();
		final GpioPinDigitalOutput pin = gpio.provisionDigitalOutputPin(RaspiPin.GPIO_01, "PinLED", PinState.LOW);
		final int SHORT_INTERVAL = 200;
		final int LONG_INTERVAL = SHORT_INTERVAL * 3;
		final int LETTER_INTERVAL = SHORT_INTERVAL * 7;

		while (true) {
			// H
			pin.high();
			Thread.sleep(SHORT_INTERVAL);
			pin.low();
			Thread.sleep(SHORT_INTERVAL);
			pin.high();
			Thread.sleep(SHORT_INTERVAL);
			pin.low();
			Thread.sleep(SHORT_INTERVAL);
			pin.high();
			Thread.sleep(SHORT_INTERVAL);
			pin.low();
			Thread.sleep(SHORT_INTERVAL);
			pin.high();
			Thread.sleep(SHORT_INTERVAL);
			pin.low();
			Thread.sleep(LETTER_INTERVAL);

			// e
			pin.high();
			Thread.sleep(SHORT_INTERVAL);
			pin.low();
			Thread.sleep(LETTER_INTERVAL);

			// l
			pin.high();
			Thread.sleep(SHORT_INTERVAL);
			pin.low();
			Thread.sleep(SHORT_INTERVAL);

			pin.high();
			Thread.sleep(LONG_INTERVAL);
			pin.low();
			Thread.sleep(SHORT_INTERVAL);

			pin.high();
			Thread.sleep(SHORT_INTERVAL);
			pin.low();
			Thread.sleep(SHORT_INTERVAL);
			pin.high();
			Thread.sleep(SHORT_INTERVAL);
			pin.low();
			Thread.sleep(LONG_INTERVAL);

			// l
			pin.high();
			Thread.sleep(SHORT_INTERVAL);
			pin.low();
			Thread.sleep(SHORT_INTERVAL);

			pin.high();
			Thread.sleep(LONG_INTERVAL);
			pin.low();
			Thread.sleep(SHORT_INTERVAL);

			pin.high();
			Thread.sleep(SHORT_INTERVAL);
			pin.low();
			Thread.sleep(SHORT_INTERVAL);
			pin.high();
			Thread.sleep(SHORT_INTERVAL);
			pin.low();
			Thread.sleep(LONG_INTERVAL);
		}
	}
}

소스를 통해 LED 전구가 깜빡거리며 모스부호대로 HELL을 점멸하였다.

2일차

라즈베리파이 커널에서는 
javac  -cp ".:/opt/pi4j/lib/*" HelloWorldRaspberryPi.java ; java  -cp ".:/opt/pi4j/lib/*" HelloWorldRaspberryPi
이 소스 한줄로 똑같은 결과를 내었다..

편리한 기능
sout 컨트롤+스페이스 = System.out.println();

자바에서 숫자를 그냥 표현 

// 뒤에 있는 코드를 자바는 없는 셈 = 주석
숫자-Number
문자열-String

public class Datatype{
	public static void main(String[] args) {
		System.out.println(6); // Number
		System.out.println("six"); // String
		System.out.println("6"); // String 6
		
		System.out.println(6+6); // 12
		System.out.println("6"+"6"); // 66
		
		System.out.println(6*6); // 36
		//System.out.println("6"*"6"); error
		
		System.out.println("1111".length());
		//System.out.println(1111.length()); error
	}
}

결과 : 6
six
6
12
66
36
4

Description	Resource	Path	Location	Type The project cannot be built until build path errors are resolved	HelloWorld		Unknown	Java Problem
editor does no contain a main type
java.lang.ClassNotFoundException
어제부터 뜬 에러들인데 전부
Project-properties-java build path-전부 jdk20으로 호환시켜주면 됨

타입별로 연산방법이 존재


New-class-Name+public static void main(String[] args)체크 
연산자 = Operator
Math (캐비넷)안에 수학과 관련된 명령어 기능

public class Number {

	public static void main(String[] args) {
		// Operator
		System.out.println(6 + 2); //8
		System.out.println(6 - 2); //4
		System.out.println(6 * 2); //12
		System.out.println(6 / 2); //3
		
		System.out.println(Math.PI); //3.141592653589793
		System.out.println(Math.floor(Math.PI)); //3.0 내림
		System.out.println(Math.ceil(Math.PI)); //4.0 올림
		System.out.println(Math.round(Math.PI)); //3 반올림
		System.out.println(Math.abs(-5)); //인수의 절대값 반환
		System.out.println(Math.pow(3, 4)); //거듭 제곱 (3에 4승)
		System.out.println(Math.random()); //0.0~1.0 사이의 실수를 랜덤 생성하여 반환

	}

}

결과 : 8
4
12
3
3.141592653589793
3.0
4.0
3
5
81.0
0.302652439921948 <-랜덤값


public class StringApp {

	public static void main(String[] args) {
		
		System.out.println("Hello World"); //String 문자열 문자가 모인
		
		System.out.println('Hello World'); //Character 문자 한글자만 에러
		
		System.out.println("H"); //이건 가능은 함
		
		System.out.println("Hello " //이클립스가 자동으로 연결
				+ "World");
		
		System.out.println("Hello \nWorld"); // \n은 new line의 약자 (역슬레시 n) 줄바꿈
		
		System.out.println("Hello \"World\""); // escape Hello "World" //특정

	}

}

결과 : H
Hello World
Hello 
World
Hello "World"


public class StringOpreration {

	public static void main(String[] args) {
		
		System.out.println("Hello World".length()); //11
		System.out.println("Hello, leezche ... bye.".replace("leezche", "egoing")); //대체
		
	}

}

결과 : 11
Hello, egoing ... bye.

3일차


public class Variable {

	public static void main(String[] args) {
		
		int a = 1; // Number -> integer 정수 
		System.out.println(a); // 1
		
		double b = 1.1; //real number -> double 실수
		System.out.println(b); // 1.1
		
		String c = "Hello World";
		System.out.println(c); // Hello World

	}

}

1
1.1
Hello World


public class Letter {

	public static void main(String[] args) {
		System.out.println("Hello, egoing ... egoing ... egoing ... bye");
		String name = "egoing";
		System.out.println("Hello, "+name+" ... "+name+" ... egoing ... bye");
		
		double VAT = 10.0;
		System.out.println(VAT);
		

	}

}

결과 : Hello, egoing ... egoing ... egoing ... bye
Hello, egoing ... egoing ... egoing ... bye
10.0


public class Casting {

	public static void main(String[] args) {
		
		double a = 1.1;
		double b = 1;
		double b2 = (double) 1; // 손실 없으므로 같음
		
		System.out.println(b);
		
//		int c = 1.1;
		double d = 1.1;
		int e = (int) 1.1;
		System.out.println(e); // 1.1 -> 1.0 손실
		
		// 1 to String
		String f = Integer.toString(1);
		System.out.println(f.getClass());

	}

}

결과 : 1.0
1
class java.lang.String


public class Program {

	public static void main(String[] args) {
		
		System.out.println(1);
		System.out.println(2);
		System.out.println(3);

	}

}

import org.opentutorials.iot.Elevator;
import org.opentutorials.iot.Lighting;
import org.opentutorials.iot.Security;

public class OkJavaGoInHome {

	public static void main(String[] args) {
		
		String id = "JAVA APT 507";
		// Elevator call
		Elevator myElevator = new Elevator("id");
		myElevator.callForUp(1);
		
		// Security off
		Security mySecurity = new Security("id");
		mySecurity.off();
		
		// Light on
		Lighting hallLamp = new Lighting("id+ / Hall Lamp");
		hallLamp.on();
		Lighting floorLamp = new Lighting("id+ / floor Lamp");
		floorLamp.on();

	}

}

디버거 기능
브레이크 포인트까지 실행
Step Over  다움 줄에 브레이크 포인트 생성
Resume 다음 브레이크 포인트까지 실행 더이상 없다면 끝까지 실행
우측 Variable 탭에서 변수 확인

4일차
 argument는 사용자 입력을 의미하는 문자열배열
parameter는 함수에서 전달되어 사용되어지는 변수
argument는 main()함수의 매개변수로 작용한다.
args는 문자열 배열(array)로 여러 개의 String 데이터가 들어있을 수 있다.
인덱스를 통해 배열의 데이터를 꺼내 쓸 수 있고, 인덱스는 0번부터 시작
자바 파일 컴파일하기
기존에 있던 class 파일을 지우고 javac Program.java를 컴파일
실행하기 
java Program

# 5일차
====================================================================
## c13 자바 문서 보는 법
--------------------------------------------------------------------
자바 API(Application Programming Interface) = 자바의 도구들을 응용해서 사용하기 위해서 일정한 조작 장치를 구성
사용자가 자바 프로그램을 사용할 수 있도록 만들어둔 장치 = UI(User Interface)
패키지>연관된 클래스>연관된 변수, 메소드
인스턴스는 클래스를 컴퓨터 상에서 실체화한 것
클래스의 상속관계
자식에 해당하는 클래스는 부모에 해당하는 클래스의 모든 변수와 메소드를 사용할 수 있다.

## c14.4까지 나의 앱만들기
--------------------------------------------------------------------
public class AccoutingApp {

	public static void main(String[] args) {
		
		System.out.println("Value of supply : "+12345.0);
		System.out.println("VAT : "+ (12345.0*0.1));
		System.out.println("Total : "+ (12345.0+ 12345.0*0.1));
		System.out.println("Expense : "+ (12345.0*0.3));
		System.out.println("Income : "+ (12345.0 - 12345.0*0.3));
		System.out.println("Dividend 1 : "+ (12345.0 - 12345.0*0.3) * 0.5 );
		System.out.println("Dividend 2 : "+ (12345.0 - 12345.0*0.3) * 0.3 );
		System.out.println("Dividend 3 : "+ (12345.0 - 12345.0*0.3) * 0.2 );
		
	}

}

Find/Replace로 선택한 값 모두 대체 
**단축키 ctrl + f**

변수 적용하기 우클릭+Refactor+Extract Local Variable 변수 지정
**단축키 alt + shift + L**

---------------------------------------------------------
public class AccoutingApp {

	public static void main(String[] args) {
		
		double ValueOfSupply = 10000.0;
		double vatRate = 0.1;
		double vat = ValueOfSupply*vatRate;
		double total = ValueOfSupply+ vat;
		double expenseRate = 0.3;
		double expense = ValueOfSupply*expenseRate;
		double income = ValueOfSupply - expense;
		double dividend1 = income * 0.5;
		double dividend2 = income * 0.3;
		double dividend3 = income * 0.2;
		
		System.out.println("Value of supply : "+ValueOfSupply);
		System.out.println("VAT : "+ vat);
		System.out.println("Total : "+ total);
		System.out.println("Expense : "+ expense);
		System.out.println("Income : "+ income);
		System.out.println("Dividend 1 : "+ dividend1 );
		System.out.println("Dividend 2 : "+ dividend2 );
		System.out.println("Dividend 3 : "+ dividend3 );
		
	}

}
**프로그램의 기능은 바꾸지 않으면서 이해하기 쉽게 바꾸는 과정을 리팩토링**

아규먼트를 받는 프로그램으로 수정하기

public class AccountingApp {

	public static void main(String[] args) {
		
		double ValueOfSupply = Double.parseDouble(args[0]);
		double vatRate = 0.1;
		double vat = ValueOfSupply*vatRate;
		double total = ValueOfSupply+ vat;
		double expenseRate = 0.3;
		double expense = ValueOfSupply*expenseRate;
		double income = ValueOfSupply - expense;
		double dividend1 = income * 0.5;
		double dividend2 = income * 0.3;
		double dividend3 = income * 0.2;
		
		System.out.println("Value of supply : "+ValueOfSupply);
		System.out.println("VAT : "+ vat);
		System.out.println("Total : "+ total);
		System.out.println("Expense : "+ expense);
		System.out.println("Income : "+ income);
		System.out.println("Dividend 1 : "+ dividend1 );
		System.out.println("Dividend 2 : "+ dividend2 );
		System.out.println("Dividend 3 : "+ dividend3 );
		
	}

}

문자열을 실수형으로 바꾼다는 코드 **Double.parseDouble**

터미널에서 실행하기
Properties -> Location 복사 -> 터미널(cmd)에서 cd+주소 ->
javac AccountingApp.java javac 명령어로 컴파일 -> java AccountingApp 33333.0 java 명령어로 AccountingApp 실행 아규먼트로 원하는 공급가액 입력

*사소한 실수*
터미널 실행하면서 에러가 떳는데 알고보니 파일명에서 n을 빼먹어서 발생했다.
자바 파일을 우클릭하고 rename으로 이름을 다시 바꾸고 소스도 바꿔주니 정상적으로 작동하였다.


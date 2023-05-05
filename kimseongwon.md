
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

Description	Resource	Path	Location	Type The project cannot be built until build path errors are resolved	HelloWorld		Unknown	Java Problem
editor does no contain a main type
java.lang.ClassNotFoundException
어제부터 뜬 에러들인데 전부
Project-properties-java build path-전부 jdk20으로 호환시켜주면 됨

타입별로 연산방법이 존재
//변수의 정의, 정 int에서는 정수가 
public class variable {

    public static void main(String[] args) {

      int a=1; // number -> integer ... -2, -1, 0, 1, 2 ... 정수 데이터 integer를 이용해서 정수 표현
      System.out.println(a);
      double b=1.1; // real number -> double = (실수값이 올수있다) ... -2.0, -1.0, 0, 1.0, 2.0 ...
      System.out.println(b);
      String c = "Hello World"; // 문자열 데이터 string 선언
      System.out.println(c);                          
    }
}
// 변수의 효용 //
public class letter{

    public static void main(String[] args){
        String name = "leezche"; // name이라는 변수를 지정해주면, 자주 사용하는 데이터를 여러번 재사용 가능(변수의 재사용)
        System.out.println("Hello, "+name+"..."+name+" ... egoing ... bye");

        double VAT = 10.0; // VAT(부가가치세)라는 이름을 붙이게 되면, 단순히 실수 10이 아닌 '부가가치세'라는 의미, 코드의 의미를 쉽게 파악
        System.out.println(VAT); // 코드의 가독성
    }
}
//데이터 타입의 변환
public class Casting {

    public static void main(String[] args) {
//정수와 실수 간에 변환하기
        double a = 1.1; //명시적으로 데이터 타입 변환을 나타내야됨
        double b = 1;
        double b2 = (double) 1;
        System.out.println(b);

//      int c = 1.1;
        double d = 1.1; //실수 1.1에서 정수로 변환할려면 데이터 타입을 명시적으로 변경해 주어야 함.
        int e = (int) 1.1;
        System.out.println(e);

        //1 to string
        String f = Integer.toString(1); //정수를 문자열로 변환 , integer 객체의 toString를 이용하면 숫자를 문자열로 변환 가능 
        System.out.println(f.getClass());
    }
}
//프로그래밍이란 무엇인가 ?
//프로그램 = 순서를 나타내는 것 , 컴퓨터 프로그래밍으로 사람이 잘 못하는 일을 기계에서 위임하여 자동화할 수 있다.
public class Program{

    public static void main(sting[] args){

        System.out.println(1);
        System.out.println(2);
        System.out.println(3);
    }
}
//프로그램 만들기 - IoT 라이브러리 만들기 , IoT 프로그램 만들기
//import 구문을 이용해서 org.opentutorials.Elevator를 입력해야 되는 구문을 Elevator로 단순하게 할 수 있다!
import  org.opentutorials.iot.Elevator;
import org.opentutorials.iot.Lighting;
import org.opentutorials.iot.Security;

public class OKjavaGoInHome {

    public static void main(String[]args){
        String id = "JAVA APT 507"; // 반복적으로 사용되는 값의 경우는 변수로 지정하여 재사용함(코드의 가독성 높임)

        // Elevator call
        Elevator myElevator = new Elevator(id);
        myElevator.callForUp(1);
        // Security off
        Security mySecurity = new Security(id);
        mySecurity.off();
        // Light on
        Lighting hallLamp = new Lighting(id+" / Hall Lamp");
        hallLamp.on();
         
        Lighting floorLamp = new Lighting(id+" / floorLamp");
        floorLamp.on();

    }
}
//디버거
//본인의 코드를 분석하고 싶을 때 이용하는 것 : 디버거
//브레이크 포인트

//입력과 출력 1,2 - arguments & parameter
import javax.swing.JOptionPane; // JOptionpane 객체의 showInputDialog 메소드를 이용하면 id 값을 입력 가능하다.

import org.opentutorials.iot.DimmingLights;
import org.opentutorials.iot.Elevator;
import org.opentutorials.iot.Lighting;
import org.opentutorials.iot.Security;
public class OKjavaGoInHomeInput {

    public static void main(String[]args){
        String id = JOptionPane.showInputDialog("Enter a ID");
        string bright = JOptionPane.showInputDialog("Enter a Bright level"); //밝기 값 입력
        // Elevator call
        Elevator myElevator = new Elevator(id);
        myElevator.callForUp(1);
        // Security off
        Security mySecurity = new Security(id);
        mySecurity.off();
        // Light on
        Lighting hallLamp = new Lighting(id+" / Hall Lamp");
        hallLamp.on();
         
        Lighting floorLamp = new Lighting(id+" / floorLamp");
        floorLamp.on();

        DimmingLights moodLamp = new DimmingLights(id+"moodLamp"); 
        moodLamp.setbright(Double.parseDouble(bright)); //setbright 메소트의 밝기는 double 데이터로 타입 변환을 해야됨.
        moodLamp.on();

        DimmingLights moodLamp = new DimmingLights(id+" moodLamp");
        moodLamp.setBright(10);
        moodLamp.on(); // 밝기 10으로 조절한 것
    }
}

input -> program -> output == 입력정보를 받아서 출력을 하는 것!

import javax.swing.JOptionPane; // JOptionpane 객체의 showInputDialog 메소드를 이용하면 id 값을 입력 가능하다.

import org.opentutorials.iot.DimmingLights;
import org.opentutorials.iot.Elevator;
import org.opentutorials.iot.Lighting;
import org.opentutorials.iot.Security;
public class OKjavaGoInHomeInput {
//parameter, 매개변수
    public static void main(String[]args){
        String id = args[0];
        String bright = args[1];
        // args parameter는 argument의 값을 받아서 동작, 인덱스를 통해 배열의 데이터를 꺼내 쓸수 있고, 인덱스는 0번부터 시작 ! //
        // Elevator call
        Elevator myElevator = new Elevator(id);
        myElevator.callForUp(1);
        // Security off
        Security mySecurity = new Security(id);
        mySecurity.off();
        // Light on
        Lighting hallLamp = new Lighting(id+" / Hall Lamp");
        hallLamp.on();
         
        Lighting floorLamp = new Lighting(id+" / floorLamp");
        floorLamp.on();

        DimmingLights moodLamp = new DimmingLights(id+"moodLamp"); 
        moodLamp.setbright(Double.parseDouble(bright)); 
        moodLamp.on();

        DimmingLights moodLamp = new DimmingLights(id+" moodLamp");
        moodLamp.setBright(10);
        moodLamp.on(); 
    }
}
//argument를 입력받아 프로그램 실행시키기
main 메소드의 args 파라미터를 이용하여 입력값을 받는 방법이 있다.

// 직접 컴파일 - 실행
'이클립스는 자바로 프로그램을 만들기 위해 유용한 도구'
이클립스 없이 자바로 프로그래밍을 하려면 우선 자바 파일을 스스로 컴파일할 수 있어야 한다.
그리고 컴파일한 클래스 파일을 실행하는 과정을 거쳐야 한다.
Compile , Run , Input

// 직접 컴파일 - 실행 - 실행환경 살펴보기
// 터미널 열기 //
window : 윈도우 키 + R로 실행 창을 키고, cmd를 입력하여 명령 프롬프트를 실행한다.
MacOS: 스포트라이트에서 terminal을 입력해서 터미널을 실행한다.

// javac 확인 //
터미널에 javac를 입력하고 실행하면 javac 명령어의 사용 방법이 출력된다.
//Windows 자바 확인
자바의 설치 경로(ex: C:\Program files\java\jdk-14.0.1)\bin\javac.exe
// 환경 변수 경로 //
내 pc 오른쪽 클릭 -> 속성 클릭 => 고급 시스템 설정 클릭 -> 환경 변수 클릭 -> path 더블클릭해서 수정 가능

// 직접 컴파일 - 실행 - 컴파일과 실행하기
cd 명령어를 통해 프로젝트 디렉토리로 이동한다.
// 자바 파일 컴파일하기 // 
터미널에 javac를 입력하면 javac 명령어의 사용 방법을 보여준다.
javac Program.java
입력하면 Program.class가 생성된 것을 확인할 수 있다.
javac -cp "." Program.java
(에러가 난다면 위의 코드로 해보기)
// 실행하기 //
java 명령어 이용해서 입력
java Program
(에러가 난다면 아래의 코드로 해보기)
java -cp "." Program

이렇게 해서 파일을 컴파일해서 실행까지 해보는 시간이였다.

//직접 컴파일 - 실행 - 라이브러리이용
//라이브러리를 이용하는 프로그램을 컴파일하기

// OKjavaGoInHome.java 파일 컴파일
import org.opentutorials.iot.Elevator;
import org.opentutorials.iot.Lighting;
import org.opentutorials.iot.Security;
 
public class OkJavaGoInHome {
 
    public static void main(String[] args) {
         
        ....
    }
 
}
//외부 라이브러리도 포함해서 컴파일하기 위해서는 javac 명령어의 옵션 중 --class-path(-cp) 옵션을 이용해서 외부 라이브러리도 함께 지정해야 한다.//
javac -cp ".;lib" OkJavaGoInHome.java 로 입력
macOS나 Linux의 경우에는 ".;lib" 부분의 세미콜론(;)을 콜론(:)으로 바꿔서 입력한다.
콜론(:)이나 세미콜론(;)은 구분자의 의미를 가진다.
//외부 라이브러리의 클래스들도 함께 사용하는 프로그램을 실행하기 위해서는
컴파일했을 때와 마찬가지로 --class-path 옵션에 외부 라이브러리도 포함해서 실행해야 한다.//
//윈도우
java -cp ".;lib" OkJavaGoInHome 로 입력

// 직접 컴파일-실행 - 입력과 출력
// OKjavaGoInHomeInput.java 파일 컴파일
import org.opentutorials.iot.DimmingLights;
import org.opentutorials.iot.Elevator;
import org.opentutorials.iot.Lighting;
import org.opentutorials.iot.Security;
 
public class OkJavaGoInHomeInput {
 
    public static void main(String[] args) {
         
        String id = args[0];
        String bright = args[1];
        
        ....
 
    }
 
}
실행할 때 argument 입력
org.opentutorials.iot 패키지는 다시 lib 폴더 밖으로 꺼낸다.
터미널에서 argument 주기
- 실행할 클래스 파일 이름 다음에 연달아서 입력 -
java OkJavaGoInHomeInput "JAVA APT 507" 15.0

자바 문서 보는 법 - API VS UI//
------------------------------------------
API: 사용자가 직접 사용하는 것
UI: 사용자가 자바 프로그램을 이용할 수 있도록 만들어 놓은 것

자바 문서 보는 법 - 패키지, 클래스, 변수, 메소드//
---------------------------------------------------------------
클래스 : 서로 연관된 변수와 메소드로 모아서 이름을 붙히는 것 
패키지 : 연관된 클래스를 묶어서 정리한 것 
자바 문서 보는 법 - 클래스
------------------------------------------
클래스 ? 서로 연관된 변수와 메소드로 모아서 이름을 붙히는 것
public class OKjavaGoInHome {

    public static void main(String[]args){ // Math 클래스 : 수학과 관련된 여러 변수들과 메소드들이 있다.

        System.out.println(Math.PI); // PI: 원주율이 적절한 정밀도로 저장되어 있는 변수
        System.out.println(Math.floor(1.6)); // floor 메소드: 특정 소수점 이하에 대하여 버림한 값 산출
        System.out.println(Math.ceil(1.6)); // ceil 메소드: 특정 소수점 이하에 대하여 올림한 값 산출
    }

}

//자바 문서 보는 법 - 인스턴스
------------------------------------
인스턴스 ? 클래스를 컴퓨터 상에서 실체화한 것
import java.io.FileNotFoundException;
import java.io.IOException;
import java.io.PrintWriter;
public class InstanceApp {
 
    public static void main(String[] args) throws IOException{
         
        PrintWriter p1 = new PrintWriter("result1.txt");
        p1.write("Hello 1");
        p1.close();
         
        PrintWriter p2 = new PrintWriter("result2.txt");
        p2.write("Hello 2");
        p2.close();

    }

}
자바 문서 보는 법
--------------------

나의 앱 만들기
=====================
오리엔테이션
---------------------
'우리의 문제 현상은 무엇인가?'
계산기로 하면 너무 손이 많이 감 !
프로그램으로 하면 대기업을 위한 프로그램이라서 너무 복잡함 !
-> 자바로 해결해보자 !
'우선적으로 해야될 일은 현실을 분석하는 것'


//나의 앱 만들기_기본 기능 구현
-------------------------------
public class AccountingApp{

    public static void main(String{ args}){

        System.out.println("Value of supply:" + 10000.0);
        System.out.println("VAT:"(10000.0*0.1));
        System.out.println("Total:"+(10000.0 + 10000.0*0.1));
        System.out.println("Expense:"+(10000.0*0.3));
        System.out.println("Income:"+(10000.0 - 10000.0*0.3));
        System.out.println("Dividend 1:"+(10000.0 - 10000.0*0.3)*0.5);
        System.out.println("Dividend 2:"+(10000.0 - 10000.0*0.3)*0.3);
        System.out.println("Dividend 3:"+(10000.0 - 10000.0*0.3)*0.2);
    }
}
//나의 앱 만들기-
---------------------
public class AccountingApp{

    public static void main(String{ args}){

        double valueOfSupply = 12345.0;
        double vatRate = 0.1;
        double expenseRate = 0.3;
        double vat = valueOfSupply * vatRate;
        double total = valueOfSupply + vat;
        double expense = valueOfSupply * expenseRate;
        double income = valueOfSupply - expense;
        double dividend1 = income * 0.5;
        double dividend2 = income * 0.3;
        double dividend3 = income * 0.2;


        System.out.println("Value of supply:" + valueOfSupply);
        System.out.println("VAT:"+ vat);
        System.out.println("Total:"+ total);
        System.out.println("Expense:"+ expense);
        System.out.println("Income:"+ income);
        System.out.println("Dividend 1:"+ dividend1);
        System.out.println("Dividend 2:"+ dividend2);
        System.out.println("Dividend 3:"+ dividend3);
    }
}

//나의 앱 만들기
----------------
import javax.management.ValueExp;

public class AccountingApp{

    public static void main(String[]args){

        double valueOfSupply = Double.parseDouble(args[0]);
        double vatRate = 0.1;
        double expenseRate = 0.3;
        double vat = valueOfSupply * vatRate;
        double total = valueOfSupply + vat;
        double expense = valueOfSupply * expenseRate;
        double income = valueOfSupply - expense;
        double dividend1 = income * 0.5;
        double dividend2 = income * 0.3;
        double dividend3 = income * 0.2;


        System.out.println("Value of supply:" + valueOfSupply);
        System.out.println("VAT:"+ vat);
        System.out.println("Total:"+ total);
        System.out.println("Expense:"+ expense);
        System.out.println("Income:"+ income);
        System.out.println("Dividend 1:"+ dividend1);
        System.out.println("Dividend 2:"+ dividend2);
        System.out.println("Dividend 3:"+ dividend3);
    }
}

나의 앱 만들기_조건문
------------------------
> 조건문 : 비슷한 프로그램 두가지를 하나로 합칠 때 유용하게 쓰인다.
public class AccountingIFApp {
 
    public static void main(String[] args) {
 
        double valueOfSupply = Double.parseDouble(args[0]);
        double vatRate = 0.1;
        double expenseRate = 0.3;
        double vat = valueOfSupply * vatRate;
        double total = valueOfSupply + vat;
        double expense = valueOfSupply * expenseRate;
        double income = valueOfSupply - expense;
         
        double dividend1;
        double dividend2;
        double dividend3;
         
        if(income > 10000.0) {
            dividend1 = income * 0.5;
            dividend2 = income * 0.3;
            dividend3 = income * 0.2;
        } else {
            dividend1 = income * 1.0;
            dividend2 = income * 0;
            dividend3 = income * 0;
        }
 
        System.out.println("Value of supply : " + valueOfSupply);
        System.out.println("VAT : " + vat);
        System.out.println("Total : " + total);
        System.out.println("Expense : " + expense);
        System.out.println("Income : " + income);
        System.out.println("Dividend 1 : " + dividend1);
        System.out.println("Dividend 2 : " + dividend2);
        System.out.println("Dividend 3 : " + dividend3);
 
    }
 
}
나의 앱 만들기 - 배열 
----------------------
> 배열 : 비슷한 종류의 정보를 정리하기 위한 것


public class AccountingArrayApp {

  public static void main(String[] args) {

    double valueOfSupply = Double.parseDouble(args[0]);
    double vatRate = 0.1;
    double expenseRate = 0.3;
    double vat = valueOfSupply * vatRate;
    double total = valueOfSupply + vat;
    double expense = valueOfSupply * expenseRate;
    double income = valueOfSupply - expense;

    double[] dividendRates = new double[3];
    dividendRates[0] = 0.5;
    dividendRates[1] = 0.3;
    dividendRates[2] = 0.2;
> 배열은 데이터 타입 옆에 대괄호[]를 붙여서 표현, 인스턴스를 만들 때는 배열의 길이를 지정하여 생성
    double dividend1 = income * dividendRates[0]; 
    double dividend2 = income * dividendRates[1];
    double dividend3 = income * dividendRates[2];

    System.out.println("Value of supply : " + valueOfSupply);
    System.out.println("VAT : " + vat);
    System.out.println("Total : " + total);
    System.out.println("Expense : " + expense);
    System.out.println("Income : " + income);
    System.out.println("Dividend 1 : " + dividend1);
    System.out.println("Dividend 2 : " + dividend2);
    System.out.println("Dividend 3 : " + dividend3);

  }

}
나의 앱 만들기 - 반복문
-----------------------
> while 문 : 괄호 안의 조건이 참인 한 블록 내의 작업을 게속 반복
> 
public class AccountingArrayApp {

  public static void main(String[] args) {

    double valueOfSupply = Double.parseDouble(args[0]);
    double vatRate = 0.1;
    double expenseRate = 0.3;
    double vat = valueOfSupply * vatRate;
    double total = valueOfSupply + vat;
    double expense = valueOfSupply * expenseRate;
    double income = valueOfSupply - expense;

    double[] dividendRates = new double[3];
    dividendRates[0] = 0.5;
    dividendRates[1] = 0.3;
    dividendRates[2] = 0.2;

    double dividend1 = income * dividendRates[0];
    double dividend2 = income * dividendRates[1];
    double dividend3 = income * dividendRates[2];

    System.out.println("Value of supply : " + valueOfSupply);
    System.out.println("VAT : " + vat);
    System.out.println("Total : " + total);
    System.out.println("Expense : " + expense);
    System.out.println("Income : " + income);

    double[] dividendRates = new double[3];
    dividendRates[0] = 0.5;
    dividendRates[1] = 0.3;
    dividendRates[2] = 0.2;

    int i = 0;
    while (i < dividendRates.length) {
      System.out.println("Diviidend:" + (income * dividendRates[i]));
      i = i + 1;
    }

  }

}
> while 문을 이용하여 반복적으로 동작하던 작업을 간결하게 바꿀 수 있다 !!
        ....

        double dividend1 = income * dividendRates[0];
        double dividend2 = income * dividendRates[1];
        double dividend3 = income * dividendRates[2];

        System.out.println("Dividend 1 : " + dividend1);
        System.out.println("Dividend 2 : " + dividend2);
        System.out.println("Dividend 3 : " + dividend3);

        ....

        double[] dividendRates = new double[3];
        dividendRates[0] = 0.5;
        dividendRates[1] = 0.3;
        dividendRates[2] = 0.2;
        
        int i = 0;
        while (i < dividendRates.length) {
            System.out.println("Dividend : " + income * dividendRates[i]);
            i = i + 1;
        }
나의 앱 만들기 - 메소드
------------------------
> 메소드 : 클래스의 동작을 나타내는 함수
> Math의 floor, ceil
> PrintWriter의 write, close 등의 메소드

public class AccountingMethodApp {
    public static double valueOfSupply;
    public static double vatRate;
    public static double expenseRate;
    public static void main(String[] args) {
        valueOfSupply = 10000.0;
        vatRate = 0.1;
        expenseRate = 0.3;
        print();
    }
 
    public static void print() {
        System.out.println("Value of supply : " + valueOfSupply);
        System.out.println("VAT : " + getVAT());
        System.out.println("Total : " + getTotal());
        System.out.println("Expense : " + getExpense());
        System.out.println("Income : " + getIncome());
        System.out.println("Dividend 1 : " + getDiviend1());
        System.out.println("Dividend 2 : " + getDiviend2());
        System.out.println("Dividend 3 : " + getDiviend3());
    }
 
    public static double getDiviend1() {
        return getIncome() * 0.5;
    }
    public static double getDiviend2() {
        return getIncome() * 0.3;
    }
    public static double getDiviend3() {
        return getIncome() * 0.2;
    }
 
    public static double getIncome() {
        return valueOfSupply - getExpense();
    }
 
    public static double getExpense() {
        return valueOfSupply * expenseRate;
    }
 
    public static double getTotal() {
        return valueOfSupply + getVAT();
    } 
 
    public static double getVAT() {
        return valueOfSupply * vatRate;
    }
 
}
# result
> Value of supply : 10000.0
VAT : 1000.0
Total : 11000.0
Expense : 3000.0
Income : 7000.0
Dividend 1 : 3500.0
Dividend 2 : 2100.0
Dividend 3 : 1400.0

나의 앱 만들기 - 클래스 
-----------------------
+<<<<<<< HEAD
-----------------------
> 클래스 : 객체지향의 핵심, 서로 연관된 변수와 메소드를 그룹핑해 소속관계를 명확히 해서 이름을 붙여 놓은 것
class Accounting{
    public static double valueOfSupply;
    public static double vatRate;
    public static double expenseRate;
    public static void print() {
        System.out.println("Value of supply : " + valueOfSupply);
        System.out.println("VAT : " + getVAT());
        System.out.println("Total : " + getTotal());
        System.out.println("Expense : " + getExpense());
        System.out.println("Income : " + getIncome());
        System.out.println("Dividend 1 : " + getDiviend1());
        System.out.println("Dividend 2 : " + getDiviend2());
        System.out.println("Dividend 3 : " + getDiviend3());
    }
 
    public static double getDiviend1() {
        return getIncome() * 0.5;
    }
    public static double getDiviend2() {
        return getIncome() * 0.3;
    }
    public static double getDiviend3() {
        return getIncome() * 0.2;
    }
 
    public static double getIncome() {
        return valueOfSupply - getExpense();
    }
 
    public static double getExpense() {
        return valueOfSupply * expenseRate;
    }
 
    public static double getTotal() {
        return valueOfSupply + getVAT();
    } 
 
    public static double getVAT() {
        return valueOfSupply * vatRate;
    }
}
public class AccountingClassApp {
     
    public static void main(String[] args) {
        Accounting.valueOfSupply = 10000.0;
        Accounting.vatRate = 0.1;
        Accounting.expenseRate = 0.3;
        Accounting.print();
        // anotherVariable = ...;
        // anotherMethod = ...;
        // 이전 메소드에서 표현한 것에서 이사시킴, Accounting.를 써서 명확하게 표현함(소속감을 가짐)
    }
 
     
 
}
나의 앱 만들기 - 인스턴스
--------------------------
> 인스턴스 : 클래스를 실제로 실행시킨 실체화된 클래스
class Accounting{
    public double valueOfSupply; //accouunting을 복제했을때, static은 사용되면 안된다.
    public double vatRate;
    public double expenseRate;
    public void print() {
        System.out.println("Value of supply : " + valueOfSupply);
        System.out.println("VAT : " + getVAT());
        System.out.println("Total : " + getTotal());
        System.out.println("Expense : " + getExpense());
        System.out.println("Income : " + getIncome());
        System.out.println("Dividend 1 : " + getDiviend1());
        System.out.println("Dividend 2 : " + getDiviend2());
        System.out.println("Dividend 3 : " + getDiviend3());
    }
 
    public double getDiviend1() {
        return getIncome() * 0.5;
    }
    public double getDiviend2() {
        return getIncome() * 0.3;
    }
    public double getDiviend3() {
        return getIncome() * 0.2;
    }
 
    public double getIncome() {
        return valueOfSupply - getExpense();
    }
 
    public double getExpense() {
        return valueOfSupply * expenseRate;
    }
 
    public double getTotal() {
        return valueOfSupply + getVAT();
    } 
 
    public double getVAT() {
        return valueOfSupply * vatRate;
    }
}
public class AccountingClassApp {
     
    public static void main(String[] args) {
        // instance 
        // 1. 상품
        Accounting a1 = new Accounting(); -> Acounting a1을 복제
        a1.valueOfSupply = 10000.0;
        a1.vatRate = 0.1;
        a1.expenseRate = 0.3;
        a1.print();
        // 2. 상품 
        Accounting a2 = new Accounting(); -> Accounting a2을 복제
        a2.valueOfSupply = 20000.0;
        a2.vatRate = 0.05;
        a2.expenseRate = 0.2;
        a2.print();
         
        a1.print();
    }
}
==============================
## 쉽게 배우는 자바 2
==============================

1. JAVA 제어문
====================

Boolean Datatype
--------------------------
> Boolean : 참과 거짓을 표현하는 데이터 타입
> true와 false 키워드를 이용하여 직접 입력, 메소드의 리턴 값이나 비교 연산으로 도출할 수 있음
public class BooleanApp {

    public static void main(String[] args) {

        System.out.println("one");
        System.out.println(1);

        System.out.println(true);
        System.out.println(false);

        String foo = "Hello world";
        // String true = "Hello world"; reserved word
        // contains 메소드와 같이 결과값이 boolean 데이터 타입인 경우 또는 비교 연산자를 이용하여 계산하는 경우에도 boolean 데이터 타입을 다루게 됨
        System.out.println(foo.contains("world"));  
        System.out.println(foo.contains("egoing"));

    }
}

비교 연산자
----------------------
> 비교 연산자 = 값의 대소, 같음을 비교하는 연산자 (부등호, 등호)
public class ComparisonOperatorApp {
 
    public static void main(String[] args) {
         
        System.out.println(1 > 1); // false
        System.out.println(1 == 1); // true
        System.out.println(1 < 1);
        System.out.println(1 >= 1);
         
    }
 
}

조건문 형식
--------------------
> 조건문은 중첩할 수 있고, if와 else는 하나의 조건문에 한 번만 들어갈 수 있지만, eise if는 여러 개가 들어갈 수 있다.
# if
## 조건식
### 코드블럭 (실행할 코드)
#### else if
##### else
public class IfApp {
 
    public static void main(String[] args) {
 
        System.out.println("a");
        if(false) {
            System.out.println(1);
        } else if(true) {
            System.out.println(2);
        } else {
            System.out.println(3);
        }
        System.out.println("b");
 
    }
 
}
조건문 응용 1,2
------------------------
public class AuthApp {
 
    public static void main(String[] args) {
         
        String id = "egoing";
        String inputId = args[0];
         
        System.out.println("Hi.");
        //==와 같은 비교 연산자는 기본 데이터 형과는 달리 문자열과 같은 객체에는 의도치 않은 결과를 가져옴
        //if(inputId == id) {
        if(inputId.equals(id)) {
            System.out.println("Master!");
        } else {
            System.out.println("Who are you?");
        }
 
    }
 
}
}
> boolean 데이터를 연산하기 위한 조건 연산자 사용
> 조건 연산자에는 &&(AND)와 ||(OR, shift + \)가 있다.
public class AuthApp {
 
    public static void main(String[] args) {
         
        String id = "egoing";
        String inputId = args[0];
         
        String pass = "1111";
        String inputPass = args[1];
         
        System.out.println("Hi.");
         
        if(inputId.equals(id) && inputPass.equals(pass)) {
            System.out.println("Master!");
        } else {
            System.out.println("Who are you?");
        }       
 
    }
 
}
>> && 연산자는 전항과 후항이 모두 참일 경우에만 참을 반환하고, 아니면 거짓을 반환한다.
>> || 연산자는 전항과 후항 중 하나라도 참일 경우에 참을 반환, 모두 거짓일 때에만 거짓을 반환한다.
>> && 연산자는 || 연산자보다 우선순위가 높다 !!

 == vs equals
------------------
# 자바에서는 기본적으로 다루는 데이터 타입이 존재, 이러한 데이터 타입을 <원시 데이터 타입> 이라고 부름
## boolean, byte, char, short, int, long, float, double 8개가 있다.

+>원시 데이터 타입의 변수는 선언되면 메모리(stack)에 공간에 할당, 그 메모리 공간 안에 실제 값이 들어감
int a = 1;
int b = 1;

String s1 = new String("JAVA");
String s2 = new String("JAVA");
> new 키워드를 통한 인스턴스를 만든 시점에 또 다른 메모리 구역(Heap)에서 새로운 공간을 할당
String s3 = "JAVA";
String s4 = "JAVA";
> 문자열 리터럴로 문자열로 생성할 때, 이미 같은 문자열을 생성한 적이 있다면, 새로 메모리 공간을 할당하지 않고 새로운 변수는 기존의 문자열이 저장된 메모리(String pool(Heap))의 주소를 가리키게 된다.

# == 연산자는 변수가 일차적으로 가리키고 있는 메모리 공간의 값을 기준으로 판단
> 반면 equals 메소드는 구현에 따라 다르지만, 변수가 최종적으로 가리키고 있는 값을 기준으로 판단

논리연산자
-----------------
> ! 연산자 : NOT 연산을 수행하고 참, 거짓 값을 반전시킨다.

public class AuthApp2 {
 
    public static void main(String[] args) {
         
        String id = "egoing";
        String inputId = args[0];
         
        String pass = "1111";
        String pass2 = "2222";
        String inputPass = args[1];
        // 둘 중 하나만 충족, || 연산자를 이용하고, 이 조건을 boolean 변수 IsRightPass에 할당하여 간결성있게 표현
        System.out.println("Hi.");
        boolean isRightPass = (inputPass.equals(pass) || inputPass.equals(pass2));
        if(inputId.equals(id) && isRightPass ) {
            System.out.println("Master!");
        } else {
            System.out.println("Who are you?");
        }       
 
    }
 
}

반복문, 배열 
-----------------
> 반복문 : 조건에 따라 특정한 작업을 반복하게 하는 제어문
> 자바에서는 while문, for문 등으로 반복문을 구현
public class LoopApp {
 
    public static void main(String[] args) {
         
        System.out.println(1);
        System.out.println("=== while ===");
        int i = 0;
        //..
        while(i < 3) {
            System.out.println(2);
            System.out.println(3);
//          i = i + 1;
            //..
            i++;
        }
        System.out.println("=== for ===");
        for(int j=0; j < 3; j++) {
            System.out.println(2);
            System.out.println(3);
        }
         
        System.out.println(4);
 
    }
 
}
>> while문 : 조건식이 참일 동안에 코드블럭의 작업을 반복, 조건식에 true을 입력할 경우 조건이 항상 참이기 때문에 무한으로 반복하게 된다
>> For문은 조건식이 3개의 부분을 나누어짐
# 변수의 초기화
## 조건식
### 1회 반복을 끝내고 수행할 연산 
각각의 부분은 세미콜론(;)으로 구분이 되어있음
변수의 초기화는 for문이 시작될 때 한 번만 수행되고, 조건식이 참일 경우에만 반복
1회 반복이 끝나면(}부분) 지정한 연산을 처리하고 다시 조건식을 확인하여 반복작업을 실행

>>변수의 초기화 부분에서 변수를 새로 선언했다면, 그 변수는 for문 안에서만 존재하고, for문을 벗어나면 사라진다 

>>> 배열

public class ArrayApp {
 
    public static void main(String[] args) {
         
        // egoing, jinhuck, youbin 
//      String users = "egoing, jinhuck, youbin";
        String[] users = new String[3];
        users[0] = "egoing";
        users[1] = "jinhuck";
        users[2] = "youbin";
         
        System.out.println(users[1]);
        System.out.println(users.length);
         
        int[] scores = {10, 100, 100}; // 원소, element
        System.out.println(scores[1]);
        System.out.println(scores.length);
 
    }
 
}
 
=======
-----------------------
>>>>>>> 881d7c444e50d32fc2984bfcebb7c3d7c00cf598
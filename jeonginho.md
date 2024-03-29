> 2023-05-03
> Chapter 8
>> Chapter 8-1 변수의 정의
<pre><code>
public class Variable {
    public static void main(Static[] args) {
        int a = 1; // a는 정수 1이다.
        System.out.println(a);
        
        int b = 1.1; // 1.1은 정수(x) ERROR.
        double c = 1.1; // 1.1은 실수(o) -> c는 실수 1.1이다.
        System.out.println(c);
        String d = "Hello World"; 
        // "Hello World"는 문자열 d에 저장됨.
        System.out.println(d);
    }
}
</code></pre>
# 결과 : 1, 1.1, Hello World
>> Chapter 8-2 변수의 효용
<pre><code>
public class Letter {
    public static void main(String[] args) {
        String name = "leezche"; 
        // "leezche"는 문자열 name에 저장됨
        System.out.println("Hello, "+name+" ... "+name+" ... egoing ... bye");
        double VAT = 10.0;
        System.out.println(VAT);
    }
}
</code></pre>
# 결과 : Hello, leezche ... leezche ... egoing ... bye
>> Chapter 8-3 데이터 타입의 변환 - casting
<pre><code>
public class Casting {
    public static void main(String[] args) {
        double a = 1.1;
        double b = 1; 
        // 정수 1을 실수 1로 바꾸고 b에 담아서 출력 시 1.0이 나옴, 손실이 일어나지 않음
        double b2 = (double) 1; 
        // 강제로 1을 실수로 변환하여 1.0 출력.
        System.out.println(b);
        int c = 1.1; 
        // ERROR. 
        double d = 1.1;
        int e = (int)1.1; 
        // 강제로 1.1을 정수로 변환하여 1 출력, 손실이 일어남
        
        System.out.println(e);
        String f = Integer.toString(1); 
        // 1이 출력 되지만 실제로 1은 문자열이다.
        System.out.println(f.getClass()); 
        // .getClass()를 이용하여 출력 시 값의 데이터타입을 함께 출력.
    }
}
</code></pre>
# 결과 : 1.0, 1, 1, class java.lang.String
> Chapter 9
>> Chapter 9-1 프로그래밍이란 무엇인가
<pre><code>
public class Program {
    public static void main(String[] args) {
         
        System.out.println(1); // 1 출력
        System.out.println(2); // 2 출력
        System.out.println(3); // 3 출력
    }
}
</code></pre>
# 결과 : 1, 2, 3
> 프로그래밍을 하는 이유는 자동화 하기 위함.
> 컴퓨터 프로그래밍을 이용하여 사람이 잘 못하는 일을 기계에게 위임하여 자동화할 수 있음. (이런 작업을 하는 언어중 가장 유명한 언어가 JAVA.)
>> Chapter 9-2 프로그램 만들기 - IoT 라이브러리 설치하기
<pre><code>
public class programming {   
}
</code></pre>
> 방법 : iot 사물을 제어할 수 있는 프로그램을 작성하기 위해서 외부 패키지를 다운받아 org 폴더를 programming 프로젝트에 드래그 앤 드랍 시킨다.
>> Chapter 9-3 IoT 프로그램 만들기
<pre><code>
import org.opentutorials.iot.Elevator; 
// org폴더 > opentutorials > iot > Elevator를 import 함. 
import org.opentutorials.iot.Lighting;
// org폴더 > opentutorials > iot > Lighting를 import 함.
import org.opentutorials.iot.Security;
// org폴더 > opentutorials > iot > Security를 import 함.
public class programming {
    public static void main(String[] args) {
        String id = "JAVA APT 507"; 
        // 동작은 같지만 중복이 제거됨.
         
        // Elevator call 
        Elevator myElevator = new Elevator(id);
        // Elevator는 데이터 타입, myElevator는 변수
        myElevator.callForUp(1); 
        // 1층으로 엘레베이터를 보내라는 명령문
         
        // Security off 
        Security mySecurity = new Security(id);
        mySecurity.off();
         
        // Light on
        Lighting hallLamp = new Lighting(id+" / Hall Lamp");
        hallLamp.on();
        //hallLamp 의 불을 킨다.
         
        Lighting floorLamp = new Lighting(id+" / floor Lamp");
        floorLamp.on();
        //floorLamp 의 불을 킨다.
    }
}
</code></pre>
# 결과 : JAVA APT 507 -> Elevator callForUp stopFloor : 1
# JAVA APT 507 -> Security off
# JAVA APT 507 / Hall Lamp -> Lighting on
# JAVA APT 507 / floorLamp -> Lighting on
> Chapter 10 - 디버거
>> 이클립스에서 디버그 하는 방법은 우측상단 Run java 버튼 옆 아래 화살표를 눌러 Debug java를 클릭하면 된다.
>> 이클립스에서 브레이크 포인트를 지정하는 방법은 코드 편집창에서 줄 번호 왼편을 더블클릭하여 브레이크 포인트를 지정할 수 있다.
>> 브레이크 포인트를 지정하고 디버거를 실행하면 브레이크 포인트까지 코드가 실행되며 그 이후로 실행이 정지된다.
>> 브레이크 포인트를 해제 하는 방법은 지정했던 브레이크 포인트를 다시 클릭하면 해제할 수 있다.
>> 이클립스에서 우측의 Variable 탭에서 변수들을 확인할 수 있다.
>> Step Into 버튼을 클릭하면 코드의 자세한 실행과정(메소드)를 볼 수 있다.
>> 다시 원래의 코드로 돌아가고자 할 경우에는 Step Return 버튼을 클릭하여 돌아갈 수 있다.

>8, 9, 10 ENDS

> 2023-05-04
>> 11강, 12강 스터디 내용

> Chapter 11-1 입력과 출력
<pre><code>
import javax.swing.JOptionPane; 
// javax.swing에 속해있는 JOptionPane이 로드되었다.
 
import org.opentutorials.iot.DimmingLights;
import org.opentutorials.iot.Elevator;
import org.opentutorials.iot.Lighting;
import org.opentutorials.iot.Security;
 
public class OkJavaGoInHomeInput {
    public static void main(String[] args) {
         
        String id = JOptionPane.showInputDialog("Enter a ID");
        // 이름 입력 (showInputDialog)
        String bright = JOptionPane.showInputDialog("Enter a Bright level");
        // 밝기 입력 (showInputDialog)

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
         
        DimmingLights moodLamp = new DimmingLights(id+" moodLamp");
        moodLamp.setBright(Double.parseDouble(bright));
        //Double.parseDouble()시 double형으로 변환 됨.
        moodLamp.on();
    }
}
</code></pre>

# 입력 : JAVA APT 1004, 10
# 결과 : JAVA APT 1004 -> Elevator callForUp stopFloor : 1
# JAVA APT 1004 -> Security off
# JAVA APT 1004 / Hall Lamp -> Lighting on
# JAVA APT 1004 / floorLamp -> Lighting on
# JAVA APT 1004 moodLamp -> DimmingLights bright : 10.0
# JAVA APT 1004 moodLamp -> Lighting on
> Chapter 11-2 입력과 출력 - arguments & parameter
<pre><code>
import javax.swing.JOptionPane; 
// javax.swing에 속해있는 JOptionPane이 로드되었다.
 
import org.opentutorials.iot.DimmingLights;
import org.opentutorials.iot.Elevator;
import org.opentutorials.iot.Lighting;
import org.opentutorials.iot.Security;
 
public class OkJavaGoInHomeInput {
 
    public static void main(String[] args) {
        //args()는 매개변수이다.(patameter)
        String id = args[0];
        String bright = args[1];

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
         
        DimmingLights moodLamp = new DimmingLights(id+" moodLamp");
        moodLamp.setBright(Double.parseDouble(bright));
        //Double.parseDouble()시 double형으로 변환 됨.
        moodLamp.on();
    }
}
</code></pre>

>> argument는 사용자 입력을 의미하는 문자열 배열이다.

>> parameter는 함수에서 전달되어서 사용되는 변수이다.

>> argument는 main()함수의 매개변수로 작용한다.

>> 196줄에 브레이크를 걸고 디버그 시키면 vscode 기준 왼편에 VARIABLES.Local 창이 뜨고 그 속에 args, id, bright에 할당한 값이 보인다.

<pre><code>
first(a,b);
return;

a,b("parameter","argument")
</code></pre>
>> 위 코드에서 a,b는 parameter이다.

>> 위 코드에서 "parameter","argument"는 argument이다.

> Chapter 12-1 직접 컴파일 - 실행 - 소개
>> 이클립스,vscode 없이 혼자 컴파일하기

>> 1. 자바 확장자가 붙은 소스코드를 Class확장자가 붙은 실행파일로 바꾼다 (Compile)

>> 2. 클래스 확장자가 붙은 파일을 실행한다(Run)

>> 3. 실행할 때 입력값을 준다 (Input)

> Chapter 12-2 직접 컴파일 - 실행 - 실행환경 살펴보기
>> 직접 컴파일을 하기 위해 자바의 설치경로를 알고 있어야 한다.

>> 터미널 열기 Window - 윈도우키 + R키로 실행창을 키고, cmd를 입력하여 명령프롬프트를 실행한다.

>> 컴파일, 실행을 하기 위해선 명령 프롬프트에 javac을 입력하여 컴파일 할 수 있다.

>> 자바의 설치경로(C:\Program Files\Java\jdk-17\bin\javac.exe)

>> 환경 변수는 윈도우 탐색기에서 내 PC 항목을 오른쪽 버튼으로 클릭하여 나오는 팝업창에 속성을 클릭한다. 이후 고급시스템 설정을 클릭하고 환경 변수를 클릭하면 환경 변수 목록을 확인할 수 있다. 목록 중 Path를 더블클릭하면 수정 할 수있다.

>> Path는 디렉터리 경로의 목록. 사용자가 전체 경로를 지정하지 않고 명령을 입력하면 목록을 확인하여 해당 명령어가 경로에 속하는지를 살펴본다. 이 과정을 통하여 어떠한 경로든 해당 명령어로 실행 파일을 실행할 수 있다.

> Chapter 12-3 직접 컴파일 - 실행 - 컴파일과 실행하기

>> 명령 프롬프트에서 소스 코드가 위치한 경로를 붙여넣기 한다. (ex)cd C:\Users\egoing\Desktop\java1\Programming

>> dir 명령어로 프로젝트 디렉토리 내부 구조를 확인할 수 있다.

>> 터미널에 javac를 입력하면 javac 명령어의 사용 방법을 보여준다.

>> javac Program.java 를 입력하여 Program.java를 컴파일한다. 에러가 날 시 javac -cp "." Program.java를 입력한다.

>> 컴파일된 클래스 파일을 실행하는 방법은 java Program을 입력한다. 에러가 날 시 java -cp "." Program 을 입력한다.

> Chapter 12-4 직접 컴파일 - 실행 - 라이브러리이용
<pre><code>
import org.opentutorials.iot.Elevator;
import org.opentutorials.iot.Lighting;
import org.opentutorials.iot.Security;
 
public class OkJavaGoInHome {
 
    public static void main(String[] args) {
         
        ....
    }
}
</code></pre>
>> OkJavaGoInHome.java 파일을 컴파일 하기 위해서는 OkJavaGoInHome가 Import 구문을 통해 org.opentutorials.iot 클래스들을 불러들이고 있어서 컴파일을 실행할 때 자동적으로 org.opentutorials.iot의 Elevator, Lighting, Security 클래스들도 컴파일한다. 이때 lib 폴더를 새로 만들어서 org 폴더를 lib 폴더 내부로 이동시킨다.

>> org.opentutorials.iot 패키지는 lib 라이브러리의 일부가 되었다. 그렇기 때문에 OkJavaGoInHome.java 파일은 제대로 실행되지 않는다.

>> 외부 라이브러리도 포함해서 컴파일 하기 위해서는 명령 프롬프트에서 javac -cp ".;lib" OkJavaGoInHome.java 명령어를 입력한다.

>> 외부 라이브러리도 포함해서 실행하려면 java -cp ".;lib" OkJavaGoInHome 명령어를 입력한다.

>> 1. 라이브러리란 다른 사람들 만들어 놓은 여러 유용한 기능을 모아둔 클래스의 집합.
>> 2. 패키지는 특정한 기능들을 모아둔 더 작은 단위의 집합.

> Chapter 12-5 직접 컴파일 - 실행 - 입력과 출력

<pre><code>
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
</code></pre>
>> org.opentutorials.iot 패키지는 다시 iot 폴더 밖으로 꺼낸다.

>> 터미널에서 javac OkJavaGoInHomeInput.java 명령어를 입력하여 컴파일 한다.

>> 터미널에서 아규먼트를 주기 위해서 실행할 클래스 파일 이름다음에 연달아서 입력한다. -> java OkJavaGoInHomeInput "JAVA APT 507" 15.0 (2번째 입력값 15.0은 큰 따옴표 안에 넣어도 되고, 소수점은 생략할 수 있다.)

>> 커맨드 라인에서 우리가 임의값을 추가하여 프로그램을 작동시킨다면 이것만으로 충분히 많은 일을 가치있게 할 수 있다. 

>> * 2023-05-04 11,12 END 

> * 2023-05-08 [Chapter 13 ~ 14.4]-

> Chapter 13 - 1 자바 문서 보는 법 - API vs UI

>> 자바 프로그램 : 자바 도구 응용 + 시간적 순서에 따른 동작

>> 프로그램 : 작업들의 시간적 순서에 주목

>> 애플리케이션 : 도구의 응용에 주목

>> 자바 API : 자바의 도구들을 응용하여 사용하기 위해서 일정한 조작 장치를 구성 한 것.

>> *자바 프로그램은 다른 자바 프로그램에서 사용이 가능하며 다른 프로그램에서 사용할 수 있도록 만들어 둔 장치 또한 API이다.

>> UI : 사용자가 자바 프로그램을 사용할 수 있도록 만들어 둔 장치

> Chapter 13 - 2 자바 문서 보는 법 - 패키지, 클래스, 변수, 메소드

>> 자바 프로그램을 만들기 위해서는 자바의 도구들을 사용할 수 있게 만든 장치인 자바 API를 이용한다.

>> API Documentation 페이지 왼쪽의 위쪽 섹션에는 패키지들에 대한 정보를 담고 있고, 왼쪽의 아래 섹션에는 클래스에 대한 정보를 담고 있다.

>> 패키지는 비슷한 성격의 클래스들을 하나의 묶음으로 정리한 것.

>> 클래스는 변수와 메소드라는 것을 모아서 하나의 묶음으로 정리한 것.

> Chapter 13 - 3 자바 문서 보는 법 - 클래스
<pre><code>
public class ClassApp {
 
    public static void main(String[] args) {
         
        System.out.println(Math.PI);
        System.out.println(Math.floor(1.6));
        System.out.println(Math.ceil(1.6));
    }
}
</code></pre>
# 결과 : 3.141592653689793, 1.0, 2.0
>> 위 코드는 수학과 관련된 작업을 해야하며 파이의 크기를 출력하기 위하여 math라는 클래스를 불러들여 출력하는 코드이다.

>> 위와 같이 클래스를 불러들여 원하는 값을 출력하기 위해선 (Math.PI)처럼 클래스.값 을 넣어야 한다.

>> 클래스는 서로 연관된 변수와 메소드들을 모아서 이름을 붙이고 묶음으로 정리한 것.

> Chapter 13 - 4 자바 문서 보는 법 - 인스턴스

>> 클래스 안에는 변수와 메소드가 존재한다.

>> 인스턴스는 클래스에 있는 속성을 사용하는 복제품을 만드는 것이다. 단 인스턴스를 사용하려면 클래스안에 constructor가 있어야 한다.

>> 클래스중에 constructor가 없는 클래스(예:Math)는 인스턴스로 사용하지 못하는 클래스. 즉, 인스턴스를 사용하려면 해당 클래스에 constructor가 있어야 한다.

> Chapter 13 - 5 자바 문서 보는 법 - 상속
<pre><code>
//Class PrintWriter

java.lang.Object
    java.io.Writer
        java.io.PrintWriter
</code></pre>
>> 1. 들여쓰기 되어 표현된 각각의 클래스 간의 관계는 상속 관계.

>> PrintWriter 클래스는 Writer 클래스에서 상속을 받음.

>> Writer클래스는 Object 클래스로부터 상속을 받음.

>> 2. 자식에 해당하는 클래스는 부모에 해당하는 클래스의 모든 변수와 메소드를 사용할 수 있다.

>> 3. 그래서 PrintWriter 클래스는 Writer의 write 메소드를 사용할 수 있고
, Object의 toString 메소드를 사용할 수 있다.

> Chapter 14 - 2 나의 앱 만들기 - 오리엔테이션
> Chapter 14 - 3 나의 앱 만들기 - 기본 기능 구현
<pre><code>
public class AccountingApp {

	public static void main(String[] args) {
		
		System.out.println("Value of supply : " + 10000.0);
        System.out.println("VAT : " + (10000.0 * 0.1));
        System.out.println("Total : " + (10000.0 + (10000.0 * 0.1)));
        System.out.println("Expense : " + (10000.0 * 0.3));
        System.out.println("Income : " + (10000.0 - (10000.0 * 0.3)));
        System.out.println("Dividend 1 : " + (10000.0 - (10000.0 * 0.3)) * 0.5);
        System.out.println("Dividend 2 : " + (10000.0 - (10000.0 * 0.3)) * 0.3);
        System.out.println("Dividend 3 : " + (10000.0 - (10000.0 * 0.3)) * 0.2);

	}

}
</code></pre>
>> * 오리엔테이션에서 궁리한 문제에 대한 해결책을 제시하는 코드. 

>> 공급가를 10000.0 으로 잡고 시작.

>> 부가 가치세는 10000.0에 0.1.을 곱한 10000.0 * 0.1.

>> 총 판매가는 공급가와 부가가치세를 합한 10000.0 + (10000.0 * 0.1).
비용은 판매가의 30%이므로 10000.0 * 0.3.

>> 수익은 판매가에 비용을 뺀 값이므로 10000.0 - (10000.0 * 0.3).

>> 첫 번째 배당자는 수익의 50%를 배당받으므로 (10000.0 - (10000.0 * 0.3)) * 0.5.

>> 두 번째 배당자는 수익의 30%를 배당받으므로 (10000.0 - (10000.0 * 0.3)) * 0.3.

>> 세 번째 배당자는 수익의 20%를 배당받으므로 (10000.0 - (10000.0 * 0.3)) * 0.2.

> Chapter 14 - 3 나의 앱 만들기 - 변수도입
<pre><code>
public class AccountingApp {
 
    public static void main(String[] args) {
 
        double valueOfSupply = 10000.0; // 공급가
        double vatRate = 0.1; // 부가가치세율
        double expenseRate = 0.3; 
        double vat = valueOfSupply * vatRate;
        double total = valueOfSupply + vat;
        double expense = valueOfSupply * expenseRate;
        double income = valueOfSupply - expense;
        double dividend1 = income * 0.5;
        double dividend2 = income * 0.3;
        double dividend3 = income * 0.2;
 
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
</code></pre>
>> 변수를 도입하면 코드의 재사용성을 높이고 가독성을 높일 수 있다.

> Chapter 14 - 4 나의 앱 만들기 - 입력값 도입
<pre><code>
public class AccountingApp {
 
    public static void main(String[] args) {
 
        double double valueOfSupply = Double.parseDouble(args[0]);
        // 공급가
        double vatRate = 0.1; // 부가가치세율
        double expenseRate = 0.3; 
        double vat = valueOfSupply * vatRate;
        double total = valueOfSupply + vat;
        double expense = valueOfSupply * expenseRate;
        double income = valueOfSupply - expense;
        double dividend1 = income * 0.5;
        double dividend2 = income * 0.3;
        double dividend3 = income * 0.2;
 
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
</code></pre>
>> valueOfSupply(공급가)에 입력값을 입력받아 공급가를 사용자가 지정할 수 있도록 코드를 수정했다.

>> 터미널에서 실행할 시 : javac 명령어로 AccountingApp.java를 컴파일하고 java 명령어로 AccountingApp을 실행하고 아규먼트로 원하는 공급가액을 입력하여 실행하면 valueOfSupply에 내가 직접 지정한 값으로 계산을 하여 값이 반환된다.


2023-05-08 13 ~ 14-4 END 
-------------

<hr/>

<2023-05-09 / 14-5 ~ 15>
-------------

* 조건문
<pre><code>
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
            // 만약 income이 10000.0원 보다 클 시 구문 실행
            dividend1 = income * 0.5;
            dividend2 = income * 0.3;
            dividend3 = income * 0.2;
        } else { 
            // 만약 income이 10000.0원 보다 작을 시 구문 실행
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
</code></pre>
-제어문 : 프로그램의 실행 과정을 조건에 따라 바꾸는 것.   
-제어문의 종류 : 조건문, 반복문
* 배열
<pre><code>
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
        //double 형 데이터로 이루어져 있는 배열, new double[3] = double형의 데이터를 3개를 담을 수 있는 수납공간이 만들어 짐.
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
        System.out.println("Dividend 1 : " + dividend1);
        System.out.println("Dividend 2 : " + dividend2);
        System.out.println("Dividend 3 : " + dividend3);
    }
}
</code></pre>
-배열 : 서로 연관된 데이터를 정리정돈하는 수단

* 반복문(while)
<pre><code>
public class AccountingArrayLoopApp {
 
    public static void main(String[] args) {
 
        double valueOfSupply = Double.parseDouble(args[0]);
        double vatRate = 0.1;
        double expenseRate = 0.3;
        double vat = valueOfSupply * vatRate;
        double total = valueOfSupply + vat;
        double expense = valueOfSupply * expenseRate;
        double income = valueOfSupply - expense;
         
         
 
        System.out.println("Value of supply : " + valueOfSupply);
        System.out.println("VAT : " + vat);
        System.out.println("Total : " + total);
        System.out.println("Expense : " + expense);
        System.out.println("Income : " + income);
         
        double[] dividendRates = new double[3];
        dividendRates[0] = 0.5;
        dividendRates[1] = 0.3;
        dividendRates[2] = 0.2;
         
             
        int i = 0; // 반복하기전 i를 0으로 초기화시킴.
        while(i < dividendRates.length) {
            // 3보다 i의 값이 작을 동안 
            // 반복할 때 마다 i의 값을 1씩 증가시킨다.
            System.out.println("Dividend : " + (income*dividendRates[i]) );
            i = i + 1;
        }
    }
}
</code></pre>
-배열과 반복문을 함께 사용하면 프로그램을 훨씬 간결하게 만들 수 있다.   
-while 문은 괄호 안의 조건이 참인 한 블록내의 작업을 계속 반복한다.
-반복문은 배열과 단짝.

* 메소드
<pre><code>
public class AccountingMethodApp {
    //valueOFsupply, vatRate, expenseRate를 main 바깥에서 선언.
    //전역변수로 선언하면 main뿐만 아니라 어느곳에서든 사용될 수 있다.
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
</code></pre>
-메소드 : 서로 연관된 코드를 그룹핑해서 이름을 붙인 정리정돈된 상자
ex) Math의 floor, ceil, PrintWriter의 write, close등.   
-메소드로 전역변수를 설정할 시 main함수 안에서 따로 지역변수를 지정하지 않아도 사용자가 많은 함수를 만들 시 미리 만들어놓은 Public 전역변수를 호출하여 코드를 단정하게 만들 수 있다.

* 클래스
<pre><code>
//ClassApp
class Accounting{
    //AccountingApp 소속의 변수들을 이사시킴.
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
        //기존 변수 앞에 Class로 선언한 Accounting.을 붙여 소속관계를 명확하게 할 수 있다.
        Accounting.valueOfSupply = 10000.0;
        Accounting.vatRate = 0.1;
        Accounting.expenseRate = 0.3;
        Accounting.print();
        // anotherVariable = ...;
        // anotherMethod = ...;
    }
}
</code></pre>
-클래스는 서로 연관된 변수와 메소드를 그룹핑한 것. (정리정돈의 상자)   
-메소드, 클래스 등이 중요한 이유는 소프트웨어를 만들어 감에 있어서 구조를 결정하기 때문.   
-클래스는 객체지향의 핵심이다.

* 인스턴스
<pre><code>
class Accounting{
    public double valueOfSupply;
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
        Accounting a1 = new Accounting(); // Class를 복제함.
        a1.valueOfSupply = 10000.0;
        a1.vatRate = 0.1;
        a1.expenseRate = 0.3;
        a1.print(); 
        // Accounting1의 내부 상태는 모두 같아서 a2 이후에 print 문을 선언해도 상관없다.
         
        Accounting a2 = new Accounting(); // Class를 복제함
        a2.valueOfSupply = 20000.0;
        a2.vatRate = 0.05;
        a2.expenseRate = 0.2;
        a2.print();
    }
}
</code></pre>
-인스턴스는 하나의 클래스를 복제해서 서로 다른 데이터의 값과 서로 같은 메소드를 가진 복제본을 만드는 것.   
-위 코드에서 new Accounting()을 사용하여 Class를 복제함.  
-따라서 Class이름 앞에 new를 붙여서 만든 것을 인스턴스라고 함.   
-이 후 Public static에서 static을 빼도 코드에 오류가 없음.

<2023-05-09 / 14-5 ~ 15 END>
-------------

<hr/>

<2023-05-10 / JAVA 2 / 1 ~ 7.3>
-------------

* Boolean Datatype
<pre><code>
public class BooleanApp {
 
    public static void main(String[] args) {
         
        System.out.println("One");
        System.out.println(1);
         
        System.out.println(true); // 첫번째 데이터 타입
        System.out.println(false); // 두번째 데이터 타입
         
        String foo = "Hello world";
        // String true = "Hello world"; reserved word
         
        System.out.println(foo.contains("world"));
        System.out.println(foo.contains("egoing"));
    }
}
</code></pre>
-'.contains' 라는 메소드를 사용하면 return 값으로 그 문자열의 입력값으로 전달할 어떤 값이 들어있다면 True를 리턴하고 없다면 False를 리턴한다.   
-foo.contains() 안에 world 라는 문자열이 들어있으므로 true를 반환한다.   
-foo.contains() 안에 egoing 라는 문자열은 foo에서 입력되지 않았으므로 False를 반환한다.   

* 비교연산자
<pre><code>
public class ComparisonOperatorApp {
 
    public static void main(String[] args) {
         
        System.out.println(1 > 1); // false 반환
        System.out.println(1 == 1); // true 반환
        System.out.println(1 < 1); // false 반환
        System.out.println(1 >= 1); // true 반환
    }
}
</code></pre>
-a > b : a가 b보다 큼   
-a < b : a가 b보다 작음   
-a >= b : a가 b보다 크거나 같음    
-a <= b : a가 b보다 작거나 같음   
-a == b : a가 b와 같음   
-a != b : a가 b와 같지 않음   
-위 설명에 해당하는 진술이 참이라면 True, 아니라면 False를 반환.

* 조건문 형식 4-1
<pre><code>
public class IfApp {
 
    public static void main(String[] args) {
 
        System.out.println("a");
        if(false) { // 만약 조건식에 부합하지 않는다면
            System.out.println(1);
        } else if(true) { // 만약 조건식에 부합한다면
            System.out.println(2);
        } else { // else if 조건식이 아니라면
            System.out.println(3);
        }
        System.out.println("b");
    }
}
</code></pre>
-'IF'문의 구성요소 : 조건식 - 코드블럭(실행할 코드) - else if - else   
-'IF'와 '조건식'이 필수구성요소 이며, 나머지는 필수요소가 아니다.   
-'조건식'에는 'Boolean'타입만 기입할 수 있다.   
<pre><code>
 if (조건식) {
    // code
} else if (조건식) {
} else {
}
</code></pre>
-위와 같은 코드에서 IF의 조건식에 해당되면 IF속 코드가 실행되며, 아니라면 else IF의 조건을 확인하고 else IF의 코드를 실행하고, else IF 또한 아니라면 else의 코드를 실행한다.   

* 조건문 응용 1
<pre><code>
public class AuthApp {
    public static void main(String[] args) {
         
        String id = "egoing"; // 문자열 id 선언 후 "egoing" 값 기입
        String inputId = args[0]; // 들어갈 id는 args값의 0번째
         
        System.out.println("Hi."); // Hi.
         
        //if(inputId == id) { // 만약 inputId와 id값이 같다면 
        if(inputId.equals(id)) { // 위 주석처리 한 구문과 같은 의미
            System.out.println("Master!"); 
            // 같다면 Master! 출력
        } else { 
            System.out.println("Who are you?"); 
            // 아니라면 Who are you? 출력
        }
    }
}
</code></pre>

* 조건문 응용 2
<pre><code>
public class AuthApp {
 
    public static void main(String[] args) {
         
        String id = "egoing";
        String inputId = args[0];
         
        String pass = "1111"; // 비밀번호 1111 선언
        String inputPass = args[1];
         
        System.out.println("Hi.");
         
        if(inputId.equals(id) && inputPass.equals(pass)) {
            System.out.println("Master!");
        } else {
            System.out.println("Who are you?");
        }       
    }
}
</code></pre>
-위 코드에서 if(inputId.equals(id) && inputPass.equals(pass))를 해석하면 만약 아이디도 동일하고, 패스워드도 동일하다면 아래 구문을 동작시킨다. 하지만 그렇지 않으면 else 구문을 동작시킨다.   
-논리연산자 &&는 앞 구문이 참이고 뒤 구문이 참이면 전체 구문을 참으로 반환한다.   

* == vs equals   
-원시 데이터 타입 : boolean, byte, char, short, int, long, float, double   
-원시 데이터 타입의 변수는 선언되면 메모리에 공간이 할당 되며 실제값이 들어간다.   
-원시 데이터의 경우 == 연산자는 변수가 가리키는 값을 토대로 비교한다.   
-인스턴스 간 == 연산자를 이용할 경우 그 메모리의 주소를 비교하게 된다.
-원시 데이터는 equals를 가지고 있지 않다.
<pre><code>
int a = 1;
int b = 1;

String s1 = new String("JAVA");
String s2 = new String("JAVA");

String s3 = "JAVA";
String s4 = "JAVA";
</code></pre>
-위 코드의 경우 s1,s2,s3(4)변수는 각각 10번지, 11번지, 12번지라는 주소값을 가리키고 있기 때문에 == 연산자를 이용하면 false라고 연산한다.   
-반면, equals 메소드는 변수가 최종적으로 가리키고 있는 값을 기준으로 판단하여 다른 번지에 저장되어 있는 s1,s2,s3(4)에 대해서도 서로 같다고 판단한다.

* 논리연산자
-조건연산자 : &&, ||
-논리연산자 || : L || R 중 하나라도 참이면 True를 반환.
-논리연산자 ! : NOT 연산 수행후 참, 거짓 값을 반전.   
<pre><code>
public class AuthApp2 {
 
    public static void main(String[] args) {
         
        String id = "egoing";
        String inputId = args[0];
         
        String pass = "1111";
        String pass2 = "2222";
        String inputPass = args[1];
         
        System.out.println("Hi.");
        boolean isRightPass = (inputPass.equals(pass) || inputPass.equals(pass2));
        // 둘중 하나라도 true면 true 반환
        if(inputId.equals(id) && isRightPass ) 
        {
            System.out.println("Master!");
        } else {
            System.out.println("Who are you?");
        }       
    }
}
</code></pre>
-boolean isRightPass = (inputPass.equals(pass) || inputPass.equals(pass2)); 에서 하나라도 참이면 true 값을 반환하는 변수를 선언.   
-if(inputId.equals(id) && isRightPass ) 에서 && 논리 연산자를 사용하여 두 개의 조건문이 모두 참인 경우에만 IF문의 코드를 실행하게 된다.
-논리연산자를 사용하면 조건식을 간결하게 만들어 코드에 대한 가독성이 좋아지고 유지, 보수가 원활해진다.

* 반복문
<pre><code>
public class LoopApp {
 
    public static void main(String[] args) {
         
        System.out.println(1);
        System.out.println("=== while ===");
        int i = 0;
        //..
        while(i < 3) {
            System.out.println(2);
            System.out.println(3);
            //i = i + 1;
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
</code></pre>
-'while'문에는 'iF'문처럼 'boolean' 타입의 조건식을 기입해야한다.   
-while 문을 해석하면 i < 3으로 i가 3보다 작으면 계속 반복시킨다.   
-'for'문은 사용자가 직접 반복횟수를 지정시킬 때 용이하다.   
-for(int j = 0; j < 3; j++) 구문을 해석하면 int j = 0; 으로 j 값을 초기화 시키고 j가 3이 되기 전까지 j에 1을 증가시킨다.   
-따라서 i++ 는 i = i + 1과 같다.
-'while'문은 자유도가 높고 'for'문은 사용자가 반복횟수를 지정할 수 있기에 자유도가 낮다.

* 배열
-배열은 반복문과 항상 함께한다.
<pre><code>
public class ArrayApp {
 
    public static void main(String[] args) {
         
        // egoing, jinhuck, youbin 
        //String users = "egoing, jinhuck, youbin";
        String[] users = new String[3];
        users[0] = "egoing";
        users[1] = "jinhuck";
        users[2] = "youbin";
         
        System.out.println(users[1]);
        System.out.println(users.length); // 배열의 크기 출력
         
        int[] scores = {10, 100, 100}; // 원소, element
        System.out.println(scores[1]);
        System.out.println(scores.length); // 배열의 크기 출력
    }
}
</code></pre>
-배열 선언 시 변수 타입명 뒤에 []를 입력하고 변수이름을 입력한다.   
-초기화를 할 경우 new 키워드를 이용하여 []안에 개수를 입력한다.   
-리터럴로 입력할 수 있는 데이터 타입은 {}안에 요소를 리터럴로 입력한다.   
-'배열'은 '인덱스'를 통해 접근하고 '인덱스'는 []안에 입력한다.   

* 반복문 + 배열
<pre><code>
public class LoopArray {
 
    public static void main(String[] args) {
        /*
         <li>egoing</li>
         <li>jinhuck</li>
         <li>youbin</li>
        */
         
        String[] users = new String[3];
        users[0] = "egoing";
        users[1] = "jinhuck";
        users[2] = "youbin";
         
        for(int i = 0; i < users.length; i++) {
            System.out.println(users[i]+",");
        }  
    }
}
</code></pre>
-위 코드중 for문을 해석하면 int i = 0;으로 초기화 시킨 뒤 i가 users.length. 즉, 배열의 요소 개수보다 작을때 반복하여 i값을 1씩 증가시킨다.   
-따라서 밑에 프린트문은 배열 값에 i 를 넣어 i가 1씩 증가할때마다 해당하는 배열의 문자열을 출력한다.
-조건식에서 length필드를 사용하게 되면 직접 배열의 요소 개수를 입력하지 않아도 되는 편리성을 가지게 된다.   

<2023-05-10 / JAVA 2 / 1 ~ 7.3 END>
-------------

<hr/>

< 2023-05-11 / JAVA 2 / 제어문 8 ~ 메소드 9 >
-------------

* 제어문 종합응용 1

<pre><code>
public class AuthApp3 {
 
    public static void main(String[] args) {
         
        String[] users = {"egoing", "jinhuck", "youbin"};
        String inputId = args[0];
         
        boolean isLogined = false;
        for(int i=0; i < users.length; i++) {
            String currentId = users[i];
            if(currentId.equals(inputId)) {
                isLogined = true;
                break;
                // break : 더 이상 현재 반복문을 진행하지 않고 빠져나오게 하는 구문.
            }
        }
        System.out.println("Hi,");
        if(isLogined) {
            System.out.println("Master!!");
        } else {
            System.out.println("Who are you?");
        }
    }
}
</code></pre>
-위 코드를 해석하면 처음부터 users 라는 문자열 형식의 데이터타입 배열에 값을 넣고, inputid 문자열을 선언하여 배열의 크기를 0으로 초기화 시켰다.   
-이후 boolean 형식의 isLogined 를 false로 선언하고, for문안에서 currentld 문자열 데이터를 선언하여 if문으로 inputid와 같을 시 동작을 시키는 코드를 만들었다.   

* 제어문 종합응용 2

-이차원 배열을 응용한 로그인 기능
<pre><code>
public class AuthApp3 {
 
    public static void main(String[] args) {
         
        //String[] users = {"egoing", "jinhuck", "youbin"};
        String[][] users = {
                {"egoing", "1111"},
                {"jinhuck", "2222"},
                {"youbin", "3333"}
        };
        String inputId = args[0];
        String inputPass = args[1];
         
        boolean isLogined = false;
        for(int i=0; i < users.length; i++) {
            String[] current = users[i];
            if(
                    current[0].equals(inputId) && 
                    current[1].equals(inputPass)
            ) {
                isLogined = true;
                break;
            }
        }
        System.out.println("Hi,");
        if(isLogined) {
            System.out.println("Master!!");
        } else {
            System.out.println("Who are you?");
        }
    }
}
</code></pre>
-위 코드는 이차원 배열을 이용하여 하나의 배열에 각각의 원소를 두개씩 넣었다.   
-이차원 배열을 구성하여 아이디와 비밀번호 모두 저장하는 방식의 로그인 기능을 구현한 코드이다.   
<pre><code>
if(current[0].equals(inputId) && current[1].equals(inputPass))
</code></pre>
-이 코드는 current 0번째 배열에 해당하는 값이 inputID에 지정된 값과 같고, current 1번째 배열에 해당하는 값이 inputPass에 지정된 값과 모두 같을 시 코드를 동작시킨다.   

* 메소드 - 이미 익숙한 메소드

<pre><code>
public class FirstMethod {
 
    public static void main(String[] args) {
         
        System.out.println("Hello Method");
        System.out.println(Math.floor(1.1));
    }
}
</code></pre>
-이미 사용했던 메소드 : equals, contains, Mathclass-floor, main(특수)   
-floor 메소드 : Math 클래스, double 형 자료형을 받아서 올림 연산을 수행하여 double 형으로 반환한다.   
-main 메소드 : 특수한 메소드로, 우리가 클래스를 실행할 때 어떠한 명령을 내리지 않아도 main 메소드를 실행한다.

* 메소드의 기본 형식

-메소드를 이용한다면 쉽게 같은 코드를 재사용하고, 유지보수를 쉽게 할 수 있다.   
<pre><code>
public class WhyMethod {
     
    public static void main(String[] args) {
         
        // 100000000
        printTwoTimesA();
        // 100000000
        printTwoTimesA();
        // 100000000
        printTwoTimesA();
 
    }
 
    public static void printTwoTimesA() {
        System.out.println("-");
        System.out.println("a");
        System.out.println("a");
    }
}
</code></pre>
-중간에 작업을하는 코드가 여러 줄 있을 때 일일이 우리가 직접 코드를 복사해서 넣지 않아도 메소드를 이용하여 코드를 재사용하여서 코드의 가독성을 높일 수 있다.   

* 메소드의 입력

<pre><code>
public class WhyMethod {
     
    public static void main(String[] args) {
         
                    //인자, argument
            printTwoTimes("a", "-");
            // 100000000
            printTwoTimes("a", "*");
            // 100000000
            printTwoTimes("a", "&");
            printTwoTimes("b", "!");
 
    }
                                    //매개변수,parameter 
    public static void printTwoTimes(String text, String delimiter) {
        System.out.println(delimiter);
        System.out.println(text);
        System.out.println(text);
    }
}
</code></pre>
-매개변수(파라미터)는 메소드 안에서 통용되는 변수, 메소드를 호출하고 실제 데이터값을 메소드의 파라미터 안에 넣게 될 때는 인자(아규먼트)라고 함.   
-main 메소드는 문자열 배열인 args파라미터를 이용함.   

* 메소드의 출력

<pre><code>
public class OutputMethod {
     
    public static String a() {
        // ... 
        return "a";
    }
     
    public static int one() {
        return 1;
        //...
    }
 
    public static void main(String[] args) {
 
        System.out.println(a());
        System.out.println(one());
    }
}
</code></pre>
-위 코드는 값을 반환하는 메소드를 이용한 코드이다.   
-a라는 메소드는 문자열 형식이므로 return "a";라고 작성한다.   
-one라는 메소드는 정수 형식이므로 return 1;라고 작성한다.   
-void는 return값이 없다.
<pre><code>
import java.io.FileWriter;
import java.io.IOException;

public class WhyMethod {

	public static void main(String[] args) throws IOException {
		String out = twoTimes("a", "-");
		System.out.println(out);
		FileWriter fw = new FileWriter("out.txt");
		fw.write(out);
		fw.close();
		System.out.println(twoTimes("a", "*"));
	}
	public static String twoTimes(String text, String delimiter) {
		String out = "";
		out = out + delimiter + "\n";
		out = out + text + "\n";
		out = out + text + "\n";
		return out;
	}
}
</code></pre>

* 메소드의 활용

<pre><code>
public class AccountingApp {

	public static void main(String[] args) {
		double valueOfSupply = 10000.0; // 공급가액
		double vatRate = 0.1; // 부가가치세율
		double vat = valueOfSupply * vatRate; // 부가세
		double total = valueOfSupply + vat; // 합계
		
		System.out.println("Value of supply : " + valueOfSupply);
		System.out.println("VAT : " + vat);
		System.out.println("Total : " + total);
	}
}
</code></pre>
-main 메소드 바깥으로 지역변수화 되어 있는 valueOfSupply와 vatRate, vat, total 변수들을 빼내어 전역변수화 시킨다.
<pre><code>
public class AccountingApp {
    public static double valueOfSupply = 10000.0; // 공급가액

    public static double vatRate = 0.1; // 부가가치세율
 
    public static double getVAT() {
        return valueOfSupply * vatRate; // 부가세
    }
     
    public static double getTotal() {
        return valueOfSupply + getVAT(); // 합계
    }
 
    public static void main(String[] args) {
 
        System.out.println("Value of supply : " + valueOfSupply);
        System.out.println("VAT : " + getVAT());
        System.out.println("Total : " + getTotal());
    }
}
</code></pre>
-위 코드에서 공급가와 부가가치세율은 모든 메소드에서 바로 접근할 수 있게 클래스이 static 필드로 빼내었다.   
-메소드 안에서 메소드를 호출할 수 있다.   
-메소드 내에서 return을 통해 main에서 메소드에 접근하고 출력할 수 있다.   
-메소드를 이요하면 재사용성이 높아진다.   

* 클래스, OOP

-클래스 : 비슷한 연관된 일을 하는 메소드와 변수들을 묶어 그룹으로 만든 것.   
-인스턴스 : 클래스를 틀로 하여 실제로 프로그램에서 동작하는 객체들.   
-위와 같은 클래스와 인스턴스 들과 같은 객체를 뼈대로 해서 프로그램을 만들어 가는 방식을 객체지향 프로그래밍(OOP, Object Oriented Programming)이라고 한다.   

* Access Level Modifiers

<pre><code>
public class AccessLevelModifiersMethod {

	private static void hi() {
		System.out.println("Hi");
	}
	public static void main(String[] args) {
		hi();
	}
}
-접근제어자 public의 자리에 public, protected, default, private 라는 값이 올 수 있다.   
-위 네개 모두 동작한다.   
-public = 모든 클래스에서 실행 된다. (웬만하면 public을 사용하면 된다.)   
-private = 같은 클래스 안에서만 사용할 수 있다.   
</code></pre>
<pre><code>
class Greeting {
	private static void hi() {
		System.out.println("Hi");
	}
}

public class AccessLevelModifiersMethod {

	public static void main(String[] args) {
		Greeting.hi();
	}
}
</code></pre>
-위 코드는 오류를 낸다.   
-이유 : hi는 Greeting 클래스 밖에서 직접 접근해서 사용할 수 없기 때문(private 제약조건)   

* Static

<pre><code>
class Print{
    public String delimiter;
    public void a() {
        System.out.println(this.delimiter);
        System.out.println("a");
        System.out.println("a");
    }
    public void b() {
        System.out.println(this.delimiter);
        System.out.println("b");
        System.out.println("b");
         
    }
    public static void c(String delimiter) {
        System.out.println(delimiter);
        System.out.println("b");
        System.out.println("b");
    }
}
public class staticMethod {
     
    public static void main(String[] args) {
//      Print.a("-");
//      Print.b("-");
         
        // instance
        Print t1 = new Print();
        t1.delimiter = "-";
        t1.a();
        t1.b();
        Print.c("$");
         
         
//      Print.a("*");
//      Print.b("*");
         
        Print t2 = new Print();
        t2.delimiter = "*";
        t2.a();
        t2.b();
    }
}
</code></pre>
-Static이란 키워드가 붙은 메소드는 클래스의 메소드다.   
-Static이란 키워드가 붙지 않은 메소드는 인스턴스의 메소드다.   
-this.delimiter = t1,2의 값으로 지정한 delimiter이다.   
-메소드가 인스턴스 소속일때는 static을 빼주어야 한다.   
-메소드가 클래스 소속일때는 static이 존재하여야 한다.   

< 2023-05-11 / JAVA 2 / 제어문 8 ~ 메소드 9 END >
-------------

<hr/>

< 2023-05-12 / JAVA 2 / 객체지향 프로그래밍 1 ~ 5 >
-------------

* 메소드와 절차적 프로그래밍

-메소드는 언어마다 메소드, 함수, 서브루틴, 프로시저라는 이름으로 불림.   
-이러한 메소드를 중심으로 프로그램을 만들어 나가는 프로그래밍을 절차적 프로그래밍이라고 함.   
-대표적 언어 : C언어   

* 클래스와 객체지향 프로그래밍

-객체지향 프로그래밍 : 변수와 메소드를 모은 수납상자와 같은 클래스를 이용하여 프로그램을 정돈시켜 프로그램의 구조를 만들어 가는 방식.   
-객체 지향 언어 : 위와 같은 방식은 언어차원에서 지원하는 프로그래밍 언어.   

* 남의 클래스, 남의 인스턴스

<pre><code>
import java.io.FileWriter;
import java.io.IOException;
 
public class OthersOOP {
 
    public static void main(String[] args) throws IOException {
        // class : System, Math, FileWriter
        // instance : f1, f2
         
        System.out.println(Math.PI);
        System.out.println(Math.floor(1.8));
        System.out.println(Math.ceil(1.8));
         
        FileWriter f1 = new FileWriter("data.txt");
        f1.write("Hello");
        f1.write(" Java");
         
         
        FileWriter f2 = new FileWriter("data2.txt");
        f2.write("Hello");
        f2.write(" Java2");
        f2.close();
         
        f1.write("!!!");
        f1.close();
    }
}
</code></pre>
-Math Class : 수학적 계산을 도와주는 여러 메소드를 포함.   
=> floor, ceil 메소드, 클래스 변수(PI)   
=> 자연상수 E, 삼각함수, 제곱, 로그, 절대값, 난수, 반올림 등의 기능들을 할 수 있는 여러 메소드와 변수 포함.   
=> 이러한 메소드와 변수는 인스턴스를 생성하지 않아도 클래스에서 직접 호출할 수 있다.   
-FileWriter class : 파일을 열고 원하는 내용을 입력할 수 있는 기능 제공.   
=> 각각의 파일에 해당하는 인스턴스를 생성하여 Write 메소드로 쓰기 작업을 수행하고 close 메소드로 파일을 닫는다.   
=> 이러한 메소드와 변수는 인스턴스를 생성하여 사용하여야 하고 클래스에서 직접 호출할 수 없다.   

* 변수와 메소드

<pre><code>
public class MyOOP {

	public static void main(String[] args) {
		String delimiter = "----";
		printA(delimiter);
		printA(delimiter);
		printB(delimiter);
		printB(delimiter);
		
		delimiter = "****";
		printA(delimiter);
		printA(delimiter);
		printB(delimiter);
		printB(delimiter);
	}

	public static void printA(String delimiter) {
		System.out.println(delimiter);
		System.out.println("A");
		System.out.println("A");
	}
	public static void printB(String delimiter) {
		System.out.println(delimiter);
		System.out.println("B");
		System.out.println("B");
	}
}
</code></pre>
-위 코드에서 String delimiter는 변수의 인자값을 바꾸는 변수선언이다.   
-메소드 안에서 정의된 변수는 메소드안에서만 사용할 수 있다.   
-이때 print 소속의 변수를 선언하면 아래 코드와 같다.
<pre><code>
class Print {
	public static String delimiter = "";
	public static void printA() {
		System.out.println(delimiter);
		System.out.println("A");
		System.out.println("A");
	}
	public static void printB() {
		System.out.println(delimiter);
		System.out.println("B");
		System.out.println("B");
	}
	public static void printAll() {
		printA();
		printA();
		printB();
		printB();
	}
}
public class MyOOP {
	
	public static void main(String[] args) {
		Print.delimiter = "----";
		Print.printAll();
		
		Print.delimiter = "****";
		Print.printAll();
	}	
}
</code></pre>

* 클래스의 존재 이유와 기본형식

-클래스의 장점 : 관련있는 변수들과 메소드를 묶어서 정리정돈을 할 수 있게 한다.   
-우리는 위 코드에서  PrintA(), PrintB() 식으로 프린트문을 실행했다. 이를 더 편하게 하려면 Print.A, Print.B 이런식으로 변경해주면 된다. 이는 Print에 속한 A라는 뜻이다.
=> Print.A 처럼 쓰면 굳이 메소드의 이름을 PrintA라고 적지 않고 A라고만 적어도 Print 객체의 A메소드이기 때문에 A를 출력한다는 의미를 쉽게 유추할 수 있다.   

* 클래스의 형식

-클래스는 한파일에 여러 개를 넣을 수 있지만 접근제어자 Public은 Java 파일과 같은 이름의 클래스에 하나만 붙일 수 있다.   
-소스 코드를 컴파일할 때 그 안에 들어 있는 클래스는 아래와 같이 따로따로 하나씩 class 파일로 만들어진다.   
<pre><code>
    MyOOP.class // 실행을 담당하는 main 메소드가 들어있는 MyOOP.class
    Print.class // 프로그램의 실질적인 액션을 담당하는 Print.class
(폴더)src
    MYOOP.java
</code></pre>
-따라서 한 파일안에 여러 클래스가 등장할 수 있지만 여러 클래스를 각각 하나의 java 파일로 만들게 되면 프로그램 기능별로 쪼개어 소스 코드를 별도 저장할 수 있다.   

* 인스턴스

-클래스 : 어떠한 형틀.   
-인스턴스 : 형틀로 찍어낸 실체.   
-객체를 인스턴스로 만들면 그 인스턴스를 바꾼다 하더라도 다른 인스턴스는 영향을 받지 않는다.   
-클래스를 복제하는 키워드 : "new"   
<pre><code>
class Print {
	public String delimiter = "";
	public void A() {
		System.out.println(delimiter);
		System.out.println("A");
		System.out.println("A");
	}
	public void B() {
		System.out.println(delimiter);
		System.out.println("B");
		System.out.println("B");
	}
}
public class MyOOP {
	
	public static void main(String[] args) {
		Print p1 = new Print();
		p1.delimiter = "----";
		Print p2 = new Print();
		p2.delimiter = "****";
		
		p1.A();
		p2.A();
		p1.B();
		p2.B();	
	}	
}
</code></pre>
-위 코드에서 A()와 B() 속에 있는 코드를 실행시킬려면, MyOOP 클래스의 main에서 Print 클래스를 객체화 시켜 p1,p2이라는 변수를 선언하고 이를 "new" 를 사용해 Print()를 복제한 복제본을 만들어서 각각의 복제본을 내부적으로 다른데이터(딜리버리)를 유지하게 하여 코드를 깔끔하고 중복을 제거하는 결과를 얻게되었다.   

< 2023-05-12 / JAVA 2 / 객체지향 프로그래밍 1 ~ 5 END >
-------------

<hr/>

< 2023-05-15 / JAVA 2 / 객체지향 프로그래밍 6 ~ 9 >
-------------

* static

-static 변수, 메소드는 클래스에서 생성된 모든 인스턴스가 공유하는 자원,   
인스턴스를 만들지 않고도 클래스에서 직접 호출할 수 있다.   
<pre><code>
class Foo{
    public static String classVar = "I class var";
    public String instanceVar = "I instance var";
    public static void classMethod() {
        System.out.println(classVar); // Ok
//      System.out.println(instanceVar); // Error
    }
    public void instanceMethod() {
        System.out.println(classVar); // Ok
        System.out.println(instanceVar); // Ok
    }
}
public class StaticApp {
 
    public static void main(String[] args) {
        System.out.println(Foo.classVar); // OK
//      System.out.println(Foo.instanceVar); // Error
        Foo.classMethod();
//      Foo.instanceMethod();
         
        Foo f1 = new Foo();
        Foo f2 = new Foo();
//      
        System.out.println(f1.classVar); // I class var
        System.out.println(f1.instanceVar); // I instance var
//      
        f1.classVar = "changed by f1";
        System.out.println(Foo.classVar); // changed by f1
        System.out.println(f2.classVar);  // changed by f1
//      
        f1.instanceVar = "changed by f1";
        System.out.println(f1.instanceVar); // changed by f1
        System.out.println(f2.instanceVar); // I instance var
    }
}
</code></pre>
-Class 메소드 안에서는 class변수는 접근이 가능하지만 instance변수는 접근이 불가능하다.   
-Instance 메소드 안에서는 class변수와 instance변수 모두 접근이 가능하다.   
-f1 인스턴스는 class를 원형으로 하기 때문에 class의 여러가지 멤버들을 복제한다.   
-만약 class에 값도 세팅되어 있다면 f1에서 그 값까지 복제가 된다.   
-따라서 class의 변수를 바꾸면 모든 인스턴스들의 변수의 값까지 바뀐다.   

* 생성자와 this

<pre><code>
class Print {
	public String delimiter = "";
	public Print(String delimiter) {
		this.delimiter = delimiter;
	}
	public void A() {
		System.out.println(this.delimiter);
		System.out.println("A");
		System.out.println("A");
	}
	public void B() {
		System.out.println(this.delimiter);
		System.out.println("B");
		System.out.println("B");
	}
}
public class MyOOP {
    public static void main(String[] args) {
        Print p1 = new Print("----");
        p1.A();
        p1.A();
        p1.B();
        p1.B();
 
        Print p2 = new Print("****");
        p2.A();
        p2.A();
        p2.B();
        p2.B();
         
         
        p1.A();
        p2.A();
        p1.A();
        p2.A();
    }
}
</code></pre>
-생성자는 초기에 주입할 필요가 있는 값을 전달하거나 초기에 작업을 수행할 때 사용한다   
-this란 클래스가 인스턴스화 되었을때 그 클래스의 인스턴스를 가리킨다.   

* 활용 (클래스화)

<pre><code>
class Accounting{
    public static double valueOfSupply;
    public static double vatRate = 0.1;
    public static double getVAT() {
        return valueOfSupply * vatRate;
    }
    public static double getTotal() {
        return valueOfSupply + getVAT();
    }
}
public class AccountingApp {
    public static void main(String[] args) {
        Accounting.valueOfSupply = 10000.0;
        System.out.println("Value of supply : " + Accounting.valueOfSupply);
        System.out.println("VAT : " + Accounting.getVAT());
        System.out.println("Total : " + Accounting.getTotal());
  
    }
}
</code></pre>
-위 코드는 부가가치세와 총 가격을 구하는 프로그램이다.   
-Accounting 클래스를 새로 정의하여 valueOfSupply, vatRate, getVAT, getTotal을 static 필드, 메소드로 구현한다.   
-AccountingApp이라는 클래스를 새로 만들어서 프린트문을 작성한다. 이때 내부 파라미터의 값은 본래 값을 가지고 있는 Accounting 클래스를 상속받는다.   

* 활용 (인스턴스화)

-위 코드에서는 클래스 하나만으로는 그 때마다 일일이 필드를 수정해야 하는 귀찮은 작업을 해야한다.   
-밑에 코드는 공급가액이 서로 다르고 번갈아 가면서 부가가치세와 총 가격을 구해서 출력해야 할 상황을 가정해서 인스턴스를 생성한 코드이다.   
<pre><code>
class Accounting{
    public double valueOfSupply;
    public static double vatRate = 0.1;
    public Accounting(double valueOfSupply) {
        this.valueOfSupply = valueOfSupply;
    }
    public double getVAT() {
        return valueOfSupply * vatRate;
    }
    public double getTotal() {
        return valueOfSupply + getVAT();
    }
}
public class AccountingApp {
    public static void main(String[] args) {
        Accounting a1 = new Accounting(10000.0);
         
        Accounting a2 = new Accounting(20000.0);
         
        System.out.println("Value of supply : " + a1.valueOfSupply);
        System.out.println("Value of supply : " + a2.valueOfSupply);
         
        System.out.println("VAT : " + a1.getVAT());
        System.out.println("VAT : " + a2.getVAT());
         
        System.out.println("Total : " + a1.getTotal());
        System.out.println("Total : " + a2.getTotal());
    }
}
</code></pre>
-AccountingApp에서 new를 통해 Accounting 클래스를 복제 하여 a1,a2라는 인스턴스를 만들고 값을 받을 수 있게했다.
-static은 클래스의 소속이기 때문에 valueOfSupply, getVAT, getTotal 는 static이 되면 안된다.   
-정리하면 static을 삭제처리해서 인스턴스화 하고 생성할때 초기화를 해야하기 때문에 생성자 세팅을 해줘야한다.   
-생성자가 호출될 때 인자를 매개변수로 전달하려면 Accounting 클래스에서 아래 코드처럼 선언해야 한다.    
<pre><code>
public Accounting(double valueOfSupply){
    this.valueOfSupply = valueOfSupply;
}
</code></pre>

* 상속과 인터페이스

-어떤 클래스와 비슷한 다른 것을 만들고 싶다면 어떻게 해야할까?   
=> 상속 : 어떤 클래스의 변수와 메소드를 모두 복사해서 만드는 방법.   
=> 인터페이스 : 일종의 규격, 클래스에 대한 규격을 선언하는 것.   

< 2023-05-15 / JAVA 2 / 객체지향 프로그래밍 6 ~ 9 END >
-------------

<hr/>

< 2023-05-16 / JAVA 2 / 상속 1 ~ 6 >
-------------

* 기능의 개선과 발전

<pre><code>
class Cal {
	public int sum(int v1, int v2) {
		return v1 + v2;
	}
}
class Cal3 extends Cal{
	public int minus(int v1, int v2) {
		return v1 - v2;
	}
}

public class InheritanceApp {

	public static void main(String[] args) {
		Cal c = new Cal();
		System.out.println(c.sum(2, 1));
		Cal3 c3 = new Cal3();
		System.out.println(c3.sum(2, 1));
		System.out.println(c3.minus(2, 1));
	}
}
</code></pre>
-위 코드는 부모클래스가 가지고 있지 않은 기능을 추가했으며, 부모클래스가 가진 기능이지만 더 보태서 재정의(override)했다.   

* Overriding, Overloading

<pre><code>
class Cal {
	public int sum(int v1, int v2) {
		return v1 + v2;
	}
	// Overloading
	public int sum(int v1, int v2, int v3) {
		return v1 + v2 + v3;
	}
}
</code></pre>
<pre><code>
class Cal {
	public int sum(int v1, int v2) {
		return v1 + v2;
	}
    public int sum(int v1, int v2, int v3) {
		return v1 + v2 + v3;
    }    
}
class Cal3 extends Cal{
	public int minus(int v1, int v2) {
		return v1 - v2;
	}
}

public class InheritanceApp {

	public static void main(String[] args) {
		Cal c = new Cal();
		System.out.println(c.sum(2, 1));
		Cal3 c3 = new Cal3();
		System.out.println(c3.sum(2, 1));
		System.out.println(c3.minus(2, 1));
	}
}
</code></pre>
-위 코드에서 오버로딩 동작을 하기위해 추가된 코드는 아래 코드와 같다.   
<pre><code>
public int sum(int v1, int v2, int v3) {
		return v1 + v2 + v3;
    }
</code></pre> 
-만약 파라미터의 값을 세개를 추가해주고 싶다면 그 값의 개수와 동일한 코드를 부모클래스에서 찾아서 출력할 것이다.   
-오버라이딩은 같은 클래스에서 이루어질 수 없고, 상속 관계를 가진 클래스 사이에서 이루어질 수 있다.   

* This, Super

-This : 인스턴스를 가리킴.   
-Super : 부모클래스를 가리킴.   
=> 자식 클래스에서 Super를 이용하여 접근 권한이 부여된 부모 클래스의 변수와 메소드에 접근할 수 있다.   
<pre><code>
class Cal {
	public int sum(int v1, int v2) {
		return v1 + v2;
	}
	// Overloading
	public int sum(int v1, int v2, int v3) {
		return this.sum(v1, v2) + v3;
	}
}
class Cal3 extends Cal{
	// Overriding
	public int sum(int v1, int v2) {
		System.out.println("Cal3!!!");
		return super.sum(v1, v2);
	}

	public int minus(int v1, int v2) {
		return v1 - v2;
	}
}
</code></pre>
-위 코드에서 Cal3에서 Cal의 변수와 메소드에 접근하기 위해서 Super를 이용하여 오버라이딩하는 메소드에서 기존의 작업 앞 뒤로 손쉽게 추가적인 작업을 추가하였다.   
-따라서 this는 자기자신, sum은 부모이다.   

* 상속과 생성자

<pre><code>
class Cal{
    int v1,v2;
    Cal(int v1, int v2){
        System.out.println("Cal init!!");
        this.v1 = v1; this.v2 = v2;
    }
    public int sum(){return this.v1+v2;}
}
class Cal3 extends Cal{
    Cal3(int v1, int v2) {
        super(v1, v2);
        System.out.println("Cal3 init!!");
    }
    public int minus(){return this.v1-v2;}
}
public class InheritanceApp {
    public static void main(String[] args) {
        Cal c = new Cal(2,1);
        Cal3 c3 = new Cal3(2, 1);
        System.out.println(c3.sum()); // 3
        System.out.println(c3.minus()); // 1
    }
}
</code></pre>
-상속받은 클래스의 생성자가 있다면 반드시 부모클래스의 생성자를 실행시키도록 강제하고 있다.   
-super = 부모클래스의 생성자.   
-만약 부모클래스에 기본 생성자가 아닌 인자를 주는 생성자만 명시된 경우 자식 클래스에서 생성자를 명시적으로 만들지 않는다면 컴파일이 되지 않는다.   

< 2023-05-16 / JAVA 2 / 상속 1 ~ 6 END >
-------------

<hr/>

< 2023-05-17 / JAVA 2 / 인터페이스 1 ~ 5 >
-------------

* 인터페이스

-규격을 지정한다.   
-메소드에서 implements 인터페이스시에 해당 메소드에서는 인터페이스의 규격 메소드가 생성된다.   
<pre><code>
interface Calculable {
	int sum(int v1, int v2);
}
class RealCal implements Calculable {

	public int sum(int v1, int v2) {
		return v1 + v2;
	}	
}
</code></pre>
-위 코드에서 interface로 Calculable을 만들고 내부에서 정수형 sum변수의 파라미터를 지정하였다.   

* 인터페이스의 형식

<pre><code>
interface Calculable {
	double PI = 3.14; // 변수를 초기화.
	int sum(int v1, int v2);
}
interface Printable {
	void print();
}
class RealCal implements Calculable, Printable {
// 하나의 클래스는 여러개의 인터페이스를 구현할 수 있다.
	public int sum(int v1, int v2) {
		return v1 + v2;
	}

	public void print() {
		System.out.println("this is RealCal!!!");
	}	
}

public class InterfaceApp {

	public static void main(String[] args) {
		RealCal c = new RealCal();
		System.out.println(c.sum(2, 1));
		c.print();
		System.out.println(c.PI);
	}
}
</code></pre>
-인터페이스의 이름은 대문자로 시작하고 형용사의 이름을 붙이기도 한다.   
-인터페이스는 클래스 여러개를 모두 적용할 수 있다.   
-인터페이스에는 변수를 정의할 수 있다.(변수는 반드시 초기화 되어야 한다.)   
-인터페이스를 적용한 클래스는 변수를 다시 대입할 수 없다.   

* 다형성

-다형성 : 객체의 타입이 부모 클래스, 인터페이스, 자식 클래스 등 여러 형태인데도 인스턴스로 만든 객체와 같이 행동하는 것.   
<pre><code>
interface Calculable {
	double PI = 3.14;
	int sum(int v1, int v2);
}
interface Printable {
	void print();
}
class RealCal implements Calculable, Printable {

	public int sum(int v1, int v2) {
		return v1 + v2;
	}

	public void print() {
		System.out.println("this is RealCal!!!");
	}	
}

public class InterfaceApp {

	public static void main(String[] args) {
		Calculable c = new RealCal();
		System.out.println(c.sum(2, 1));
		c.print(); // Compile Error
		System.out.println(c.PI);
	}
}
</code></pre>
-RealCal 인스턴스를 Calculable 타입으로 선언하면, Printable 메소드를 사용할 수 없다.   
-Printable 타입으로 선언하면, Calculable 메소드를 사용할 수 없다.
-어떤 클래스가 데이터타입을 무엇으로 하느냐에 따라서 다양한 얼굴을 가지게 된다.   

* 사용설명서 속의 인터페이스
-JAVA API속의 인터페이스   
<pre><code>
import java.io.FileWriter;
import java.io.IOException;
import java.io.Writer;

public class FileWriterApp {
	public static void main(String[] args) throws IOException {
		Writer fileWriter = new FileWriter("filewriter.txt");
		fileWriter.write("data 1");
		fileWriter.write("data 2");
		fileWriter.write("data 3");

		fileWriter.close();
	}
}
</code></pre>
-FileWriter 인스턴스는 초기화할 때 파일에 접근해서 파일을 점유하고 있다는 표시를 한다.   
-다 끝낸 후에는 close 메소드를 이용해서 현재 파일에 대한 점유를 끝낸다는 표시를 한다.   
-close 메소드는 AutoCloseable 인터페이스에 선언되어 있는 메소드다.   
-FileWriter와 같이 작업함에 있어서 복수의 접근을 막을 필요가 있는 경우에 AutoCloseable 인터페이스를 적용한다.   
-(https://docs.oracle.com/javase/8/docs/api/java/lang/AutoCloseable.html)   

< 2023-05-17 / JAVA 2 / 인터페이스 1 ~ 5 END >
-------------

<hr/>

< 2023-05-18 / JAVA 2 / 예외 1 ~ 9 >
-------------

* 예외의 발생

<pre><code>
public class ExceptionApp {
	public static void main(String[] args) throws ArithmeticException {
		System.out.println(1);
		System.out.println(2/0); // Run-Time Exception ArithmeticException
		System.out.println(3); 
	}
}
</code></pre>
-자바는 숫자를 0으로 나누는 경우 예외로 처리한다.   
-실제 실행을 시켜보면 ArithmeticException이라고 알려주고, 0으로 나누었다는 설명도 나오게 된다.   
-예외가 발생하는 이유는 프로그램이 실행하는 동안, 프로그램을 만들 사람들이 설계한 모양대로 운영되지 않았기 때문이다.   

* 예외의 처리

<pre><code>
public class ExceptionApp {
	public static void main(String[] args) throws ArithmeticException {
		System.out.println(1);
		int[] scores = {10, 20, 30};

		try {
			System.out.println(2);
			System.out.println(scores[3]); //ArrayIndexOutOfBoundsException
			// 여기까지 실행 -> catch(ArrayIndexOutOfBoundsException e)문으로 이동
			System.out.println(3);
			System.out.println(2/0); //ArithmeticException
			System.out.println(4);
		} catch(ArithmeticException e) {
			System.out.println("잘못된 계산이네요.");
		} catch(ArrayIndexOutOfBoundsException e) {
			System.out.println("없는 값을 찾고 계시네요 ^^");
		}		
		System.out.println(5); 
	}
}
</code></pre>
-위 코드는 try catch문을 이용하여 예외를 처리하여 이상한 경우에도 끝까지 실행되는 튼튼한 프로그램이다.
-try catch 구문을 사용하면 프로그램이 유연하게 흘러간다.   
-ArrayIndexOutOfBoundsException 는 배열의 없는값을 가져올려고 할때 실행된다.   

* 예외의 우선순위
 
<pre><code>
public class ExceptionApp {
	public static void main(String[] args) throws ArithmeticException {
		System.out.println(1);
		int[] scores = {10, 20, 30};

		try {
			System.out.println(2);
			System.out.println(scores[3]); //ArrayIndexOutOfBoundsException
			System.out.println(3);
			System.out.println(2/0); //ArithmeticException
			System.out.println(4);
		} catch (ArithmeticException e) {
			System.out.println("계산이 잘못된 것 같아요.");
		} catch (Exception e) {
			System.out.println("뭔가 이상합니다. 오류가 발생했습니다. ");
		}	
		System.out.println(5); 
	}
}
</code></pre>
-ArithmeticException은 RuntimeException으로부터 상속받은 클래스.   
-또한 RuntimeException은 Exception 클래스로부터 상속받은 클래스.   
-여러 예외가 있더라도 Exception클래스를 이용해서 포괄적으로 처리 가능.   
-catch문의 위치가 중요하다.   
-try문에서 발생한 예외는 여러 개의 catch문을 순서대로 거쳐서 하나씩 확인한다.   

* Exception 변수 e

-catch문의 변수 e는 인스턴스.   
-예외들의 인스턴스에는 예외가 발생한 원인, 어디서 발생했는지에 대한 정보들이 들어 있다.   
<pre><code>
catch (ArithmeticException e) {
	System.out.println("계산이 잘못된 것 같아요."e.getMessage());
}
</code></pre>
-getMessage 메소드를 이용하면 예외 상황에 대한 자세한 정보를 얻을 수 있다.   

* Checked Exception vs Unchecked Exception

-ArithmeticException, ArrayIndexOutOfBoundsException 같은 경우 는 try catch 문으로 잡아내지 않아서 프로그램이 뻗어도 컴파일해서 실행할 수 있었다. 이런 예외들을 Unchecked Exception라고 부른다.   
-try catch문 으로 잡아내지 않으면 프로그램이 컴파일 되지 않는 예외들을 Checked Exception라고 부른다.   
<pre><code>
import java.io.FileWriter;
import java.io.IOException;

public class CheckedExceptionApp {

	public static void main(String[] args) {
		try {
			FileWriter f = new FileWriter("data.txt");
			f.write("Hello");
			f.close();
		} catch(IOException e) {
			e.printStackTrace();
		}
	}
}
</code></pre>
-IOException을 처리하지 않으면 컴파일이 되지 않는다.   

* Finally, Resource

-대표적인 Resource : 파일, 네트워크, 데이터베이스   
=> 우리의 프로그램만을 위해 존재하지 않음.   
=> 파일의 경우 점유상태를 나타내기도 하고, 네트워크나 데이터베이스는 연결 상태를 유지한다. 그리고 우리가 필요한 작업을 끝내고 나서는 자원을 놓아주는 작업을 한다.   

-Finally : 자원을 놓아주는 작업을 try문에 넣게 되면 예외가 발생했을 때 자원을 놓아주는 작업을 하지 못한다. 그래서 자원을 일단 잡았으면 놓아주는 작업을 실행해야 하는데 이때 사용하는 형식이 Finally문이다.   
<pre><code>
import java.io.FileWriter;
import java.io.IOException;

public class CheckedExceptionApp {

	public static void main(String[] args) {
		FileWriter f = null;
		try {
			f = new FileWriter("data.txt");
			f.write("Hello");
			// close를 하기 전에 예외가 발생한다면 close가 실행되지 않음
			// f.close();
		} catch(IOException e) {
			e.printStackTrace();
		} finally {
			if (f != null) {
				try {
					f.close();
				} catch (IOException e) {
					e.printStackTrace();
				}
			}			
		}
	}
}
</code></pre>
-null : 값이 없다.   
-위 코드를 해석하면 만약 f가 null이 아니라면 close를 실행해라.   
-close()도 IOexception이 일어날 수 있으므로 catch에 처리해주어야 한다.   

* Try-with-Resource

-try-with-resource 문을 이용하여 자원관리를 훨씬 단순하게 할 수 있다.   
-클래스가 AutoCloseable 인터페이스를 상속한다면 try-with-resource 문에 사용할 수 있다.   
<pre><code>
import java.io.FileWriter;
import java.io.IOException;

public class TryWithResource {

	public static void main(String[] args) {
		try (FileWriter f = new FileWriter("data.txt")) {
			f.write("Hello");
		} catch (IOException e) {
			e.printStackTrace();
		}
	}
}
</code></pre>
-이전 코드는 try catch finally 문으로 매우 복잡했지만, 이번 코드는 try-with-resource문을 사용하여 코드의 가독성을 높혔다.   
-특징으로는 try문에 괄호를 추가하여 사용할 자원을 정의한다.   
=> 객체를 여러개 선언할 수 있고 세미콜론으로 구별한다.   
=> 객체의 정의 가장 마지막에는 세미콜론을 넣지 않는다.   
=> 전체 try문이 종료되면 생성된 인스턴스는 자동으로 종료되기 때문에 명시적으로 close를 이용하여 자원을 놓아주지 않는다.   
-자바는 내부적으로 f.close를 수행한다.   

< 2023-05-18 / JAVA 2 / 예외 1 ~ 9 END >
-------------

<hr/>

< 2023-07-10 ~ 07-13 / 스프링 입문 - 섹션1 ~ 섹션 5 >
-------------

* 정적 컨텐츠
<pre><code>
<*!DOCTYPE HTML>
<*html>
<*head>
    <*title>static content</title>
    <*meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
<*/head>
<*body>
정적 컨텐츠 입니다.
<*/body>
<*/html>
</code></pre>

* MVC
<pre><code>
package hello.hellospring.controller;

import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RequestParam;

@Controller
public class HelloController {

    @GetMapping("Hello")
    public String hello(Model model){
        model.addAttribute("data","Hello");
        return "hello";
    }

    @GetMapping("hello-mvc")
    public String helloMvc(@RequestParam("name") String name, Model model){
        model.addAttribute("name",name);
        return "hello-template";
    }

}
</code></pre>
- 

* API
<pre><code>
package hello.hellospring.controller;

import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.bind.annotation.ResponseBody;

@Controller
public class HelloController {

    @GetMapping("Hello")
    public String hello(Model model){
        model.addAttribute("data","Hello");
        return "hello";
    }

    @GetMapping("hello-mvc")
    public String helloMvc(@RequestParam("name") String name, Model model){
        model.addAttribute("name",name);
        return "hello-template";
    }

    @GetMapping("hello-string")
    @ResponseBody
    public String helloString(@RequestParam("name") String name){
        return "Hello " + name; // hello spring
    }

    //API - json 방식 HTML출력
    @GetMapping("hello-api")
    @ResponseBody
    public Hello helloApi(@RequestParam("name") String name){
        Hello hello = new Hello();
        hello.setName(name);
        return hello;
    }

    static class Hello{
        private String name;

        public String getName(){
            return name;
        }

        public void setName(String name){
            this.name = name;
        }
    }

}
</code></pre>
- @ResponseBody 사용원리
- HTTP의 Body에 문자 내용을 직접 변환.
- 'viewResolver' 대신에 'HttpMessageConverter'동작.
- 기본 문자처리 : 'StringHttpMessageConverter'
- 기본 객체처리 : 'MappingJackson2HttpMessageConverter'
- byte 처리 등등 여러 HttpMessageConverter가 기본으로 등록되어 있음.

* 회원 관리 예제 - 백앤드 개발

- 일반적인 웹 애플리케이션 계층
- 컨트롤러 : 웹 MVC의 컨트롤러 역할
- 서비스 : 핵심 비즈니스 로직 구현
- 리포지토리 : 데이터베이스에 접근, 도메인 객체를 DB에 저장하고 관리
- 도메인 : 비즈니스 도메인 객체, 예) 회원, 주문, 쿠폰 등등 주로 데이터베이스에 저장하고 관리됨.

* 테스트코드
- 테스트 코드는 개발자들에게 있어서 없어선 안되는 기능중 하나.
- 개인으로 할때는 상관없지만 단체로 프로젝트를 진행할 때 오류를 줄이기 위해 미리 개인 코드를 테스트 해보는 용도로 사용.

* 회원 관리 예제 - Domain
<pre><code>
package hello.hellospring.domain;

public class Member {

    private Long id;
    private String name;

    public Long getId() {
        return id;
    }

    public void setId(Long id) {
        this.id = id;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }
}
</code></pre>
- getter, setter 단축키 숙지

* 회원 관리 예제 - Controller
<pre><code>
//HelloController
package hello.hellospring.controller;

import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.bind.annotation.ResponseBody;

@Controller
public class HelloController {

    @GetMapping("Hello")
    public String hello(Model model){
        model.addAttribute("data","Hello");
        return "hello";
    }

    @GetMapping("hello-mvc")
    public String helloMvc(@RequestParam("name") String name, Model model){
        model.addAttribute("name",name);
        return "hello-template";
    }

    @GetMapping("hello-string")
    @ResponseBody
    public String helloString(@RequestParam("name") String name){
        return "Hello " + name; // hello spring
    }

    //API
    @GetMapping("hello-api")
    @ResponseBody
    public Hello helloApi(@RequestParam("name") String name){
        Hello hello = new Hello();
        hello.setName(name);
        return hello;
    }

    static class Hello{
        private String name;

        public String getName(){
            return name;
        }

        public void setName(String name){
            this.name = name;
        }
    }
}
</code></pre>
<pre><code>
//MemberController
package hello.hellospring.controller;

import hello.hellospring.service.MemberService;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Controller;

@Controller
public class MemberController {

    private final MemberService memberService;

    @Autowired
    public MemberController(MemberService memberService) {
        this.memberService = memberService;
    }
}
</code></pre>

* 회원 관리 예제 - Repository
<pre><code>
//INTERFACE
package hello.hellospring.repository;

import hello.hellospring.domain.Member;

import java.util.List;
import java.util.Optional;

public interface MemberRepository {
    Member save(Member member);
    Optional<Member> findById(Long id);
    Optional<Member> findByName(String name);
    List<Member> findAll();
}
</code></pre>
<pre><code>
package hello.hellospring.repository;

import hello.hellospring.domain.Member;
import org.springframework.stereotype.Repository;

import java.util.*;

@Repository
public class MemoryMemberRepository implements MemberRepository {

    private static Map<Long, Member> store = new HashMap<>();
    private static long sequence = 0L;

    @Override
    public Member save(Member member) {
        member.setId(++sequence);
        store.put(member.getId(), member);
        return member;
    }

    @Override
    public Optional<Member> findById(Long id) {
        return Optional.ofNullable(store.get(id));
    }

    @Override
    public Optional<Member> findByName(String name) {
        return store.values().stream()
               .filter(member -> member.getName().equals(name))
               .findAny();
    }

    @Override
    public List<Member> findAll() {
        return new ArrayList<>(store.values());
    }

    public void clearStore(){
        store.clear();
    }
}
</code></pre>

* 회원 관리 예제 - Service
<pre><code>
package hello.hellospring.service;

import hello.hellospring.domain.Member;
import hello.hellospring.repository.MemberRepository;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Service;

import java.util.List;
import java.util.Optional;

@Service
public class MemberService {

    private final MemberRepository memberRepository;

    @Autowired
    public MemberService(MemberRepository memberRepository) {
        this.memberRepository = memberRepository;
    }


    /**
     *회원가입
     */
    public Long join(Member member){
        validateDuplicateMember(member); // 중복 회원 검증
        memberRepository.save(member);
        return member.getId();
    }

    private void validateDuplicateMember(Member member) {
        memberRepository.findByName(member.getName())
                .ifPresent(member1 -> {
                    throw new IllegalStateException("이미 존재하는 회원입니다.");
                });
    }

    /**
     * 전체회원 조회
     */
    public List<Member> findMembers(){
        return memberRepository.findAll();
    }

    public Optional<Member> findOne(Long memberId){
        return memberRepository.findById(memberId);
    }
}
</code></pre>
- join을 통해서 멤버함수에 접근하고 .getId()를 통해 중복회원인지 아닌지 검증한다.
- 이후 vaildateDuplicateMember객체에서 getId()에 들어간 회원정보를 찾고 만약 회원정보가 같다면 "이미 존재하는 회원입니다."라는 문구를 출력한다.

* 스프링 빈 실행방법 1 : 컴포넌트 스캔, 자동 의존관계 설정
<pre><code>
@Component // 애노테이션이 있으면 스프링 빈으로 자동 등록된다.
@Controller // 컨트롤러가 스프링 빈으로 자동 등록된 이유도 컴포턴트 스캔 때문.
</code></pre>
- 스프링 빈 : 스프링 컨테이너에 의해 관리되는 재사용 가능한 소프트웨어 컴포넌트, 스프링 컨테이너가 관리하는 자바 객체를 뜻함.
- 빈(Bean) : 인스턴스화된 객체
- `@Component`를 포함하는 다음 애노테이션도 스프링 빈으로 자동 등록 됨.
- `@Controller`
- `@Service`
- `@Repsitory`

* 스프링 빈 실행방법 2 : 자바 코드로 직접 스프링 빈 등록하기
<pre><code>
package hello.hellospring;

import hello.hellospring.domain.Member;
import hello.hellospring.repository.MemberRepository;
import hello.hellospring.repository.MemoryMemberRepository;
import hello.hellospring.service.MemberService;
import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;

@Configuration
public class SpringConfig {

    @Bean
    public MemberService memberService(){
        return new MemberService(memberRepository());
    }

    @Bean
    public MemberRepository memberRepository() {
        return new MemoryMemberRepository();
    }
}
</code></pre>
- 위 코드에서 @Bean을 선언하여 스프링 빈 컨테이너에 public MemberService memberService(), public MemberRepository memberRepository() 를 올려준다.
- 컨트롤러는 스프링이 관리하는 코드이기 때문에 컴포넌트 스캔으로 올라가며, 컴포넌트 스캔이기 때문에 오토와이어로 유지해도 된다.

- 참고 ) DI에는 필드, setter 주입, 생성자 주입 이렇게 3가지 방법이 있다. 의존관계가 실해중에 동적으로 변하는 경우는 거의 없으므로 생성자 주입을 권장한다.
- 참고 ) 실무에서는 주로 정형화된 컨트롤러, 서비스, 리포지토리 같은 코드는 컴포넌트 스캔을 사용한다. 그리고 정형화 되지 않거나, 상황에 따라 구현 클래스를 변경해야 하면 설정을 통해 스프링 빈으로 등록한다.

- 주의 ) `@Autowired`를 통한 DI는 `helloController`, `MemberService`등과 같이 스프링이 관리하는 객체에서만 동작한다. 스프링 빈으로 등록하지 않고 내가 직접 생성한 객체에서는 동작하지 않는다.

* 회원 관리 예제 - 웹 MVC 개발
* 회원 웹 기능 - 홈 화면 추가
<pre><code>
// Controller
package hello.hellospring.controller;

import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.GetMapping;

@Controller
public class HomeController {

    @GetMapping("/")
    public String home() {
        return "home";
    }
}
</code></pre>
- HomeController 클래스를 생성하고 리턴값으로 home을 출력한다.

<pre><code>
// HTML
<*!DOCTYPE html>
<*html xmlns:th="http://www.thymeleaf.org">
<*body>

<*div class="container">
  <*div>
    <*h1>Hello Spring<*/h1>
    <*p>회원 기능<*/p>
    <*p>
      <*a href="/members/new">회원 가입<*/a>
      <*a href="/members">회원 목록<*/a>
    <*/p>
  <*/div>
<*/div>

<*/body>
<*/html>
</code></pre>
- 코드 작성 후 localhost:8080 에 접속.
- 아래는 결과.
<!DOCTYPE html>
<html xmlns:th="http://www.thymeleaf.org">
<body>

<div class="container">
  <div>
    <h1>Hello Spring</h1>
    <p>회원 기능</p>
    <p>
      <a href="/members/new">회원 가입</a>
      <a href="/members">회원 목록</a>
    </p>
  </div>
</div>

</body>
</html>
-------------------------------------------
* 회원 웹 기능 - 등록
<pre><code>
//MemberController

package hello.hellospring.controller;

import hello.hellospring.service.MemberService;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.GetMapping;

@Controller
public class MemberController {

    private final MemberService memberService;

    @Autowired
    public MemberController(MemberService memberService) {
        this.memberService = memberService;
    }

    @GetMapping("/members/new")
    public String createForm() {
        return "members/createMemberForm";
    }
}
</code></pre>  

- MemberController 클래스 에 @GetMapping("/members/new")를 추가.
<pre><code>
<*!DOCTYPE html>
<*html xmlns:th="http://www.thymeleaf.org">
<*body>

<*div class="contrainer">
  <*form action="/members/new" method="post">
    <*div class="form-group">
      <*label for="name">이름<*/label>
      <*input type="text" id="name" name="name"  placeholder="이름을 입력하세요">
    <*/div>
    <*button type="submit">등록<*/button>
  <*/form>

<*/div>

<*/body>
<*/html>
</code></pre>
- <*form>은 값을 입력할 수 있는 구간
- 아래는 결과.
<!DOCTYPE html>
<html xmlns:th="http://www.thymeleaf.org">
<body>

<div class="contrainer">
  <form action="/members/new" method="post">
    <div class="form-group">
      <label for="name">이름</label>
      <input type="text" id="name" name="name" placeholder="이름을 입력하세요">
    </div>
    <button type="submit">등록</button>
  </form>

</div>

</body>
</html>
-------------------------------------------
<pre><code>
@MemberController

package hello.hellospring.controller;

import hello.hellospring.domain.Member;
import hello.hellospring.service.MemberService;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.PostMapping;

@Controller
public class MemberController {

    private final MemberService memberService;

    @Autowired
    public MemberController(MemberService memberService) {
        this.memberService = memberService;
    }

    @GetMapping("/members/new")
    public String createForm() {
        return "members/createMemberForm"; // createMemberForm으로 이동한다.
    }

    @PostMapping("/members/new")
    public String create(MemberForm form){
        Member member = new Member();
        member.setName(form.getName());

        memberService.join(member);

        return "redirect:/"; // 회원가입이 끝나면 홈 화면으로 돌려보냄.
    }
}
</code></pre>

- `@PostMapping(/members/new)`은 데이터를 form에 넣어서 전달할 때 사용한다.
- 위에서 method를 "post"로 지정했기 때문에 데이터를 등록할 때 `@PostMapping`이 사용된다.

* 회원 웹 기능 - 조회
<pre><code>
//MemberController

import java.util.List;

@Controller
public class MemberController {

    private final MemberService memberService;

    @Autowired
    public MemberController(MemberService memberService) {
        this.memberService = memberService;
    }

    @GetMapping("/members/new")
    public String createForm() {
        return "members/createMemberForm";
    }

    @PostMapping("/members/new")
    public String create(MemberForm form){
        Member member = new Member();
        member.setName(form.getName());

        memberService.join(member);

        return "redirect:/"; // 회원가입이 끝나면 홈 화면으로 돌려보냄.
    }

    @GetMapping("/members")
    public String List(Model model){
        List<Member> members = memberService.findMembers();
        model.addAttribute("members", members);
        return "members/memberList";
    }
}
</code></pre>
- 회원조회를 위해 `@GetMapping("/members")`로 매핑하여 memberList라는 페이지로 이동할 수 있도록 리턴값을 설정한다.
<pre><code>
//HTML
<*!DOCTYPE HTML>
<*html xmlns:t="http://www.thymeleaf.org">
<*body>
<*div class="contrainer">
    <*div>
        <*table>
            <*thead>
            <*tr>
                <*th>#<*/th>
                <*th>이름<*/th>
            <*/tr>
            <*/thead>
            <*tbody>
            <*tr th:each="member : ${members}">
                <*td th:text="${member.id}"><*/td>
                <*td th:text="${member.name}"><*/td>
            <*/tr>
            <*/tbody>
        <*/table>
    <*/div>
<*/div>

<*/body>
<*/html>
</code></pre>
- return값으로 받았던 memberList를 HTML로 구현한다.
- 아래는 결과.
<!DOCTYPE HTML>
<html xmlns:t="http://www.thymeleaf.org">
<body>
<div class="contrainer">
    <div>
        <table>
            <thead>
            <tr>
                <th>#</th>
                <th>이름</th>
            </tr>
            </thead>
            <tbody>
            <tr th:each="member : ${members}">
                <td th:text="${member.id}"></td>
                <td th:text="${member.name}"></td>
            </tr>
            </tbody>
        </table>
    </div>
</div>

</body>
</html>
--------------------------------

- 만약 자바를 실행 중지하고 다시 실행하게 되면 데이터가 다 사라지므로 주의 해야한다.

< 2023-07-10 ~ 07-13 / 스프링 입문 - 섹션1 ~ 섹션 5 END >
-------------

<hr/>

< 2023-07-14 / 스프링 입문 - 섹션 6 >
-------------

* h2데이터베이스 설치, 실행
- 설치 : https://www.h2database.com/
- 실행 : h2.bat
- 데이터베이스 파일 생성 :
1. `jdbc:h2:~/test`
2. `~/test.mv.db` 생성 확인
3. 이후, `jdbc:h2:tcp://localhost/~/test` 접속.

- 테이블 관리를 위해 프로젝트 루트에 `sql/ddl.sql` 파일 생성
<pre><code>
drop table if exists member CASCADE;

create table member
(
    id bigint generated by default as identity,
    name varchar(255),
    primary key (id)
);
</code></pre>

* 순수 Jdbc
- build.gradle 파일에 jdbc,h2 데이터베이스 관련 라이브러리 추가.
<pre><code>
implementation 'org.springframework.boot:spring-boot-starter-jdbc'
runtimeOnly 'com.h2database:h2'
</code></pre>
- 스프링 부트 데이터 베이스 연결 설정 추가 `resources/application.properties`
<pre><code>
spring.datasource.url=jdbc:h2:tcp://localhost/~/test
spring.datasource.driver-class-name=org.h2.Driver
spring.datasource.username=sa
</code></pre>

- Jdbc 회원 리포지토리
<pre><code>
// JdbcMemberRepository

package hello.hellospring.repository;
import hello.hellospring.domain.Member;
import org.springframework.jdbc.datasource.DataSourceUtils;
import javax.sql.DataSource;
import java.sql.*;
import java.util.ArrayList;
import java.util.List;
import java.util.Optional;

public class JdbcMemberRepository implements MemberRepository {

    private final DataSource dataSource;

    public JdbcMemberRepository(DataSource dataSource) {
        this.dataSource = dataSource;
    }

    @Override
    public Member save(Member member) {
        String sql = "insert into member(name) values(?)";

        Connection conn = null;
        PreparedStatement pstmt = null;
        ResultSet rs = null;

        try {
            conn = getConnection();
            pstmt = conn.prepareStatement(sql,
                    Statement.RETURN_GENERATED_KEYS);

            pstmt.setString(1, member.getName());

            pstmt.executeUpdate();
            rs = pstmt.getGeneratedKeys();

            if (rs.next()) {
                member.setId(rs.getLong(1));
            } else {
                throw new SQLException("id 조회 실패");
            }
            return member;
        } catch (Exception e) {
            throw new IllegalStateException(e);
        } finally {
            close(conn, pstmt, rs);
        }
    }

    @Override
    public Optional<Member> findById(Long id) {
        String sql = "select * from member where id = ?";

        Connection conn = null;
        PreparedStatement pstmt = null;
        ResultSet rs = null;
        try {
            conn = getConnection();
            pstmt = conn.prepareStatement(sql);
            pstmt.setLong(1, id);

            rs = pstmt.executeQuery();

            if (rs.next()) {
                Member member = new Member();
                member.setId(rs.getLong("id"));
                member.setName(rs.getString("name"));
                return Optional.of(member);
            } else {
                return Optional.empty();
            }
        } catch (Exception e) {
            throw new IllegalStateException(e);
        } finally {
            close(conn, pstmt, rs);
        }
    }

    @Override
    public List<Member> findAll() {
        String sql = "select * from member";
        Connection conn = null;
        PreparedStatement pstmt = null;
        ResultSet rs = null;
        try {
            conn = getConnection();
            pstmt = conn.prepareStatement(sql);
            rs = pstmt.executeQuery();

            List<Member> members = new ArrayList<>();

            while (rs.next()) {
                Member member = new Member();
                member.setId(rs.getLong("id"));
                member.setName(rs.getString("name"));
                members.add(member);
            }

            return members;

        } catch (Exception e) {
            throw new IllegalStateException(e);
        } finally {
            close(conn, pstmt, rs);
        }
    }

    @Override
    public Optional<Member> findByName(String name) {
        String sql = "select * from member where name = ?";
        Connection conn = null;
        PreparedStatement pstmt = null;
        ResultSet rs = null;
        try {
            conn = getConnection();
            pstmt = conn.prepareStatement(sql);
            pstmt.setString(1, name);
            rs = pstmt.executeQuery();
            if (rs.next()) {
                Member member = new Member();
                member.setId(rs.getLong("id"));
                member.setName(rs.getString("name"));
                return Optional.of(member);
            }
            return Optional.empty();
        } catch (Exception e) {
            throw new IllegalStateException(e);
        } finally {
            close(conn, pstmt, rs);
        }
    }

    private Connection getConnection() {
        return DataSourceUtils.getConnection(dataSource);
    }

    private void close(Connection conn, PreparedStatement pstmt, ResultSet rs) {
        try {
            if (rs != null) {
                rs.close();
            }
        } catch (SQLException e) {
            e.printStackTrace();
        }
        try {
            if (pstmt != null) {
                pstmt.close();
            }
        } catch (SQLException e) {
            e.printStackTrace();
        }
        try {
            if (conn != null) {
                close(conn);
            }
        } catch (SQLException e) {
            e.printStackTrace();
        }
    }

    private void close(Connection conn) throws SQLException {
        DataSourceUtils.releaseConnection(conn, dataSource);
    }
}
</code></pre>

- 스프링 설정 변경
<pre><code>
package hello.hellospring;

import hello.hellospring.repository.JdbcMemberRepository;
import hello.hellospring.repository.JdbcTemplateMemberRepository;
import hello.hellospring.repository.MemberRepository;
import hello.hellospring.repository.MemoryMemberRepository;
import hello.hellospring.service.MemberService;
import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;

import javax.sql.DataSource;

@Configuration
public class SpringConfig {
    private final DataSource dataSource;
    public SpringConfig(DataSource dataSource) {
        this.dataSource = dataSource;
    }

    @Bean
    public MemberService memberService() {
        return new MemberService(memberRepository());
    }

    @Bean
    public MemberRepository memberRepository() {
        // return new MemoryMemberRepository();
        return new JdbcMemberRepository(dataSource);
    }
}
</code></pre>
- 스프링 부트는 데이터베이스 커넥션 정보를 바탕으로 DataSource를 생성하고 스프링 빈으로 만들어둔다. 그래서 DI를 받을 수 있다.
- 스프링의 DI (Dependencies Injection)을 사용하면 기존 코드를 전혀 손대지 않고, 설정만으로 구현클래스를 변경할 수 있다.
- 회원을 등록하고 DB에 결과가 잘 입력되는지 확인하자.
- 데이터를 DB에 저장하므로 스프링 서버를 다시 실행해도 데이터가 안전하게 저장된다.

* 스프링 통합 테스트
<pre><code>
package hello.hellospring.service;

import hello.hellospring.domain.Member;
import hello.hellospring.repository.MemberRepository;
import hello.hellospring.repository.MemoryMemberRepository;
import org.assertj.core.api.Assertions;
import org.junit.jupiter.api.AfterEach;
import org.junit.jupiter.api.BeforeEach;
import org.junit.jupiter.api.Test;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.boot.test.context.SpringBootTest;
import org.springframework.test.annotation.Commit;
import org.springframework.transaction.annotation.Transactional;

import static org.assertj.core.api.Assertions.assertThat;
import static org.junit.jupiter.api.Assertions.assertThrows;

@SpringBootTest
@Transactional
class MemberServiceIntegrationTest {

    @Autowired MemberService memberService;
    @Autowired MemberRepository memberRepository;

    @Test
    @Commit
    void 회원가입() {
        //given
        Member member = new Member();
        member.setName("spring100");

        //when
        Long saveId = memberService.join(member);

        //then
        Member findMember = memberService.findOne(saveId).get();
        Assertions.assertThat(member.getName()).isEqualTo(findMember.getName());
    }

    @Test
    public void 중복_회원_예외() {
        //given
        Member member1 = new Member();
        member1.setName("spring");

        Member member2 = new Member();
        member2.setName("spring");

        //when
        memberService.join(member1);
        IllegalStateException e = assertThrows(IllegalStateException.class, () -> memberService.join(member2));

        assertThat(e.getMessage()).isEqualTo("이미 존재하는 회원입니다.");
        //then

    }
}
</code></pre>
- `@SpringBootTest` :  스프링 컨테이너와 테스트를 함께 실행한다.
- `@Transactional` : 테스트 케이스에 이 애노테이션이 있으면, 테스트 시작 전에 트랜잭션을 시작하고, 테스트 완료 후에 항상 롤백한다. (DB에 데이터가 남지 않아 다음 테스트에 영향을 주지 않음.)

* 스프링 JdbcTemplate

- 순수 Jdbc와 동일한 환경설정진행
- 스프링 JdbcTemplate 라이브러리는 JDBC API에서 반복 코드를 대부분 제거해주지만 SQL은 직접 작성해야함.
<pre><code>
package hello.hellospring.repository;

import hello.hellospring.domain.Member;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.jdbc.core.JdbcTemplate;
import org.springframework.jdbc.core.RowMapper;
import org.springframework.jdbc.core.namedparam.MapSqlParameterSource;
import org.springframework.jdbc.core.simple.SimpleJdbcInsert;

import javax.sql.DataSource;
import java.sql.ResultSet;
import java.sql.SQLException;
import java.util.HashMap;
import java.util.List;
import java.util.Map;
import java.util.Optional;

public class JdbcTemplateMemberRepository implements MemberRepository{

    private final JdbcTemplate jdbcTemplate;

    public JdbcTemplateMemberRepository(DataSource dataSource) {
        jdbcTemplate = new JdbcTemplate(dataSource);
    }

    @Override
    public Member save(Member member) {
        SimpleJdbcInsert jdbcInsert = new SimpleJdbcInsert(jdbcTemplate);
        jdbcInsert.withTableName("member").usingGeneratedKeyColumns("id");

        Map<String, Object> parameters = new HashMap<>();
        parameters.put("name", member.getName());

        Number key = jdbcInsert.executeAndReturnKey(new MapSqlParameterSource(parameters));
        member.setId(key.longValue());
        return member;
    }

    @Override
    public Optional<Member> findById(Long id) {
        List<Member> result = jdbcTemplate.query("select * from member where id = ?", memberRowMapper(), id);
        return result.stream().findAny();
    }

    @Override
    public Optional<Member> findByName(String name) {
        List<Member> result = jdbcTemplate.query("select * from member where name = ?", memberRowMapper(), name);
        return result.stream().findAny();
    }

    @Override
    public List<Member> findAll() {
        return null;
    }

    private RowMapper<Member> memberRowMapper(){
        return (rs, rowNum) -> {

            Member member = new Member();
            member.setId(rs.getLong("id"));
            member.setName(rs.getString("name"));
            return member;
        };
    }
}
</code></pre>

- JdbcTemplate를 사용하도록 스프링 설정 변경
- `SpringConfig`
<pre><code>
package hello.hellospring;

import hello.hellospring.repository.JdbcMemberRepository;
import hello.hellospring.repository.JdbcTemplateMemberRepository;
import hello.hellospring.repository.MemberRepository;
import hello.hellospring.repository.MemoryMemberRepository;
import hello.hellospring.service.MemberService;
import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;

import javax.sql.DataSource;

@Configuration
public class SpringConfig {
    private final DataSource dataSource;

    public SpringConfig(DataSource dataSource) {
        this.dataSource = dataSource;
    }

    @Bean
    public MemberService memberService() {
        return new MemberService(memberRepository());
    }

    @Bean
    public MemberRepository memberRepository() {
        // return new MemoryMemberRepository();
        // return new JdbcMemberRepository(dataSource);
        return new JdbcTemplateMemberRepository(dataSource);
    }
}
</code></pre>

* JPA

- JPA는 기존의 반복 코드는 물론이고, 기본적인 SQL도 JPA가 직접 만들어서 실행해준다.
- JPA를 사용하면, SQL과 데이터 중심의 설계에서 객체 중심의 설계로 패러다임을 전환을 할 수 있다.
- JPA를 사용하면 개발 생산성을 크게 높일 수 있다.

- build.gradle 파일에 JPA, h2 데이터베이스 관련 라이브러리 추가
<pre><code>
dependencies {
    implementation 'org.springframework.boot:spring-boot-starter-thymeleaf'
    implementation 'org.springframework.boot:spring-boot-starter-web'
    //implementation 'org.springframework.boot:spring-boot-starter-jdbc'
    implementation 'org.springframework.boot:spring-boot-starter-data-jpa'
    runtimeOnly 'com.h2database:h2'
    testImplementation('org.springframework.boot:spring-boot-starter-test') {
        exclude group: 'org.junit.vintage', module: 'junit-vintage-engine'
    }
}
</code></pre>
- `spring-boot-starter-data-jp` 내부에 jdbc 관련 라이브러리를 포함한다. 따라서 jdbc는 제거해도 된다.

- 스프링 부트에 JPA 설정 추가
- `resources/application.properties`
<pre><code>
spring.datasource.url=jdbc:h2:tcp://localhost/~/test
spring.datasource.driver-class-name=org.h2.Driver
spring.datasource.username=sa // 스프링부트 2.4부턴 꼭 추가해야 함.

spring.jpa.show-sql=true
spring.jpa.hibernate.ddl-auto=none
</code></pre>
- `show-sql`: JPA가 생성하는 SQL을 출력한다.
- `ddl-auto`: JPA는 테이블을 자동으로 생성하는 기능을 제공하는데 none 를 사용하면 해당 기능을 끈다
- `create`를 사용하면 엔티티 정보를 바탕으로 테이블도 직접 생성해준다.

- JPA 엔티티 매핑
<pre><code>
package hello.hellospring.domain;

import jakarta.persistence.*;

@Entity
public class Member {

    @Id @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    private String name;

    public Long getId() {
        return id;
    }

    public void setId(Long id) {
        this.id = id;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }
}
</code></pre>

- JPA 회원 리포지토리
<pre><code>
package hello.hellospring.repository;

import hello.hellospring.domain.Member;
import jakarta.persistence.EntityManager;

import java.util.List;
import java.util.Optional;

public class JpaMemberRepository implements MemberRepository{

    private final EntityManager em;

    public JpaMemberRepository(EntityManager em) {
        this.em = em;
    }

    @Override
    public Member save(Member member) {
        em.persist(member);
        return member;
    }

    @Override
    public Optional<Member> findById(Long id) {
        Member member = em.find(Member.class, id);
        return Optional.ofNullable(member);
    }

    @Override
    public List<Member> findAll() {
        return em.createQuery("select m from Member m", Member.class)
                .getResultList();
    }

    @Override
    public Optional<Member> findByName(String name) {
        List<Member> result = em.createQuery("select m from Member m where m.name = :name", Member.class)
                .setParameter("name", name)
                .getResultList();

        return result.stream().findAny();
    }
}
</code></pre>

- 멤버 서비스 계층에 트랜잭션 추가
<pre><code>
import org.springframework.transaction.annotation.Transactional;

@Transactional
public class MemberService {}
</code></pre>
- 스프링은 해당 클래스의 메서드를 실행할 때 트랜잭션을 시작하고, 메서드가 정상 종료되면 트랜잭션을 커밋한다. 만약 런타임 예외가 발생하면 롤백한다.
- (중요★)JPA를 통한 모든 데이터 변경은 트랜잭션 안에서 실행해야 한다.

- JPA를 사용하도록 스프링 설정 변경
<pre><code>
package hello.hellospring;

import hello.hellospring.repository.*;
import hello.hellospring.service.MemberService;
import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;
import javax.persistence.EntityManager;

import javax.sql.DataSource;

@Configuration
public class SpringConfig {
    private final DataSource dataSource;
    private final EntityManager em;

    public SpringConfig(DataSource dataSource, EntityManager em) {
        this.dataSource = dataSource;
        this.em = em;   
    }

    @Bean
    public MemberService memberService() {
        return new MemberService(memberRepository());
    }

    @Bean
    public MemberRepository memberRepository() {
        // return new MemoryMemberRepository();
        // return new JdbcMemberRepository(dataSource);
        // return new JdbcTemplateMemberRepository(dataSource);
        return new JpaMemberRepository(em);
    }
}
</code></pre>

* 스프링 데이터 JPA

- 스프링 데이터 JPA는 JPA를 편리하게 사용할 수 있도록 도와주는 기술.

- 스프링 데이터 JPA 회원 리포지토리(인터페이스)
<pre><code>
package hello.hellospring.repository;

import hello.hellospring.domain.Member;
import org.springframework.data.jpa.repository.JpaRepository;

import java.util.Optional;

public interface SpringDataJpaMemberRepositrory extends JpaRepository<Member, Long>, MemberRepository {

    @Override
    Optional<Member> findByName(String name);
}
</code></pre>

- 스프링 데이터 JPA 회원 리포지토리(인터페이스)를 사용하도록 스프링 설정 변경
<pre><code>
package hello.hellospring;

import hello.hellospring.repository.*;
import hello.hellospring.service.MemberService;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;

@Configuration
public class SpringConfig {

    private final MemberRepository memberRepository;

    @Autowired
    public SpringConfig(MemberRepository memberRepository) {
        this.memberRepository = memberRepository;
    }

    @Bean
    public MemberService memberService(){
        return new MemberService(memberRepository);
    }
}
</code></pre>
- 스프링 데이터 JPA가 `SpringDataJpaMemberRepository` 를 스프링 빈으로 자동 등록해준다.

< 2023-07-14 / 스프링 입문 - 섹션 6 END >
-------------

<hr/>

< 2023-07-17 / 스프링 입문 - 섹션 7 >
-------------

* AOP

- AOP : Aspect Orented Programming
- 공통 관심 사항 (cross-cutting concern) vs 핵심 관심 사항 (core concern)분리

<pre><code>
package hello.hellospring.aop;

import org.aspectj.lang.ProceedingJoinPoint;
import org.aspectj.lang.annotation.Around;
import org.aspectj.lang.annotation.Aspect;
import org.springframework.stereotype.Component;

@Aspect
@Component
public class TimeTraceAop {

    @Around("execution(* hello.hellospring..*(..))")
    public Object execut(ProceedingJoinPoint joinPoint) throws Throwable{
        long start = System.currentTimeMillis();
        System.out.println("START: " + joinPoint.toString());
        
        try{
            return joinPoint.proceed();
        } finally {
            long finish = System.currentTimeMillis();
            long timeMs = finish - start;
            System.out.println("END: " + joinPoint.toString() + " " + timeMs + "ms");
        }
    }
}
</code></pre>

- 위 코드를 통해 시간을 측정하는 로직을 별도의 공동 로직으로 만들었다.
- AOP를 이용하여 핵심 관리 사항을 깔끔하게 유지할 수 있다.
- 변경이 필요하면 이 로직만 변경하면 된다.
- `@Around()`를 사용하여 원하는 적용 대상을 선택할 수 있다.

* AOP 동작 방식 설명
- 스프링은 helloController가 memberService를 의존하고 있고 helloController가 만약 메소드를 호출하면 memberService도 메소드를 호출했을 것이다.

- AOP가 존재할 때 가짜 memberService(프록시)를 만든다. 컨테이너에 스프링 빈을 등록할 때 진짜 서비스가 아닌 가짜 서비스(프록시)를 세워둔다.
- 가짜 서비스(프록시)가  `joinPoint.proceed()`를 하면 그때 진짜 서비스를 호출한다.

< 2023-07-17 / 스프링 입문 - 섹션 7 END >
-------------

<hr/>

< 2023-07-20 / SQL & JDBC 프로그래밍 / SQL 1-1 ~ DDL >

* SQL(Structured Query Language)
- SQL은 데이터를 보다 쉽게 검색하고 추가, 삭제, 수정 같은 조작을 할 수 있도록 고안된 컴퓨터 언어이다.
- 관계형 데이터베이스에서 데이터를 조작하고 쿼리하는 표준 수단이다.
- DML : INSERT, UPDATE, DELETE, SELECT 등. 데이터를 조작하기 위해 사용.
- DDL : CREATE, DROP, ALTER 등. 데이터베이스 스키마를 정의하거나 조작하기 위해 사용.
- DCL : GRANT 및 REVOKE (권한 관리, 데이터 보안, 무결성) 등. 데이터를 제어하는 언어.

* DB생성 및 권한부여, 연결끊기
<pre><code>
mysql> create database connectdb; // DB이름 : connectdb
</code></pre>

<pre><code>
grant all privileges on connectdb.* to connectuser@'%' identified by 'connect123!';

grant all privileges on connectdb.* to connectuser@'localhost' identified by 'connect123!';

flush privileges;

QUIT
</code></pre>
- @’%’는 어떤 클라이언트에서든 접근 가능하다는 의미이고, @’localhost’는 해당 컴퓨터에서만 접근 가능하다는 의미.
- db이름 뒤의 * 는 모든 권한을 의미.
- QUIT, EXIT = 연결끊기

<pre><code>
mysql> use connectdb;
</code></pre>
- 사용중인 데이터베이스 전환.

* 테이블(table)의 구성요소
- 테이블 : RDBMS의 기본적 저장구조 한 개 이상의 column과 0개 이상의 row로 구성.
- 열 : 테이블 상에서의 단일 종류의 데이터를 나타냄.
- 행 : 열들의 값의 조합. 기본키(PK)에 의해 구분. (중복 x, 반드시 존재해야 함.)
- Field : 열과 행의 교차점. Field는 데이터 포함할 수 있고, 없을 때는 NULL값을 가짐.

* DML(Select) 문
<pre><code>
mysql> show tables; // 테이블 목록 확인
</code></pre>

<pre><code>
SELECT * FROM  DEPARTMENT; // 전체 데이터 검색
</code></pre>

<pre><code>
select empno, name, job from employee; // 특정 컬럼 검색
</code></pre>

<pre><code>
select empno as 사번, name as 이름, job as 직업 from employee; // 컬럼에 Alias 부여
</code></pre>

<pre><code>
SELECT concat( empno, '-', deptno) AS '사번-부서번호' 
FROM employee; // 컬럼 합성 / concat 문자열 결합함수
</code></pre>

<pre><code>
select distinct deptno from employee; // 중복행 제거 / DISTINCT 키워드
</code></pre>

- 오름차순, 내림차순
<pre><code>
select empno as 사번, name as 이름, job as 직업 from employee order by 이름 asc; // 오름차순 / ASC : 오름차순
</code></pre>

<pre><code>
select empno as 사번, name as 이름, job as 직업 from employee order by 이름 desc; // 내림차순 / DESC : 내림차순
</code></pre>

- where(특정 행 검색) 절

- 산술 비교 연산자
<pre><code>
select name, hiredate from employee where hiredate < '1981-01-01';

// 예제 : employee 테이블에서 고용일(hiredate)이 1981년 이전의 사원이름과 고용일을 출력.
</code></pre>

- 논리연산자
<pre><code>
select name, deptno from employee where deptno = 30;

// 예제 : employee 테이블에서 부서번호가 30인 사원이름과 부서번호를 출력.
</code></pre>

- IN 키워드
<pre><code>
select name, deptno from employee where deptno in (10, 30);

// 예제 : employee 테이블에서 부서번호가 10또는 30인 사원이름과 부서번호를 출력.
</code></pre>

- LIKE 키워드
- 와일드 카드를 사용하여 특정 문자를 포함한 값에 따라 조건을 처리.
- % 는 0에서부터 여러 개의 문자열을 나타냄
- _는 단 하나의 문자를 나타냄.
<pre><code>
select name, job from employee where name like '%A%';

// 예제 : employee 테이블에서 이름에 'A'가 포함된 사원의 이름(name)과 직업(job)을 출력.
</code></pre>

* DML(Select) 문 / 함수의 사용

- FLOOR(x) : x보다 크지 않은 가장 큰 정수를 반환합니다. BIGINT로 자동 변환합니다.
- CEILING(x) : x보다 작지 않은 가장 작은 정수를 반환합니다.
- ROUND(x) : x에 가장 근접한 정수를 반환합니다.
- POW(x,y) POWER(x,y) : x의 y 제곱 승을 반환합니다.
- GREATEST(x,y,...) : 가장 큰 값을 반환합니다.
- LEAST(x,y,...) : 가장 작은 값을 반환합니다.
- CURDATE(),CURRENT_DATE : 오늘 날짜를 YYYY-MM-DD나 YYYYMMDD 형식으로 반환합니다.
- CURTIME(), CURRENT_TIME : 현재 시각을 HH:MM:SS나 HHMMSS 형식으로 반환합니다.
- NOW(), SYSDATE() , CURRENT_TIMESTAMP : 오늘 현시각을 YYYY-MM-DD HH:MM:SS나 YYYYMMDDHHMMSS 형식으로 반환합니다. 
- DATE_FORMAT(date,format) : 입력된 date를 format 형식으로 반환합니다.
- PERIOD_DIFF(p1,p2) : YYMM이나 YYYYMM으로 표기되는 p1과 p2의 차이 개월을 반환합니다. 

* DML(Select) 문 / 그룹함수, Group By 절

- COUNT(expr) : non-NULL인 row의 숫자를 반환
- COUNT(DISTINCT expr,[expr...]) : non-NULL인 중복되지 않은 row의 숫자를 반환
- COUNT(*) : row의 숫자를 반환
- AVG(expr) : expr의 평균값을 반환
- MIN(expr) : expr의 최소값을 반환
- MAX(expr) : expr의 최대값을 반환
- SUM(expr) : expr의 합계를 반환
- GROUP_CONCAT(expr) : 그룹에서 concatenated한 문자를 반환
- VARIANCE(expr) : 분산
- STDDEV(expr) : expr의 표준 편자를 반환

<pre><code>
SELECT AVG(salary) , SUM(salary)
FROM employee
WHERE deptno = 30;

// 예제 : employee 테이블에서 부서번호가 30인 직원의 급여 평균과 총합계를 출력.
</code></pre>

<pre><code>
SELECT deptno, AVG(salary) , SUM(salary)
FROM employee
group by deptno;

// 예제 : employee 테이블에서 부서별 직원의 부서번호, 급여 평균과 총합계를 출력.
</code></pre>

* DML(INSERT) 문

<pre><code>
INSERT INTO 테이블명(필드1, 필드2, 필드3, 필드4, … ) 
        VALUES ( 필드1의 값, 필드2의 값, 필드3의 값, 필드4의 값, … )

INSERT INTO 테이블명
        VALUES ( 필드1의 값, 필드2의 값, 필드3의 값, 필드4의 값, … )
</code></pre>
- 필드명을 지정해주는 방식은 디폴트 값이 세팅되는 필드는 생략할 수 있다.
- 필드명을 지정해주는 방식은 추 후, 필드가 추가/변경/수정 되는 변경에 유연하게 대처 가능하다.
- 필드명을 생략했을 경우에는 모든 필드 값을 반드시 입력해야 한다.

<pre><code>
insert into ROLE (role_id, description) values ( 200, 'CEO');

// 예제 : ROLE 테이블에 role_id는 200, description에는 'CEO'로 한건의 데이터를 저장.
</code></pre>

* DML(UPDATE) 문

<pre><code>
UPDATE  테이블명
    SET  필드1=필드1의값, 필드2=필드2의값, 필드3=필드3의값, …
        WHERE  조건식
</code></pre>
- 조건식을 통해 특정 row만 변경할 수 있다.
- 조건식을 주지 않으면 전체 로우가 영향을 미치니 조심해서 사용하도록 한다.

<pre><code>
update ROLE
set description = 'CTO'
where role_id = 200;

//예제 : ROLE 테이블에 role_id가 200일 경우 description을 'CTO'로 수정.
</code></pre>

* DML(DELETE) 문

<pre><code>
DELETE
    FROM  테이블명
        WHERE  조건식
</code></pre>
- 조건식(WHERE)을 통해 특정 row만 삭제할 수 있다.
- 조건식(WHERE)을 주지 않으면 전체 로우가 영향을 미치니 조심해서 사용하도록 한다.

<pre><code>
delete from ROLE where role_id = 200;

// 예제 : ROLE 테이블에서 role_id는 200인 정보를 삭제.
// * where절을 안줄 경우 모든 데이터가 삭제되니 조심.
</code></pre>

* DDL / 테이블 생성

<pre><code>
create table 테이블명( 
        필드명1 타입 [NULL | NOT NULL][DEFAULT ][AUTO_INCREMENT], 
        필드명2 타입 [NULL | NOT NULL][DEFAULT ][AUTO_INCREMENT], 
        필드명3 타입 [NULL | NOT NULL][DEFAULT ][AUTO_INCREMENT], 
        ........... 
        PRIMARY KEY(필드명) 
        );
</code></pre>
- 데이터 형 외에도 속성값의 빈 값 허용 여부는 NULL 또는 NOT NULL로 설정
- DEFAULT 키워드와 함께 입력하지 않았을 때의 초기값을 지정
- 입력하지 않고 자동으로 1씩 증가하는 번호를 위한 AUTO_INCREMENT

<pre><code>
CREATE TABLE EMPLOYEE2(   
        empno      INTEGER NOT NULL PRIMARY KEY,  
        name       VARCHAR(10),   
        job        VARCHAR(9),   
        boss       INTEGER,   
        hiredate   VARCHAR(12),   
        salary     DECIMAL(7, 2),   
        comm       DECIMAL(7, 2),   
        deptno     INTEGER);

// 실습 : EMPLOYEE와 같은 구조를 가진 EMPLOYEE2 테이블을 생성.
</code></pre>

* DDL / 테이블 수정 (컬럼 추가, 삭제 / 테이블 수정, 이름 변경, 삭제)
<pre><code>
alter table 테이블명
        add  필드명 타입 [NULL | NOT NULL][DEFAULT ][AUTO_INCREMENT];

alter table 테이블명
        drop  필드명;
</code></pre>

- `컬럼 추가`
<pre><code>
alter table EMPLOYEE2
add birthdate varchar(12);

// 실습 : EMPLOYEE2 테이블에 생일(birthdate)칼럼을 varchar(12)형식으로 추가.
// (컬럼 추가)
</code></pre>

- `컬럼 삭제`
<pre><code>
alter table EMPLOYEE2
drop birthdate;​

// 실습 :  EMPLOYEE2 테이블의 생일(birthdate)칼럼을 삭제.
// (컬럼 삭제)
</code></pre>

- `컬럼 수정`
<pre><code>
alter table  테이블명
    change  필드명  새필드명 타입 [NULL | NOT NULL][DEFAULT][AUTO_INCREMENT];
</code></pre>
- change 키워드를 사용하고 칼럼을 새롭게 재정의 (이름부터 속성까지 전부)

<pre><code>
alter table EMPLOYEE2
change deptno dept_no int(11);

// 실습 : EMPLOYEE2 테이블의 부서번호(deptno)를 dept_no로 수정.
// (컬럼 수정)
</code></pre>

- `테이블 이름 변경`
<pre><code>
alter table  테이블명 rename 변경이름
</code></pre>

<pre><code>
alter table EMPLOYEE2
rename EMPLOYEE3;

// 실습 : EMPLOYEE2 테이블의 이름을 EMPLOYEE3로 변경.
</code></pre>

- `테이블 삭제`
<pre><code>
drop table 테이블이름;
</code></pre>
- 테이블 삭제 후 desc 명령을 수행하면, 존재하지 않는 테이블이라고 표시됨.
<pre><code>
drop table EMPLOYEE2;

// 실습 : EMPLOYEE2 테이블을 삭제.
</code></pre>

< 2023-07-20 / SQL & JDBC 프로그래밍 / SQL 1-1 ~ DDL END >
-------------

<hr/>


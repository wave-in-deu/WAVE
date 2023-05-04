
6-2 데이터 타입
    }
}

8-2 변수의 효용
public class Letter {
 
    public static void main(String[] args) {
        String name = "leezche";
        System.out.println("Hello, "+name+" ... "+name+" ... egoing ... bye");
         
        double VAT = 10.0;
        System.out.println(VAT);
    }
 
}

8-3 데이터 타입의 변환

public class Casting {
 
    public static void main(String[] args) {
         
        double a = 1.1;
        double b = 1;
        double b2 = (double) 1;
         
        System.out.println(b);
         
        // int c = 1.1;
        double d = 1.1;
        int e = (int) 1.1;
        System.out.println(e);
         
        // 1 to String 
        String f = Integer.toString(1);
        System.out.println(f.getClass());
 
 
    }
 
}

9-1 프로그래밍이란 무엇인가 

public class Program {
 
    public static void main(String[] args) {
         
        System.out.println(1);
        System.out.println(2);
        System.out.println(3);
 
    }
 
}

9-3 IOT 프로그램 만들기

- 반복적인 값을 변수 지정으로 재사용 가능.가독성 높임

import org.opentutorials.iot.Elevator;
import org.opentutorials.iot.Lighting;
import org.opentutorials.iot.Security;
 
public class OkJavaGoInHome {
 
    public static void main(String[] args) {
         
        String id = "JAVA APT 507";
         
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

10 디버거

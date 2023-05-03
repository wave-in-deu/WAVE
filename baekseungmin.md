23.05.03
6-1 데이터와 연산 
-숫자(Number) 
-문자열(String)
-영상/소리/기타 등등 

6-2 데이터 타입
public class Datatpye{
    public static void main(String[] args) {
        System.out.println(6); // Number
        System.out.println("six"); // String
         
        System.out.println("6"); // 문자 6
         
        System.out.println(6+6); // 12
        System.out.println("6"+"6"); // 문자 66
         
        System.out.println(6*6); // 36
//      System.out.println("6"*"6"); // 문자로 인식 =>곱해지지 않음
         
        System.out.println("1111".length()); // 문자열의 길이 4
//      System.out.println(1111.length()); // 숫자의 길이 x
    }
}
6-3 숫자와 연산 

public class Number {
 
    public static void main(String[] args) {
        // Operator
        System.out.println(6 + 2); // 8
        System.out.println(6 - 2); // 4
        System.out.println(6 * 2); // 12
        System.out.println(6 / 2); // 3
 
        System.out.println(Math.PI); // 3.141592653589793
        System.out.println(Math.floor(Math.PI));//소수점 제거
        System.out.println(Math.ceil(Math.PI));
         
         
    }
 
}

6-4 문자열의 표현

-문자열은 기본적으로 Sting에 ""안에 작성

public class StringApp {
 
    public static void main(String[] args) {
         
        // Character VS String 
        System.out.println("Hello World"); // 문자 표현
        System.out.println('H'); // 문자형 '' 사용 x
        System.out.println("H"); 
     
        System.out.println("Hello "
                + "World"); // helloworld 출력
         
        // new line
        System.out.println("Hello \nWorld");//Hello후 아랫줄 World 출력
         
        // escape
        System.out.println("Hello \"World\"");// escape =>특수한 기호를 문자열에 넣기위함
    }
 
}

6-5 문자열 다루기
public class StringOperation {
 
    public static void main(String[] args) {
         
        System.out.println("Hello World".length()); // 11
        System.out.println("Hello, [[[name]]] ... bye. ".replace("[[[name]]]", "duru"));// replace => oldChar(바꾸고 싶은 부분), newChar(바꾸고자 하는 문자열)을 받음
 
    }

}

7. 작심삼일공학
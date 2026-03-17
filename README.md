# java-lab-cseg-5eb
Experiments
## Experiment 1
## Title:1a(Implement Default Primitive Type)
```
class DefaultPrimitiveType {
    byte primbyte;
    short primshort;
    int primint;
    double primdouble;
    char primchar;
    float primfloat;
    long primlong;
    boolean primboolean;
    public static void main(String args[]) {
        DefaultPrimitiveType dDpt = new DefaultPrimitiveType();
        System.out.println("default value of byte:" + dDpt.primbyte);
        System.out.println("default value of short:" + dDpt.primshort);
        System.out.println("default value of int:" + dDpt.primint);
        System.out.println("default value of double:" + dDpt.primdouble);
        System.out.println("default value of char:" + dDpt.primchar + " '");
        System.out.println("default value of float:" + dDpt.primfloat);
        System.out.println("default value of long:" + dDpt.primlong);
        System.out.println("default value of boolean:" + dDpt.primboolean);
    }
}
```
## output:
![Output for 1a](https://github.com/Kayapati-Vennela/java-lab-cseg-5eb/blob/3a3a9e73ff576021fce821d401979f57f9ded17c/exp1a.png)

## Title:1b(Implement Quadratic Equation Solution)
```
import java.util.Scanner;
class Quadraticequation{
     public static void main(String args[]){
         Scanner sc=new Scanner(System.in);
         System.out.println("Enter value of a:");
         double a=sc.nextDouble();
          System.out.println("Enter value of b:");
         double b=sc.nextDouble();
          System.out.println("Enter value of c:");
         double c=sc.nextDouble();
         double D=b*b-4*a*c;
         if(D>0){
            System.out.println("Roots are real and distinct");
            double root1=(-b+Math.sqrt(D))/(2*a);
            double root2=(-b-Math.sqrt(D))/(2*a);
            System.out.println("Root1:"+root1);
            System.out.println("Root2:"+root2);
            }
         else if(D==0){
            System.out.println("Roots are equal and real");
            double root=-b/(2*a);
            System.out.println("Root:"+root);
            }
         else{
            System.out.println("Roots are complex and imaginary");
            double realpart=-b/(2*a);
            double imaginarypart=Math.sqrt(-D)/(2*a);
            System.out.println("Roots are complex and imaginary");
            System.out.println("Root1="+realpart+"+i"+imaginarypart);
            System.out.println("Root2="+realpart+"-i"+imaginarypart);
            }
        sc.close();
        }
   }
```
## output:
![Output for 1b](https://github.com/Kayapati-Vennela/java-lab-cseg-5eb/blob/71f07a8625ee827708e72613f4fc6788a302f092/exp1b.png)

## Experiment 2
## Title:2a(Implement Class Mechanism)
```
class Rectangle{
  double l;
  double b;
  double area(){
    return l*b;
  }
  double perimeter(){
   return 2*(l+b);
   }
 }
class main{
  public static void main(String args[]){
    Rectangle rect =new Rectangle();
    rect.l=6;
    rect.b=12;
    double area = rect.area();
    double perimeter =rect.perimeter();
    System.out.println("area is:" +area);
    System.out.println("perimeter is:" +perimeter);
    }
  }
```
## output:
![Output for 2a](https://github.com/Kayapati-Vennela/java-lab-cseg-5eb/blob/ad96d82fa13038b9e1cecc1775f2cfd2fb5062cc/exp2a.png)

## Title:2b(Implement Overloading Method)
```
class sum{
  int sum(int a ,int b){
    return a+b;
  }
  int sum(int a ,int b,int c){
  return a+b+c;
  }
  double sum(double a ,double b){
   return a+b;
  }
}
class main{
 public static void main(String args[]){
   sum s= new sum();
   System.out.println("sum of 2 integers:"+s.sum(20,16));
   System.out.println("sum of 3 integers:"+s.sum(20,16,17));
   System.out.println("sum of two real numbers:"+s.sum(30.465,15.675));
  }
}
```
![Output for 2b](https://github.com/Kayapati-Vennela/java-lab-cseg-5eb/blob/7f5f671fae9854dd6d51fd098bf7fc0140667abc/exp2b.png)

## Title:2c(Implement Constructor)
```
class student{
 String sname;
 int sage;
 double smarks;
 student(String name,int age,double marks){
   sname=name;
   sage=age;
   smarks=marks;
  }
 void display(){
  System.out.println("student name is :"+sname);
  System.out.println("student age is :"+sage);
  System.out.println("stduent marks is:"+smarks);
  }
}
class main{
 public static void main(String args[]){
  student std= new student("sree",12,960);
  std.display();
  }
}
```
![Output for 2c](https://github.com/Kayapati-Vennela/java-lab-cseg-5eb/blob/1bd32a571064b5de2ceb943d5f090b55c450ed94/exp2c.png)


## Experiment 3
## Title:3a(Implement Constructor Overload)
```
class student{
 String name;
 int age;
 double marks;
 student(){
 }
 student(String name,int age,double marks){
  this.name=name;
  this.age=age;
  this.marks=marks;
}
void display(){
  System.out.println("name:"+name);
  System.out.println("age:"+age);
  System.out.println("marks:"+marks);
  }
}

class main{
 public static void main(String args[]){
   student std= new student();
   std.display();
   student std1=new student ("sree",19,60);
   std1.display();
 }
}
```
![Output for 3a](https://github.com/Kayapati-Vennela/java-lab-cseg-5eb/blob/9c3307b1deb75fcc2fcdfa49c4525ded4ec8b4e6/exp3a.png)

## Title:3b(Implement Binary Search)
```
import java.util.Scanner;
class Binary {
    int list[];
    int size;
    Binary(int size) {
        this.size = size;
        list = new int[size];
    }
    void setList() {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter items in ascending order:");
        for (int i = 0; i < size; i++) {
            System.out.println("Enter value of " + (i + 1) + ":");
            list[i] = sc.nextInt();
        }
    }
    void getList() {
        System.out.println("List elements:");
        for (int i = 0; i < size; i++) {
            System.out.print(list[i] + " ");
        }
        System.out.println();
    }
    int binary(int key) {
        int low = 0;
        int high = size - 1;
        while (low <= high) {
            int mid = (low + high) / 2;
            if (list[mid] == key)
                return mid;
            else if (list[mid] < key)
                low = mid + 1;
            else
                high = mid - 1;
        }
        return -1;
    }
}
class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter size of list:");
        int size = sc.nextInt();
        Binary b = new Binary(size);
        b.setList();
        b.getList();
        System.out.println("Enter a key to search:");
        int key = sc.nextInt();
        int index = b.binary(key);
        if (index == -1) {
            System.out.println("Key item does not exist");
        } else {
            System.out.println("Key item exists at position: " + (index + 1));
        }
    }
}
```
![output for 3b](https://github.com/Kayapati-Vennela/java-lab-cseg-5eb/blob/8f02010c245169ccb3840a204c7c84418ac26a7f/exp3b.png)

## Title:3c(Implement Bubble Sort)
```
class BubbleSort {
    BubbleSort(int arr[]) {
        int n = arr.length;
        for (int i = 0; i < n - 1; i++) {
            for (int j = 0; j < n - i - 1; j++) {
                if (arr[j] > arr[j + 1]) {
                    int temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                }

            }
        }
    }
}
import java.util.Scanner;
class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter size of array:");
        int n = sc.nextInt();
        int arr[] = new int[n];
        System.out.println("Enter elements:");
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
        new BubbleSort(arr);
        System.out.println("Sorted array:");
        for (int i = 0; i < n; i++) {
            System.out.print(arr[i] + " ");
        }
    }
}
```
![output for 3c](https://github.com/Kayapati-Vennela/java-lab-cseg-5eb/blob/41999e8b1c38ee366952459112a107dcb9b782e7/exp3c.png)

## Experiment 4
## Title:4a(Implement Single Inheritance)
```
class Person {
    String name;
    int age;

    Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    void displayPersonDetails() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
    }
}

class Employee extends Person {
    double annualSalary;
    int yearOfJoining;
    String nationalInsuranceNumber;

    Employee(String name, int age, double salary, int year, String nin) {
        super(name, age);
        annualSalary = salary;
        yearOfJoining = year;
        nationalInsuranceNumber = nin;
    }

    void displayEmployeeDetails() {
        displayPersonDetails();
        System.out.println("Annual Salary: " + annualSalary);
        System.out.println("Year of Joining: " + yearOfJoining);
        System.out.println("National Insurance Number: " + nationalInsuranceNumber);
    }
}

public class TestEmployee {
    public static void main(String[] args) {
        Employee emp = new Employee("sree", 19, 60000, 2022, "NJ123456A");
        emp.displayEmployeeDetails();
    }
}
```
![output for 4a](https://github.com/Kayapati-Vennela/java-lab-cseg-5eb/blob/876781dc53cb9c8ef9284035be4be4c865d4cbcf/exp4a.png)

## Title:4b(Implement Multilevel Inheritance)
```
class Bicycle {
    String pedalType;

    void showBicycleInfo() {
        System.out.println("This is a bicycle with pedals");
        System.out.println("Pedal Type: " + pedalType);
    }
}

class Motorbike extends Bicycle {
    int engineCapacity;

    void showMotorbikeInfo() {
        System.out.println("This motorbike has an engine");
        System.out.println("Engine Capacity: " + engineCapacity + " cc");
    }
}

class ElectricBike extends Motorbike {
    int batteryCapacity;

    void showElectricBikeInfo() {
        System.out.println("This electric bike has an electric motor & battery");
        System.out.println("Battery Capacity: " + batteryCapacity + " Wh");
    }
}

public class TestVehicle {
    public static void main(String[] args) {
        ElectricBike eBike = new ElectricBike();

        eBike.pedalType = "Standard Pedals";
        eBike.engineCapacity = 250;
        eBike.batteryCapacity = 500;

        eBike.showBicycleInfo();
        eBike.showMotorbikeInfo();
        eBike.showElectricBikeInfo();
    }
}
```
![output for 4b](https://github.com/Kayapati-Vennela/java-lab-cseg-5eb/blob/ab3e7a4c9c4d50cd2da32918dee0a0ccb753e185/exp4b.png)

## Title:4c(Implement Abstract Class)
```
abstract class Figure {
    double dim1, dim2;

    Figure(double d1, double d2) {
        dim1 = d1;
        dim2 = d2;
    }

    abstract double area();
}

class Rectangle extends Figure {
    Rectangle(double length, double breadth) {
        super(length, breadth);
    }

    double area() {
        return dim1 * dim2;
    }
}

class Triangle extends Figure {
    Triangle(double base, double height) {
        super(base, height);
    }

    double area() {
        return 0.5 * dim1 * dim2;
    }
}

public class TestFigure {
    public static void main(String[] args) {
        Figure f1 = new Rectangle(23.4, 14.5);
        Figure f2 = new Triangle(12.3, 15.6);

        System.out.println("Area of Rectangle = " + f1.area());
        System.out.println("Area of Triangle = " + f2.area());
    }
}
```
![output for 4c](https://github.com/Kayapati-Vennela/java-lab-cseg-5eb/blob/de7ded3de51ef6feda975c56c27813cbfb3b639e/exp4c.png)

## Experiment 5
## Title:5a(Implementing Interface)
```
interface Sortable{
  void sort(int [] arr);
  }
class Bubblesort implements Sortable{
  public void sort(int [] arr){
   int size =arr.length;
   int temp=0;
   for(int i=0;i<size-1;i++){
    for(int j=0;j<size-i-1;j++){
      if(arr[j]>arr[j+1]){
         temp=arr[j];
         arr[j]=arr[i];
         arr[i]=temp;
          }
       }
     }
  }
}
class Selectionsort implements Sortable {
   public void sort (int [] arr){
    int size=arr.length;
    int minindex=0;
    int min;
    for(int i=0;i<size;i++){
      min =arr[i];
     for(int j=i+1;j<size;j++){
       if(min>arr[j]){
          min=arr[j];
          minindex=j;
         }
       }
     arr[i]=min;
    }
   }
 }
class Testsort {
    static void display(int arr[]) {
        for (int ele : arr) {
            System.out.print(ele + ", ");
        }
        System.out.println();
    }
    public static void main(String args[]) {
        int arr1[] = {9, 7, 4, 3, 6, 8};
        int arr2[] = {8, 6, 3, 4, 7, 9};
        Sortable s;
        s = new Bubblesort();
        s.sort(arr1);
        System.out.println("After Bubble Sort:");
        display(arr1);

        s = new Selectionsort();
        s.sort(arr2);
        System.out.println("After Selection Sort:");
        display(arr2);
    }
}
```
![output for 5a](https://github.com/Kayapati-Vennela/java-lab-cseg-5eb/blob/c19f737f74201dab7b84f554cbdbcca8c753ba4d/exp5a.png)

## Title:5b(Polymorphism)
```
class Vehicle{
    void run(){
          System.out.println(" vechicle is running:");
     }
  }
class car extends Vehicle{
    void run(){
           System.out.println("car is running :");
      }
  }
class bike extends Vehicle{
     void run(){
       System.out.println("bike is running:");
    }
  }
class TestVehicle{
   public static void main(String args[]){
     Vehicle v ;
     v=new car();
     v.run();
     v=new bike();
     v.run();
     v=new Vehicle();
     v.run();
    }
}
```
![output for 5b](https://github.com/Kayapati-Vennela/java-lab-cseg-5eb/blob/310b1cf7238a1ad213f35fbcb33587cfc1520092/exp5b.png)

## Title:5c(Implementing String Buffer)
```
class Deletechar{
  public static void main(String args[]){
    StringBuffer sb =new StringBuffer("java programming");
    System.out.println(sb);
    sb.deleteCharAt(4);
    System.out.println(sb);
    sb.delete(0,4);
    System.out.println(sb);

   }
}
```
![output for 5c](https://github.com/Kayapati-Vennela/java-lab-cseg-5eb/blob/ce000845732419ebf47acfd6931c95cf159c76f0/exp5c.png)

## Experiment 6
## Title:6a(Exception Handling)
```
import java.util.Scanner;
class ArrayIndexExceptionDemo {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter size of array: ");
        int n = sc.nextInt();
        int[] arr = new int[n];
        System.out.println("Enter " + n + " elements:");
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
        try {
            System.out.print("Enter index to access: ");
            int index = sc.nextInt();
            System.out.println("Element at index " + index + " is " + arr[index]);
        } catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Array index out of bounds!");
        }
        sc.close();
    }
}
```
![output for 6a](https://github.com/Kayapati-Vennela/java-lab-cseg-5eb/blob/bbe5d65943a73208a9b4cbc1acf9076da34e7187/exp6a.png)

## Title:6b(Implementing Multiple Catch Blocks)
```
import java.util.Scanner;

class MultipleCatchDemo {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int[] arr = {10, 20, 30, 40, 50};

        try {
            System.out.print("Enter first number: ");
            int a = sc.nextInt();

            System.out.print("Enter second number: ");
            int b = sc.nextInt();

            int result = a / b;
            System.out.println("Result = " + result);

            System.out.print("Enter index to access array: ");
            int index = sc.nextInt();
            System.out.println("Element = " + arr[index]);
        }
        catch (ArithmeticException e) {
            System.out.println("Arithmetic Exception occurred");
        }
        catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Array Index Out Of Bounds Exception occurred");
        }
        catch (Exception e) {
            System.out.println("Some other exception occurred");
        }

        sc.close();
        System.out.println("Program continues...");
    }
```
![output for 6b](https://github.com/Kayapati-Vennela/java-lab-cseg-5eb/blob/8f1105388900edcc6d5aef5e18c983f81d223144/exp6b.png)

## Title:6c(Implementing java built-in Exception)
```
import java.util.Scanner;

class BuiltInException {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        try {
            System.out.print("Enter a number to divide 100: ");
            int n = sc.nextInt();

            int result = 100 / n;
            System.out.println("Result = " + result);

            int[] arr = new int[3];
            System.out.println(arr[5]);
        }
        catch (ArithmeticException e) {
            System.out.println("Arithmetic Exception occurred");
        }
        catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Array Index Out Of Bounds Exception occurred");
        }
        catch (Exception e) {
            System.out.println("General Exception occured");
        }
       finally{
           System.out.println("Program execution continue...");
           sc.close();
       }
   }
}
```
![output for 6c](https://github.com/Kayapati-Vennela/java-lab-cseg-5eb/blob/d046987653a9158f4a562632d0468e095bf6cc5b/exp6c.png)

## Experiment 7
## Title:7a(User Defined Exception)
```
class InvalidCountryException extends Exception {
          InvalidCountryException() {
              super();
              }
              InvalidCountryException(String message) {
              super(message);
              }
            }
class UserRegion {

    void registerUser(String userName, String userCountry) throws InvalidCountryException {

        if (!userCountry.equals("India")) {
            throw new InvalidCountryException("User outside India cannot be registered");
        } else {
            System.out.println("User registration done successfully");
        }
    }

    public static void main(String args[]) {

        UserRegion ur = new UserRegion();

        try {
            ur.registerUser("Ravi", "USA");
        }
        catch (InvalidCountryException e) {
            System.out.println(e.getMessage());
        }
    }
}
```
![output for 7a](https://github.com/Kayapati-Vennela/java-lab-cseg-5eb/blob/bb41b0a8abd91b3b97b03e5b7c742f810a67af14/exp7a.png)

## Title:7b(Creating threads by extending thread class)
```
class GoodMorningThread extends Thread {
    public void run() {
        while (true) {
            System.out.println("Good Morning");
            try {
                Thread.sleep(1000); 
            } catch (InterruptedException e) {
                System.out.println(e);
            }
        }
    }
}
  class HelloThread extends Thread {
     public void run() {
          while(true) {
            System.out.println("Hello");
         try {
            Thread.sleep(2000);
         }
         catch(InterruptedException e) {
               System.out.print(e);
           }
        }
    }
  }
   class WelcomeThread extends Thread {
         public void run() {
          while(true) {
        System.out.println("Welcome");
         try {
           Thread.sleep(3000);
         }
         catch(InterruptedException e) {
         System.out.print(e);
         }
       }
     }
   }
  class TestThreads {
     public static void main(String args[]) {
            GoodMorningThread t1 = new GoodMorningThread();
            HelloThread t2 = new HelloThread();
            WelcomeThread t3 = new WelcomeThread();


            t1.start();
            t2.start();
            t3.start();
           }
         }
```
![output for 7b](https://github.com/Kayapati-Vennela/java-lab-cseg-5eb/blob/93756bd837283324cf22baac86a896465d8871ce/exp7b.png)

## Title:7c(Illustrating isAlive() and join())
```
class LongRunningTask extends Thread {
        public void run() {
      System.out.println("Long running task started...");
      try {
            for(int i=1;i<= 5;i++) {
      System.out.println("Working..." +i);
            Thread.sleep(1000);
        }
     }
      catch(InterruptedException e) {
       System.out.println(e);
   }
  System.out.println("Long running task completed!");
      }
     }
public class ThreadDemo {
    public static void main(String[] args) {

        LongRunningTask task1 = new LongRunningTask();

        System.out.println("Before starting task1: " + task1.isAlive());

        task1.start();

        System.out.println("After starting task1: " + task1.isAlive());

        try {
            System.out.println("Main thread waiting for task1 to complete using join()...");
            task1.join();
        } catch (InterruptedException e) {
            System.out.println(e);
        }

        System.out.println("After task1 completion: " + task1.isAlive());
        System.out.println("Main thread continues execution.");
    }
}
```
![output for 7c](https://github.com/Kayapati-Vennela/java-lab-cseg-5eb/blob/f386a0e2460290cd3776873586ec8090fc955f8d/exp7c.png)

## Experiment 8
## Title:8a(Illustrating Daemon Threads)
```
class DaemonThread extends Thread {
     public void run() {
      while(true) {
     System.out.println("Daemon thread running");
      try {
      Thread.sleep(500);
       }catch(InterruptedException e) {
        System.out.print(e);
         }
      }
}
}
  class UserThread extends Thread {
     public void run() {
          while(true) {
          for(int i=1;i<=5;i++) {
            System.out.println("User thread iteration:" +i);
            try {  
         Thread.sleep(1000);
          }catch(InterruptedException e) {
             System.out.print(e);
        }
      }
    }
}
}
class TestDaemon{
    public static void main(String[]args){
              UserThread userThread=new UserThread();
              DaemonThread daemonThread=new DaemonThread();
              daemonThread.setDaemon(true);
              userThread.start();
              daemonThread.start();
         }
}
```
![output for 8a](https://github.com/Kayapati-Vennela/java-lab-cseg-5eb/blob/0b6dfb8941316e9a74b69c9a96ebb28153f254e1/exp8a.png)

## Title:8b(Producer Consumer Problem)
```
class Buffer {
    int[] buffer;
    int count = 0;
    int in = 0, out = 0;

    Buffer(int size) {
        buffer = new int[size];
    }

    synchronized void produce(int item) {
        while (count == buffer.length) {
            try {
                wait();
            } catch (InterruptedException e) {}
        }

        buffer[in] = item;
        in = (in + 1) % buffer.length;
        count++;

        notify();

        System.out.println("Produced: " + item);
    }

    synchronized int consume() {
        while (count == 0) {
            try {
                wait();
            } catch (InterruptedException e) {}
        }

        int item = buffer[out];
        out = (out + 1) % buffer.length;
        count--;

        notify();

        System.out.println("Consumed: " + item);
        return item;
    }
}

class Producer extends Thread {
    Buffer buffer;
    int N;

    Producer(Buffer buffer, int N) {
        this.buffer = buffer;
        this.N = N;
    }

    public void run() {
        for (int i = 1; i <= N; i++) {
            buffer.produce(i);
        }
    }
}

class Consumer extends Thread {
    Buffer buffer;
    int N;

    Consumer(Buffer buffer, int N) {
        this.buffer = buffer;
        this.N = N;
    }

    public void run() {
        for (int i = 1; i <= N; i++) {
            buffer.consume();
        }
    }
}

public class ProducerConsumerDemo {
    public static void main(String[] args) {

        Buffer buffer = new Buffer(5);
        int N = 10;

        Producer p = new Producer(buffer, N);
        Consumer c = new Consumer(buffer, N);

        p.start();
        c.start();
    }
}
```
![output for 8b](https://github.com/Kayapati-Vennela/java-lab-cseg-5eb/blob/e35ff680c57a0c6d4bd7feed6d7442e765d9cc31/exp8b.png)

## Title:8c(Import and use the user defined packages)
```
package arithmetic;
public class ArithmeticOperations {
    public int add(int x, int y) {
        return x + y;
    }
    public int subtraction(int x, int y) {
        return x - y;
    }
    public int multiplication(int x, int y) {
        return x * y;
    }
    public int division(int x, int y) {
        return x / y;
    }
}
import arithmetic.ArithmeticOperations;
class Calculate {
    public static void main(String[] args) {
        ArithmeticOperations ae = new ArithmeticOperations();
        int sum = ae.add(10, 5);
        System.out.println("Addition: " + sum);
        int diff = ae.subtraction(10, 5);
        System.out.println("Subtraction: " + diff);
        int prod = ae.multiplication(10, 5);
        System.out.println("Multiplication: " + prod);
        int div = ae.division(10, 5);
        System.out.println("Division: " + div);
    }
}
```
![output for 8c](https://github.com/Kayapati-Vennela/java-lab-cseg-5eb/blob/6cf30dd83010274408e122d3ee2bd382b641cc75/exp8c.png)

## Experiment 11
## Title:11(Railway Reservation)
```
class Reservation {
    private int availableBerths;
    Reservation(int berths) {
        this.availableBerths = berths;
    }
    public synchronized void bookTicket(String name, int requestedBerths) {
        System.out.println(name + " is requesting " + requestedBerths + " berths.");
        if (requestedBerths <= availableBerths) {
            System.out.println("Berths available. Booking for " + name);
            availableBerths -= requestedBerths;
            System.out.println("Ticket booked for " + name);
            System.out.println("Remaining berths: " + availableBerths);
        } else {
            System.out.println("No berths available for " + name);
        }
        System.out.println("--------------------------------");
    }
}
class Person extends Thread {
    private Reservation reservation;
    private String personName;
    private int berthsNeeded;
    Person(Reservation reservation, String name, int berths) {
        this.reservation = reservation;
        this.personName = name;
        this.berthsNeeded = berths;
    }
    public void run() {
        reservation.bookTicket(personName, berthsNeeded);
    }
}
 public class RailwayReservation {
    public static void main(String[] args) {
        Reservation reservation = new Reservation(5);
        Person p1 = new Person(reservation, "Vishnu", 2);
        Person p2 = new Person(reservation, "Siri", 3);
        Person p3 = new Person(reservation, "Neha", 2);
        p1.start();
        p2.start();
        p3.start();

   }
}
```
![output for 11](https://github.com/Kayapati-Vennela/java-lab-cseg-5eb/blob/2b47b5fd0f5d20d8c3521e32eb1c4c1d6086c350/exp11.png)

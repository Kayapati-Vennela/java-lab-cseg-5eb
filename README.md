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
![Output for 3a](

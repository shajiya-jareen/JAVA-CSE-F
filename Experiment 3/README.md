## Experiment 3

## Experiment 3A

## TITLE: Implementing constructor overloading

---

## SOURCE CODE: student

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
System.out.println("Name:"+name);
System.out.println("Age:"+age);
System.out.println("marks:"+marks);
}
}

```

## MAIN.JAVA

```
class Main {
public static void main(String args[]){
student std = new student();
std.display();
student std1 =new student("Hari",40,67.8);
std1.display();
}
}

```

## OUTPUT:
<img width="1920" height="1080" alt="EXP3A" src="https://github.com/user-attachments/assets/113ac400-e805-4b86-9049-cc7ea3ac9347" />





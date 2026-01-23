# Experiment 2:
## TITLE : 2a) Display the student details.
## SOURCE CODE:

```

class student{
int id;
String name;
void setData(int i, String n){
id = i;
name = n;
}
void display(){
System.out.println("student ID:"+id);
System.out.println("student Name:"+name);
}
public static void main(String[] args){
student s1 = new student();
s1.setData(101,"Zareen");
s1.display();
}
}
```
## OUTPUT:

<img width="1920" height="1080" alt="Exp2a" src="https://github.com/user-attachments/assets/4883183b-8367-4b2f-a9a6-76c7d4a3116e" />

## TITLE : 2b) Display the Methodoverloading.
## SOURCE CODE:

```

class Methodoverloading {
int add(int a, int b){
return a+b;
}
int add(int a,int b,int c){
return a+b+c;
}
double add(double a,double b){
return a+b;
}
public static void main(String[] args){
Methodoverloading obj = new Methodoverloading();
System.out.println("Addition of two integers: " + obj.add(10, 20));
System.out.println("Addition of three integers: " + obj.add(5, 10, 15));
System.out.println("Addition of doubles: " + obj.add(2.5, 3.5));
}
}
```
## OUTPUT:

<img width="1920" height="1080" alt="Exp2b" src="https://github.com/user-attachments/assets/7356d8c9-42a7-49e6-ad16-774af67a9cf7" />



## TITLE : 2c) Display the studentconstructor. 
## SOURCE CODE:

```

class studentconstructor {
int id;
String name;
int marks;
studentconstructor(int i,String n,int m){
id=i;
name=n;
marks=m;
}
void display(){
System.out.println(" Id:"+id);
System.out.println(" Name:"+name);
System.out.println(" Marks:"+marks);
}
public static void main(String[] args){
studentconstructor s1=new studentconstructor(101,"Alice",85);
s1.display();
}
}
```

## OUTPUT:

<img width="1920" height="1080" alt="Exp2c" src="https://github.com/user-attachments/assets/4c8869b1-e085-415d-9532-ab5d3f85e05f" />


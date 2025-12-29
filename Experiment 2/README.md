#Experiment 2
##TITLE : 2a.)Display the student details
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
#output

<img width="1920" height="1080" alt="Exp2a" src="https://github.com/user-attachments/assets/4883183b-8367-4b2f-a9a6-76c7d4a3116e" />


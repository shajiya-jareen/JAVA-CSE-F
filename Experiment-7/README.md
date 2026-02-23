## Experiment 7
## TITLE : 7A) Write a JAVA program for creation of User Defined Exception.
## SOURCE CODE :

```
class InvalidCountryException extends Exception {

    public InvalidCountryException() {
        super();
    }

    public InvalidCountryException(String message) {
        super(message);
    }
}
public class UserRegistration {

    public void registerUser(String userName, String userCountry)
            throws InvalidCountryException {

        if (!userCountry.equalsIgnoreCase("India")) {
            throw new InvalidCountryException(
                    "User outside India cannot be registered");
        } else {
            System.out.println("User registration done successfully");
        }
    }

    public static void main(String[] args) {

        UserRegistration ur = new UserRegistration();

        try {
            ur.registerUser("Ravi", "USA");
        } catch (InvalidCountryException e) {
            System.out.println(e.getMessage());
        }

        try {
            ur.registerUser("Anita", "India");
        } catch (InvalidCountryException e) {
            System.out.println(e.getMessage());
        }
    }

```

## OUTPUT :


<img width="1920" height="1080" alt="Exp7a" src="https://github.com/user-attachments/assets/8f9017c8-7cdf-4acd-855a-769de7d276fe" />




## TITLE : 7B) Write a JAVA program that creates threads by extending Thread class.

## SOURCE CODE :

```

class GoodMorningThread extends Thread {

    @Override
    public void run() {
        try {
            while (true) {
                System.out.println("Good Morning");
                Thread.sleep(1000);  
            }
        } catch (InterruptedException e) {
            System.out.println("GoodMorningThread Interrupted");
        }
    }
}

class HelloThread extends Thread {

    @Override
    public void run() {
        try {
            while (true) {
                System.out.println("Hello");
                Thread.sleep(2000);  
            }
        } catch (InterruptedException e) {
            System.out.println("HelloThread Interrupted");
        }
    }
}

class WelcomeThread extends Thread {

    @Override
    public void run() {
        try {
            while (true) {
                System.out.println("Welcome");
                Thread.sleep(3000);   
            }
        } catch (InterruptedException e) {
            System.out.println("WelcomeThread Interrupted");
        }
    }
}

public class TestThreads {

    public static void main(String[] args) {

        GoodMorningThread t1 = new GoodMorningThread();
        HelloThread t2 = new HelloThread();
        WelcomeThread t3 = new WelcomeThread();

        t1.start();
        t2.start();
        t3.start();
    }
}

 ```

## OUTPUT :


<img width="1920" height="1080" alt="Exp7b" src="https://github.com/user-attachments/assets/8f5bf1f2-7496-4ebf-a1d0-f9a6569562be" />






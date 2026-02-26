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



## TITLE : 7C) Write a JAVA program illustrating is Alive and join().

## SOURCE CODE :

```


class LongRunningTask extends Thread {

    
    public void run() {
        try {
            System.out.println("Long running task started...");

            
            for (int i = 1; i <= 5; i++) {
                System.out.println("Working... " + i);
                Thread.sleep(1000);   // 1 second delay
            }

            System.out.println("Long running task completed!");
        } catch (InterruptedException e) {
            System.out.println("Thread was interrupted.");
        }
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
            System.out.println("Main thread interrupted.");
        }

        System.out.println("After join(): " + task1.isAlive());

        System.out.println("Main thread continues after task1 completed.");
    }
}

```

## OUTPUT :

<img width="1920" height="1080" alt="Exp7c" src="https://github.com/user-attachments/assets/e9283a58-0705-4678-b322-6f167de07d9e" />



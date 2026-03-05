## EXPERIMENT 8

## TITLE: 8A)Write a program illustrating Daemon Threads.
## SOURCE CODE:

```


class DaemonThread extends Thread {

   
    @Override
    public void run() {
        try {
           
            while (true) {
                System.out.println("Daemon thread running");
                Thread.sleep(500);   // Sleep for 500 milliseconds
            }
        } catch (InterruptedException e) {
            System.out.println("Daemon thread interrupted");
        }
    }
}

class UserThread extends Thread {

    @Override
    public void run() {
        try {
                        for (int i = 1; i <= 5; i++) {
                System.out.println("User thread iteration: " + i);
                Thread.sleep(1000);   // Sleep for 1000 milliseconds
            }
        } catch (InterruptedException e) {
            System.out.println("User thread interrupted");
        }
    }
}


public class TestDaemon {

    public static void main(String[] args) {

        UserThread userThread = new UserThread();

        DaemonThread daemonThread = new DaemonThread();

        
        daemonThread.setDaemon(true);

        
        userThread.start();
        daemonThread.start();

        
        System.out.println("Main thread execution completed");
    }
}

```

## OUTPUT:

<img width="1920" height="1080" alt="EXP8A" src="https://github.com/user-attachments/assets/635ecc2e-a5ed-427f-aa8d-3ce3cf1d60f8" />


## TITLE: 8B)Write a JAVA program on Producer Consumer Problem.

## SOURCE CODE:

```

class Buffer {

    int[] buffer;
    int count = 0;
    int in = 0;
    int out = 0;

    Buffer(int size) {
        buffer = new int[size];
    }

        synchronized void produce(int item) {
        try {

            
            while (count == buffer.length) {
                wait();
            }

            buffer[in] = item;
            in = (in + 1) % buffer.length;
            count++;

            notify(); // Notify consumer

        } catch (Exception e) {
            System.out.println(e);
        }
    }

    
    synchronized int consume() {
        int item = 0;

        try {

                        while (count == 0) {
                wait();
            }

            item = buffer[out];
            out = (out + 1) % buffer.length;
            count--;

            notify(); // Notify producer

        } catch (Exception e) {
            System.out.println(e);
        }

        return item;
    }
}


class Producer extends Thread {

    Buffer buffer;

    Producer(Buffer buffer) {
        this.buffer = buffer;
    }

    public void run() {

        for (int i = 1; i <= 10; i++) {
            buffer.produce(i);
            System.out.println("Produced: " + i);
        }
    }
}


class Consumer extends Thread {

    Buffer buffer;

    Consumer(Buffer buffer) {
        this.buffer = buffer;
    }

    public void run() {

        for (int i = 1; i <= 10; i++) {
            int item = buffer.consume();
            System.out.println("Consumed: " + item);
        }
    }
}


public class ProducerConsumer {

    public static void main(String[] args) {

        Buffer buffer = new Buffer(5);

        Producer p = new Producer(buffer);
        Consumer c = new Consumer(buffer);

        p.start();
        c.start();
    }
}

```

## OUTPUT:

<img width="1920" height="1080" alt="EXP8B" src="https://github.com/user-attachments/assets/e5ef11f8-7333-44c5-bce4-f4f0df05eed7" />


## TITLE: 8C)Write a JAVA program that import and use the user defined Packages.

## SOURCE CODE:

```


package arithmetic;


public class ArithmeticOperations {

        public int addition(int x, int y) {
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

import arithmetic.*;   
public class Calculate {

    public static void main(String[] args) {

ArithmeticOperations ao = new ArithmeticOperations();

        int sum = ao.addition(10, 5);
        System.out.println("Addition: " + sum);

        int diff = ao.subtraction(10, 5);
        System.out.println("Subtraction: " + diff);

        int prod = ao.multiplication(10, 5);
        System.out.println("Multiplication: " + prod);

        int quot = ao.division(10, 5);
        System.out.println("Division: " + quot);
    }
}

```

## OUTPUT:

<img width="1920" height="1080" alt="EXP8C" src="https://github.com/user-attachments/assets/b6d16800-8c9f-49b0-bb4d-e4549e07511b" />


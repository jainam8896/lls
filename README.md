import java.util.*;

public class stack {

    

    node head;

 

    static Scanner sc = new Scanner(System.in);

     class node {

        int data;

        node next;

        node() {

            System.out.println("Enter the data");

            data = sc.nextInt();

            next = null;

        }

    }

     

     public  void push() {

        node newnode = new node();

        if (head == null) {

            head = newnode;

            return;

        }

        newnode.next = head;

        head = newnode;

    }

     

     

     public void peek() {

        if (head == null) {

            System.out.println("no data to show");

            return;

        }

        

         System.out.println("element at top "+head.data);

       

    }

     

    public void pop()

    {

         if (head == null) {

            System.out.println("no data to show");

            return;

        }

         

         System.out.println("deleted element is : "+head.data);

         head = head.next;

  

    }

     

     public void display() {

        if (head == null) {

            System.out.println("no data to show");

            return;

        }

        

        

        node temp = head;

        while (temp != null) {

           

            System.out.println("    "+temp.data);

            System.out.println("|________|");

            temp = temp.next;

        }

               

    }

     

     public static void main(String[] args) {

        stack ll = new stack();

        int ch;

        do {

            System.out.println();

            System.out.println("Enter 1 for push");

            System.out.println("Enter 2 for display");

            System.out.println("Enter 3 for pop");

            System.out.println("Enter 4 for peek");

            

            System.out.println("5 for exit");

            ch = sc.nextInt();

            switch (ch) {

                case 1:

                    ll.push();

                    break;

                case 2:

                    ll.display();

                    break;

                case 3:

                    ll.pop();

                    break;

                case 4:

                    ll.peek();

                    break;

                

            }

        } while (ch != 5);

    }

    

}

# Interviewportfolio
My experience of coding projects to be shown to interviewers in UKM

Array coding project:

/*The program will :
  1. Repeat N times to read bookTitle[] and borrowCount[]
  2. Repeat N times to display bookTitle[] , borrowCount[] and index location 
  3. Repeat N times to determine bookTitle [] with bookSearch to display borrowCount[] and index location 
    OR display error message.
  4. Repeat N times to determine borrowCount [] with borrowSearch to display bookTitle[] and index location 
    OR display error message.
    Date:3/10/26
    Programmer:Siveshavar
*/

  import java.util.Scanner;
  class AssignmentCs
    
   {
     public static void main(String[]args)
     
     {
       Scanner input= new Scanner(System.in);
       Scanner inputString = new Scanner (System.in); 
       
       System.out.println ("-------------------------------------------------");
       System.out.println ("          BOOK AND BORROWING INFORMATION           ");
       System.out.println ("-------------------------------------------------");
       System.out.print("\nEnter number of books to record: ");
       int N=input.nextInt();
        
        //Loop for entering elements into both array
        System.out.print("\n----------------- ENTERING DATA ------------------");
       //Declare and Create Array
       String [] bookTitle = new String[N];
       int [] borrowCount = new int[N];
       
        for(int i=0; i<N; i++)
        {
          System.out.print("\n\nEnter Book Title: ");
          bookTitle[i] = inputString.nextLine();
          
          System.out.print ("Enter number of times book has been borrowed: ");
          borrowCount[i] = input.nextInt();
        }
         
         //Loop for displaying elements from both array
         System.out.print("\n----------------- DISPLAYING DATA ------------------");
         
         for(int j=0; j<N; j++)
         {
         System.out.println("\nBook Title: " + bookTitle[j] + "\nNumber of times borrowed: " + borrowCount[j] + "\nIndex Location=" + j); 
         }
         System.out.print("\n\n----------------- SEARCHING LIBRARY ------------------ ");
         //linear search for Book Title
         System.out.print("\n\nEnter Book Title you want to search: ");
         String bookSearch = inputString.nextLine();
         boolean found=false;
         
         //Loop for linear search - search Book Title
         for(int k=0; k<N; k++)
         {
           if(bookSearch.equals(bookTitle[k]))
           {System.out.print("FOUND!");
           System.out.print("\nNumber of times borrowed is: " + borrowCount[k] + "\nIndex location= " + k);
           found=true;
           } }
           
           //if bookSearch NOT FOUND
           if(found==false)
           {System.out.print("NOT FOUND!" + "\tSorry the Book Title you have entered is not found");
           }

         System.out.print("\n\n----------------- SEARCHING LIBRARY ------------------ ");
         //linear search for Borrow Count
         System.out.print("\n\nEnter the number of times the book has been borrowed that you want to search: ");
          int borrowSearch=input.nextInt();
          boolean foundBorrow=false;

          //Loop for linear search - search Borrow Count
          for(int R=0; R<N; R++){
            if(borrowSearch==borrowCount[R]){
              System.out.println("\nFOUND!" + "\nBook Title is: " + bookTitle[R] + "\nIndex Location= " + R);
              foundBorrow=true;}
            }
            
            //if borrowSearch NOT FOUND
            if(foundBorrow==false)
            {System.out.print("NOT FOUND!" + "\tSorry the Book that has been borrowed this specific number of times that you have entered is not found");
            }
            
            System.out.print("\n\n----------------- END OF PROGRAM --------------------- ");
     }
     
     
           
   }





   

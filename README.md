# FDSL_43_PrathameshDesai
#include<stdio.h>

struct book 
{
 	char book_name[5];
 	int  book_price  ;
};
 void  main ()
 {
 	struct book b[20];
 	int n , ch  , d  , i , p   ; 
 	int c=0 ;
 	printf("\nEnter the  number of book ");
					scanf("%d",&n );
					for (i=0 ; i<n ; i++)
					{
						printf("\tEnter the book number %d " ,i+1 );
						printf("\n\tEnter the book name  :");
						scanf("%s", b[i+1].book_name);
						printf("\tEnter the book price :");
						scanf("%d", &b[i+1].book_price);
					}
 	
 		do
 		 {
 		 	printf("The Menu \n\t 1. Add new  records\n\t 2. Display the records \n\t 3. Update the current record \n\t 4.Delete the perticular records \n\t 5.Exit\n\t Enter the choice :   ");
 		 	scanf("%d", &ch);
 		 	switch(ch)
 		 	{
 		 		case 1 : 
 		 			printf("Enter at which position ");
  					scanf("%d",&p); 
  					for (i=n ; i>=p ; i--)
  			{
  					b[i+1]= b[i];
  		
			}
			
  					printf("\nEnter the book number %d " ,i+1 );
					printf("\nEnter the book name  :");
					scanf("%s", b[p].book_name);
	
					printf("Enter the book price :");
					scanf("%d", &b[p].book_price);
					printf("Youe data is saved Sucessfully ");
					break ; 
				case 2 :
						for (i=0 ; i<=n ; i++)
					{
						printf("\n\t\tThe book number %d " , i+1);
						printf("\n\t\tThe book name is  : %s" , b[i+1].book_name);
						printf("\n\t\tThe book price is  : %d" , b[i+1].book_price);
					}
					break ; 
					
					
				case 3 : printf("Enter at which position ");
  					scanf("%d",&p); 
  				printf("Enter book name ");
  				scanf("%s",b[p].book_name);
  				printf("Enter book price ");
  				scanf("%d",&b[p].book_price );
  				printf("Youe data is saved Sucessfully ");
  				 	break ; 
  				case 4 :printf("Enter at which position you want to delete ");
  						int e ; 
  						scanf("%d",&e);
  						for(i=e ; i<=c ; i++);
  						{
  						b[i]=b[i+1];
  						}
  						c--;
  						printf("After modifing data ");
  						for(i=0 ; i<c; i++ )
  						{
  						printf("%d", i);
  						printf("book name %s ",b[i+1].book_name);
  						printf("book price %d ",b[i+1].book_price);
  						printf("Youe data is saved Sucessfully ");
  						}
  						break ;
  						}
  						
 		 	printf("\nDO you want to contine(1/0)");
 		 	scanf("%d", &d); 
 		} while(d!=0);
                      
 }
 

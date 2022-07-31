//Activity1:Create a program to sort elements in dictionary order or the strings entered by the user, the program must accept 5 strings from the user and the output must be in order:

#include <stdio.h>
#include <string.h>

int main() {
   char str[5][50], temp[50];
   printf("Enter 5 words: ");

   for (int i = 0; i < 5; ++i) {
      fgets(str[i], sizeof(str[i]), stdin);
   }

   for (int i = 0; i < 5; ++i) {
      for (int j = i + 1; j < 5; ++j) {

         if (strcmp(str[i], str[j]) > 0) {
            strcpy(temp, str[i]);
            strcpy(str[i], str[j]);
            strcpy(str[j], temp);
         }
      }
   }

   printf("\nIn the lexicographical order: \n");
   for (int i = 0; i < 5; ++i) {
      fputs(str[i], stdout);
   }
   return 0;
}

//Activity2:Concatenate Two Strings Without Using strcat()
#include <stdio.h>
#include <string.h>
 
int main()
{
  	char Str1[100], Str2[100];
  	int i, j;
 
  	printf("\n Please Enter the First String :  ");
  	gets(Str1);
  	
  	printf("\n Please Enter the Second :  ");
  	gets(Str2);

       
  	for (i = 0; Str1[i]!='\0'; i++);

      	
  	for (j = 0; Str2[j]!='\0'; j++, i++)
  	{
  		Str1[i] = Str2[j];
  	}
  	Str1[i] = '\0';

  	printf("\n After the Concatenate = %s", Str1);
  	
  	return 0;
}

//Activity3:Program to count vowels, consonants numbers, special characters
#include <stdio.h>
int main() {

  char line[150];
  int vowels, consonant, digit, space;

  
  vowels = consonant = digit = space = 0;

  
  printf("Enter a line of string: ");
  fgets(line, sizeof(line), stdin);

  
  for (int i = 0; line[i] != '\0'; ++i) {

    
    line[i] = (line[i]);

    
    if (line[i] == 'a' || line[i] == 'e' || line[i] == 'i' ||
        line[i] == 'o' || line[i] == 'u') {

     
      ++vowels;
    }

   
    else if ((line[i] >= 'a' && line[i] <= 'z')) {
      ++consonant;
    }

   
    else if (line[i] >= '0' && line[i] <= '9') {
      ++digit;
    }

    else if (line[i] == ' ') {
      ++space;
    }
  }

  printf("Vowels: %d", vowels);
  printf("\nConsonants: %d", consonant);
  printf("\nDigits: %d", digit);
  printf("\nWhite spaces: %d", space);

  return 0;
}
//Activity4: C Program to Find Largest Element in an Array
#include <stdio.h>

int main() {
   int array[10] = {1, 2, 3, 4, 5, 6, 7, 8, 9, 0};
   int loop, largest;

   largest = array[0];
   
   for(loop = 1; loop < 10; loop++) {
      if( largest < array[loop] ) 
         largest = array[loop];
   }
   
   printf("Largest element of array is %d", largest);   
   
   return 0;
}
//activity5:C Program to Add Two Matrices Using Multi-dimensional Arrays
#include <stdio.h>
int main(){
    int a[10][10], b[10][10], sum[10][10], i, j,column, row;
    

    printf("Enter total no. of rows[Between 1 and 10]: ");
    scanf("%d", &row);
    printf("Enter total no. of columns[Between 1 and 10]: ");
    scanf("%d", &column);
    
    printf("Enter First Matrix: \n");
    for (i = 0; i < row; i++)
        for(j = 0; j < column; j++)
            scanf("%d", &a[i][j]);
            
    printf("Enter Second Matrix: \n");
    for (i = 0; i < row; i++)
        for (j = 0; j < column; j++)
            scanf("%d", &b[i][j]);
            

    for (i = 0; i < row; i++){
        for (j = 0; j < column; j++){
            sum[i][j] = a[i][j] + b[i][j];
        }
    }
    

    printf("Sum of Two Matrices: \n");
    for (i = 0; i < row; i++){
        for(j = 0; j < column; j++){
            printf("%d ", sum[i][j]);
        }
        printf("\n");
    }
    return 0;
}

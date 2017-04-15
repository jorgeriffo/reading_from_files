# reading_from_files


//UNDERTANDING FILES IN C with reading

#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>
#include <string.h>

int main(void)

{

		FILE *fp = NULL;
		int sku = 4664;
		double price;

		fp = fopen("alpha.txt", "r");
		if (fp != NULL) {
       
       fscanf(fp, "%d %lf", &sku, &price);

       fprintf(fp, "sku = %d price = %10.2lf\n", sku, price);
       fclose(fp);

   } else {

   	 printf("Failed to open file\n");

   }

     return 0; 
}

# string-operations
/*c program to implement string operations using functions*/
#include <stdio.h>
#include <stdlib.h>
void str_comp(char s1[], char s2[]);
void str_concat(char s1[], char s2[]);
void str_length(char s1[]);
void main()
{
	char str1[10],str2[10];
    int ch;
    printf("1: compare strings \n 2: concatenate strings \n 3: find length of strings \n 4: Exit \n");
    while(1)
    {
        scanf("%d",&ch);
        switch(ch)
        {
        	case 1: printf("string 1 = \n");
                    scanf("%s",str1);
                    printf("string 2 = \n");
                    scanf("%s",str2);
                    str_comp(str1,str2);
                    break;
            case 2: printf("string 1 = \n");
                    scanf("%s",str1);
                    printf("string 2 = \n");
                    scanf("%s",str2);
                    str_concat(str1,str2);
                    break;
            case 3: printf("string = \n");
                    scanf("%s",str1);
                    str_length(str1);
                    break;
            case 4: exit(0);
          }
      }
}
void str_comp(char s1[10], char s2[10])
{
	int i=0;
    while(s1[i]==s2[i] && s1[i]!='\0')
    	i++;
    if(s1[i]<s2[i])
    	printf("%s is less than %s \n", s1,s2);
    else if(s1[i]>s2[i])
    	printf("%s is greater than %s", s1,s2);
    else
    	printf("%s is equal to %s",s1,s2);
}
void str_concat(char s1[10], char s2[10])
{
	int i,j;
    for (i=0;s1[i]!='\0';i++);
    for(j=0;s2[j]!=0;i++,j++)
    	s1[i]=s2[j];
    s1[i]='\0';
    printf("concatenated string is %s",s1);
}
void str_length(char s1[10])
{
	int i;
    for(i=0;s1[i]!='\0';i++);
    printf("length of %s is %d",s1,i);
}

  

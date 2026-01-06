#include<stdio.h>
int main()
{
	struct e
	{
		int rno,s1,s2,s3;
		float avg;
		char name[20];
	}e[60];
	int n,i;
	float total;
	printf("Enter the no.of students:");
	scanf("%d",&n);
	for(i=0;i<n;i++)
	{
	printf("Enter the student rno:");
	scanf("%d",&e[i].rno);
	printf("Enter the name of the student:");
	scanf("%s",e[i].name);
	printf("Enter the all subjects marks:");
	scanf("%d%d%d",&e[i].s1,&e[i].s2,&e[i].s3);
	total=e[i].s1+e[i].s2+e[i].s3;
	e[i].avg=total/3;
	}
	printf("------------------------------students percentage-----------------------------------");
	for(i=0;i<n;i++)
	{
		printf("\nThe student rno:%d",e[i].rno);
		printf("\nThe student name: %s",e[i].name);
		printf("\nThe student percentage %f",e[i].avg);
	}
}

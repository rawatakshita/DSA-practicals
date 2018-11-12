#include<stdio.h>
#include<malloc.h>
#include<stdlib.h>
#include<string.h>
struct node
{
	int data;
	struct node *next;
}*start;
void create(int);
void display();
void first_add(int);
int first_delete();
int main()
{
	int num,i,choice,pos;
	start=NULL;
	do
	{
		printf(" \n1.create  2.display  3.add  4 delete  5.Exit \n");
		printf("Enter your choice : ");
		scanf("%d",&choice);
		switch(choice)
		{
			case 1:printf("Enter item to be add in a list\n");
			scanf("%d",&num);
			create(num);
			break;
	        case 2:
	        display();
			break;
			case 3:printf("Add newnode and item in begning of list\n");
			scanf("%d",&num);
			first_add(num);
			break;
			case 4:
			printf("Your deleted item is : %d ",first_delete());
			break;
			case 5:exit(0);
			default: printf("wrong choice\n");
		}
	 }while(1); 
}
void create(num)
{
	struct node *q,*t;
	if(start==NULL)
	{
		q=(struct node*)malloc(sizeof(struct node));
		q->data=num;
		q->next=NULL;
		start=q;
	}
	else
	{
		q=start;
		while(q->next!=NULL)
		{
			q=q->next;
		}
		t=(struct node *)malloc(sizeof(struct node));
		t->data=num;
		t->next=NULL;
		q->next=t;
	}
}
void display()
{
	struct node *q;
	q=start;
	while(q!=NULL)
	{
		printf("%d\t",q->data);
		q=q->next;
	}
}
void first_add(int num)
{
	    struct node*q;
		q=(struct node*)malloc(sizeof(struct node));
		q->data=num;
		q->next=start;
		start=q;
}	
int first_delete()
{
	struct node *q,*t;
	q=start;
	if(q==NULL)
    {
    	printf("List is Empty\n");
    	return;
	}
	start=start->next;
	q->next=NULL;
	int num=q->data;
	free(q);
	return num;
}


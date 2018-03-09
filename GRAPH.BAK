#include<stdio.h>
#include<conio.h>
struct node
{
int dest;
struct node *next;
} ;
struct node *a[10];
struct list
{
struct node *head;
};
struct graph
{
int v;
struct list *array;
};
struct node *c_node(int dest)
{
struct node *temp=(struct node*) malloc(sizeof(struct node));
temp->dest=dest;
temp->next=NULL;
return temp;
}
struct graph* create_g(int v)
{ int i;

 struct graph *g=(struct graph*) malloc(sizeof(struct graph));
 g->v=v;
 g->array=(struct list*)malloc(v *sizeof(struct list));
 for( i=0;i<v;i++)
 {
 g->array[i].head=NULL;
 }
 return g;
 }
void addedge(struct graph *g ,int src,int dest)
{//undirected graph
 struct node *temp=c_node(dest);
 temp->next=g->array[src].head;
 g->array[src].head=temp;
 temp=c_node(src);
 temp->next=g->array[dest].head;
 g->array[dest].head=temp;
 }
  void print(struct graph *g)
 {
 int x;
  for(x=0;x<g->v;++x)
  {
  struct node *p=g->array[x].head;
  printf("Adjecency list of vertex",x);
  while(p)
  {
  printf("->%d",p->dest);
  p=p->next;
  }
  printf("\n");
  }

}
void main()
{
int v,i,a,b;
struct graph *g;
clrscr();
printf("enter no of nodes");
scanf("%d",&v);
 g=create_g(v);
for(i=0;i<v;i++)
{
printf("enter values of node & its addjacent");
scanf("%d%d",&a,&b);
addedge(g,a,b);
}
print(g);

getch();
}

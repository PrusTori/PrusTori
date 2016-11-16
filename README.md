 #include <conio.h>
#include <iostream>
struct element {
int x; element *Next; 
};
 class List {
         element *Head; public:
List() {Head=NULL;} ~List(); 
void Add(int x); void Show();
};
    List::~List() 
{
   while (Head!=NULL) 
{ 
element *temp=Head->Next; 
delete Head; 
Head=temp; 
}
}
}
 
void List::Show() 
{
element *temp=Head; 
 while (temp!=NULL) {
cout<<temp->x<<" "; 
temp=temp->Next; 
     }
}
 void main()
{
int N; 
int x; 
List lst; 
      cout<<"N = ";cin>>N; 
 for (int i=0;i<N;i++)
{
cout<<i+1<<". x = "; cin>>x; 
lst.Add(x); 
}
 lst.Show(); 
_getch()
}


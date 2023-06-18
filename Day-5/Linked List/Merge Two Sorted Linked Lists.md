# Merge two sorted linked lists

~~~
Node<int>* sortTwoLists(Node<int>* a, Node<int>* b)
{
 if(a == NULL) return b;
 if(b == NULL) return a;
 
 Node<int> *head=NULL, *tail=NULL;
 if(a->data <= b->data)
 {head=tail=a; a=a->next;}
 else
 {head=tail=b; b=b->next;}

 while(a!=NULL && b!=NULL)
 {
  if(a->data <= b->data)
 {tail->next=a; tail=a; a=a->next;}
 else
 {tail->next=b; tail=b; b=b->next;}
 }
 
 if(a==NULL) tail->next=b;
 else tail->next=a;
 
return head;
}
~~~

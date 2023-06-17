# Reverse linked kist

~~~
LinkedListNode<int> *reverseLinkedList(LinkedListNode<int> *head) 
{
    if(head==NULL) return NULL;

    LinkedListNode<int>*p=NULL,*c=head,*n=head->next;

    while(c!=NULL)
    {
        c->next=p;
        p=c;
        c=n;
        if(n!=NULL)n=n->next;
    }
    return p;
}
~~~

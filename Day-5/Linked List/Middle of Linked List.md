# Middle of linked list


~~~
// TC:- O(n)
// slow and fast pointer approch
Node *findMiddle(Node *head) {
    if(head==NULL) return NULL;
  Node *slow=head, *fast=head;
  while(fast != NULL && fast->next != NULL)
  {
     slow=slow->next;
     fast=fast->next->next;
  }
 return slow;
}
~~~

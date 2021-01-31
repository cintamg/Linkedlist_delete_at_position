# Linkedlist_delete_at_position
To delete an element at a specified position from a linked list.
SinglyLinkedListNode* deleteNode(SinglyLinkedListNode* head, int position) {
if(head==NULL)
return head;
SinglyLinkedListNode* temp=head;
SinglyLinkedListNode* newnode;
if(position==0)
{
    newnode=head;
    head=head->next;
    free(newnode);
}
else 
{
while(position-1>0)
{
    temp=temp->next;
    position--;
}
newnode=temp->next;
temp->next=newnode->next;
free(newnode);
}
return head;

}

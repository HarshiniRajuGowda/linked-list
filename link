#include <stdio.h>
#include <stdlib.h>
struct Node 
{
    int data;
    struct Node* next;
};
void insertAtEnd(struct Node** head, int data);
void deleteNode(struct Node** head, int key);
void reverseList(struct Node** head);
void displayList(struct Node* head);
int main() 
{
    struct Node* head = NULL; 
    insertAtEnd(&head, 10);
    insertAtEnd(&head, 20);
    insertAtEnd(&head, 30);
    insertAtEnd(&head, 40);
    printf("Original List: ");
    displayList(head);
    deleteNode(&head, 20);
    printf("After Deletion of 20: ");
    displayList(head);
    reverseList(&head);
    printf("Reversed List: ");
    displayList(head);
    return 0;
}
void reverseList(struct Node** head) 
{
    struct Node *prev = NULL, *current = *head, *next = NULL;
    while (current != NULL) 
    {
        next = current->next;
        current->next = prev;
        prev = current;
        current = next;
    }
    *head = prev;
}
void displayList(struct Node* node) 
{
    while (node != NULL) 
    {
        printf("%d -> ", node->data);
        node = node->next;
    }
    printf("NULL\n");
}

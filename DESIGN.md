 Homework 4: Design Document

  * author: samssonn gebreslassie
  * date: 07 feb 2025

   ### intro:
   In this assignment, I will implement the core functions of a basic text editor using C. The 
editor will manage text using a linked list structure while supporting operations such as 
appending, inserting, deleting, and replacing lines. Additionally, I will implement an undo 
feature using a stack-based approach.

#1 ll_text *append_text(ll_text *list, char *text)

- This function adds a new node at the end of the linked list.if the list is null there will 
be a new node that will return,otherwise traverse to the last node. I will use strdup to 
creater a heap allocated copy of the text, then return the originial herad of list story. 
 

#2 ll_text *insert_text(ll_text *list, char *text, int position)

- it will inserts a new node at the given position. if the position is 0, the new node will 
become the new head. otherwiste traverse the list to position - 1.Uses strdup to allocate a 
fresh copy of text. Returns the updated list head.

#3 ll_text *delete_text(ll_text *list, int position)

- this will removes the node at the given position. If deleting the head , we update the head 
to the next node. Otherwise, we traverse again , update its next pointer, and free the node If 
the list becomes empty,null is returned.

#4 ll_text *replace_text(ll_text *list, char *text, int position)

- it replaces the text at the specified node. Traverses to the specified position. Frees the 
old text and assigns a strdup copy of the new text.
- Returns the head of the list.

#5 ll_text *duplicate_ll_text(ll_text *list)

- Creates a deep copy of the linked list.  Iterates through the original list, copying each 
node and its text.The new list has the same structure but independent memory allocations.
Returns the head of the new linked list.

#6 int ll_text_length(ll_text *list)

- Counts the number of nodes in the linked list. Iterates through the list, incrementing a 
counter. If list is NULL , returns 0.

#7 ll_text_stack *push_duplicate(ll_text_stack *stack)

- Pushes a new stack entry containing a deep copy of the current text list. Allocates a new 
stack node. Uses duplicate_ll_text to copy the current top text. Returns the new stack top.

#8 ll_text_stack *push_empty(ll_text_stack *stack)

- Creates a new stack entry with an empty text list. Allocates a new ll_text_stack node with 
null text. Updates the stack pointer to point to the new entry. Returns the new stack top.

#9 ll_text_stack *pop_stack(ll_text_stack *stack)

- Removes the top entry of the stack. Frees the associated ll_text list and stack node Returns 
the next node as the new top.  If the stack is empty after popping, returns null.


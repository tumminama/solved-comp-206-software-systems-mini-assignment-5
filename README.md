Download Link: https://assignmentchef.com/product/solved-comp-206-software-systems-mini-assignment-5
<br>
Linked Lists and Modular Programming




This assignment explores malloc, makefile, modular programming, and git.




The central problem you will solve is a linked-list like the one shown in the lecture slides. You do not need to use the lecture slides.




Construct a modular program from three sources files: main.c, list.c and list.h.  The file main.c will be used to call the functions provided by the file list.c.  The file list.c builds a private linkedlist within the list.c named space.  The file list.h contains the definition of the list’s node structure. Use #ifndef to protect the possible multiple inclusion of list.h, as we talked about in class.




Use a makefile to compile your assignment. Use git to version control the development of your assignment. To prove that you used a makefile submit your makefile file. To prove that you used git, save the output from git log into a text file and submit that file.




The program will run as follows:

<ul>

 <li>The main() function uses a while loop accepting only positive integer numbers (n&gt;0) from the user. The loop terminates once the user enters a non-positive value. The user is prompted for each number one at a time.</li>

 <li>In the loop, main() calls functions from the list.o named space that creates a private linked list using malloc.</li>

 <li>The following function signatures are supported by list.c:

  <ul>

   <li>void newList();

    <ul>

     <li>This function assumes there is a private global linked-list pointer in list.c called head that is used to point to the beginning of a linked-list. This function call simply initializes this pointer to NULL.</li>

    </ul></li>

   <li>int addNode(int value);

    <ul>

     <li>This function mallocs a new node and copies the parameter value into the node. This function then adds the node to the head of the linked-list.  The function ends by returning true for success and false for failure. A node has the following structure: struct NODE { int data; struct NODE *next; }.</li>

    </ul></li>

   <li>void prettyPrint();

    <ul>

     <li>This function assumes a global pointer called head exists. Using this head pointer is traverses the linked-list printing all the values stored in the list.</li>

    </ul></li>

   <li>When the loop terminates the program prints to screen all the numbers in the list. The output should be in reverse order.</li>

   <li>The program then terminates.</li>

   <li>Do NOT use recursion.</li>

  </ul></li>

</ul>
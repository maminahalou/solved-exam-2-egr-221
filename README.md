Download Link: https://assignmentchef.com/product/solved-exam-2-egr-221
<br>
Data Structures in C++Exam 2

Name:

Instructions

This is Exam 2 for EGR 221. The exam is worth 63 points. Questions have their point values indicated.

Write your name in the space provided above. You are to circle the letter of the most correct answer or fill in the blank or use the space provided in questions requiring you to write an answer.

You may use your class notes, textbook, homework solutions as your reference.

1. (1 point) The following code segment correctly modifies the value of the variable num to 10.int num = 5;const int *p;p = &amp;num;*p = 10;A. trueB. false2. (1 point) In C++, a string literal (i.e., char sequence enclosed in double quotation marks) is stored in memory as a C-string.A. trueB. false3. (1 point) Copy constructors of a class are called when one uses the simple assignment statement (i.e., the = operator) to assign one object to another object of the class.A. trueB. false4. (1 point) In C++, destructors may return a value.A. trueB. false5. (1 point) In C++, the implementation file of a class template can be compiled independently of any client code.A. trueB. false6. (1 point) In C++, the compiler actually generates code for a function template when it encounters a call to the function.A. trueB. false7. (1 point) In C++, linked lists are random access data structures.A. trueB. false8. (1 point) The programmer must know in advance how many nodes will be needed in a linked list.A. trueB. false9. (1 point) A class containing one or more pure virtual function is an abstract class and cannot be instantiated.A. trueB. false10. (1 point) Given the following code segmentint *p, *q;p = new int[2];*p = 5;*(p+1) = 10;q = p;delete [] q;q = new int;*q = 15;if we try to carry out the statementcout &lt;&lt; *(p+1) &lt;&lt; endl;after the above code, what will be the output?A. 5.B. 10.C. 15.D. Maybe a strange value. In fact, since the dynamic memory pointed by p has been deallocated, weshould not use the cout statement to output *(p+1) any more.11. (1 point) Given a C-string defined bychar name[9] = {‘M’, ‘a’, ‘s’, ‘o’, ‘n’, ‘ ’};which of the following integers will be returned by strlen(name)?A. 5B. 6C. 8D. 912. (1 point) Here is the prototype for a template function:template &lt;class Item&gt;void func(Item x);Which is the right way to call the func function with a double argument a?A. func( a );B. func&lt;double&gt;( a );C. func&lt;Item&gt;( a );D. func(&lt;double&gt; a );13. (1 point) Consider the following definitiontemplate &lt;class Item&gt;Item smaller(Item a, Item b){if (a &lt; b)return a;elsereturn b;}What restrictions are placed on the Item data type for a program that uses the smaller function?A. The Item data type must be either int, double, or float.B. The Item data type must be one of the built-in C++ data types.C. The Item data type must have a copy constructor and a &lt; operator defined.D. None of the above restrictions apply.14. (3 points) Without actually executing the program in Visual C++, what do you expect the output of the following code segment to be?int *p, *q;p = new int;*p = 6;q = p;*q = 8;q = new int;*q = 9;cout &lt;&lt; *p &lt;&lt; ” ” &lt;&lt; *q &lt;&lt; endl;

15. (3 points) Without actually executing the program in Visual C++, what do you expect the output of the following code segment to be?int x;int *p, *q;p = new int[10];q = p;*p = 10;for (int j = 0; j &lt; 9; j++){x = *p;p++;*p = x + j + 1;}for (int k = 0; k &lt; 10; k++){cout &lt;&lt; *q &lt;&lt; ” “;q++;}

16. (3 points) Givendouble *listA, *listB;listA = new double[5];listA[0] = 2.15;listA[1] = -1.27;listA[2] = 3.14;listA[3] = 10.5;listA[4] = -2.27;Write a code segment that implements deep copy of listB from listA.

17. (4 points) Consider the following class declaration:class Student{public:Student(const char last[ ] = “”, const char first[ ] = “”,const int id = 0 );Student(const Student&amp; source); // This is the copy constructor~Student( );… // Other member functions

private:char *lastName;char *firstName;int ID;};(a) Write the code for the definition (i.e., implementation) of the copy constructor. Hint: Here you may assume that the cstring header file has already been included, and consequently functions such as strlen, strcpy, strcat may be used . Their prototypes are shown as follows for your information:size_t strlen ( const char * str );char * strcpy ( char * destination, const char * source );char * strcat ( char * destination, const char * source );

(b) Write the code for the definition (i.e., implementation) of the destructor.

18. (3 points) Consider the following class declarationclass SalaryType{public:SalaryType(const SalaryType&amp; source); // This is the copy constructor~SalaryType( );

const SalaryType&amp; operator = (const SalaryType&amp; source); // overloading// assignment operator… // Other member functions

private:double *salary; // salary points to a dynamic array containing// the salaries of the employees in the company// i.e., the size of the dynamic array is numOfEmployeesint numOfEmployees; // number of employees in the company};Write the code for the definition (i.e., implementation) of the operator = function. (Hint: Here you need to pay attention to avoid self-assignment. You may need to use the this pointer which is a special built-in pointer that points to the instance of the class making the function call. )

19. (4 points) Consider the definition the following function templatetemplate &lt;class Type&gt;Type choice(Type x, Type y, Type z){if ( ((x &lt;= y) &amp;&amp; (y &lt;= z)) || ((x &lt;= z) &amp;&amp; (z &lt;= y)) )return x;else if ( ((y &lt;= x) &amp;&amp; (x &lt;= z)) || ((y &lt;= z) &amp;&amp; (z &lt;= x)) )return y;elsereturn z;}(a) What is the expected output of the following statement?cout &lt;&lt; choice(7, 4, -5) &lt;&lt; endl;

(b) What is the expected output of the following statements?string str1 = “Orange”;string str2 = “Cherry”;string str3 = “Watermelon”;cout &lt;&lt; choice(str1, str2, str3) &lt;&lt; endl;

20. (4 points) Consider the definition the following function template:template &lt;class Type&gt;Type func(Type list[], int size){Type x = list[0];Type y = list[size – 1];

for (int j = 1; j &lt; size / 2; j++){if (x &lt; list[j])x = list[j];if (y &gt; list[size – 1 – j])y = list[size – 1 – j];}

return x + y;}Further suppose that you have the following declarationsint list[10] = {4,2,10,18,14,19,25,13,21,35};string strList[] = {“One”, “Three”, “Six”, “Five”, “Two”, “Four”};(a) What is the expected output of the following statement?cout &lt;&lt; func(list, 10) &lt;&lt; endl;

(b) What is the expected output of the following statements?cout &lt;&lt; func(strList, 6) &lt;&lt; endl;

21. (4 points) Consider the following declarationtemplate &lt;class Type&gt;class Surprise{…private:Type a;Type b;};(a) Write a statement that declares sObj to be an object of type Surprise such that the private data members a and b are of type int.

(b) Write a statement that shows the declaration in the class Surprise to overload the operator != as a member function.

(c) Assume that two objects of type Surprise are equal if and only if their corresponding data members are equal. Write the definition of the function operator != for the class Surprise, which is overloaded as a member function.

22. (3 points) Using the SortedList class (sorted array-based list) you learned in lectures (items are sorted in ascending order), without actually executing the program in Visual C++, what do you expect the output of the following program to be if we enter the 5 strings as:Mazda Toyota Isuzu Honda Mitsubishi

#include &lt;iostream&gt;#include &lt;string&gt;#include “SortedList.h”using namespace std;

int main(){SortedList&lt;string&gt; stringList;string str;

cout &lt;&lt; “Please enter 5 strings: “;for (int counter = 0; counter &lt; 5; counter++){cin &gt;&gt; str;stringList.insert(str);}

for (int counter = 0; counter &lt; stringList.getLength();counter++)cout &lt;&lt; stringList[counter] &lt;&lt; endl;

return 0;}

23. (4 points) Consider an Animal class as follows//**********************************************************// SPECIFICATION FILE (Animal.h)// This file gives the specification of an Animal class.//**********************************************************#ifndef ANIMAL_H#define ANIMAL_H#include &lt;iostream&gt;#include &lt;string&gt;#include &lt;iomanip&gt;using namespace std;

class Animal{public:Animal(int id = 0, string s = “”, int k = 1){ ID = id; name = s; key = k;}

void print(){cout &lt;&lt; setw(8) &lt;&lt; ID &lt;&lt; setw(15) &lt;&lt; name &lt;&lt; endl;// setw is right-justified}

bool operator ==(const Animal&amp; other) const{ return (ID == other.ID); }bool operator !=(const Animal&amp; other) const{ return (ID != other.ID); }bool operator &lt;(const Animal&amp; other) const{if (key == 1)return (ID &lt; other.ID);elsereturn ( (name &lt; other.name) ||((name == other.name) &amp;&amp; (ID &lt; other.ID)) );}bool operator &lt;=(const Animal&amp; other) const{if (key == 1)return (ID &lt;= other.ID);elsereturn ( (name &lt; other.name) ||((name == other.name) &amp;&amp; (ID &lt;= other.ID)) );}bool operator &gt;(const Animal&amp; other) const{if (key == 1)return (ID &gt; other.ID);elsereturn ( (name &gt; other.name) ||((name == other.name) &amp;&amp; (ID &gt; other.ID)) );}bool operator &gt;=(const Animal&amp; other) const{if (key == 1)return (ID &gt;= other.ID);elsereturn ( (name &gt; other.name) ||((name == other.name) &amp;&amp; (ID &gt;= other.ID)) );}

private:int ID;string name;int key;};

Using the SortedList class (sorted array-based list) you learned in lectures (items are sorted in ascending order), the following program is given to you.#include &lt;string&gt;#include “SortedList.h”#include “Animal.h”using namespace std;

int main(){int key;cout &lt;&lt; “Enter the key (1 or 2): “;cin &gt;&gt; key;SortedList&lt;Animal&gt; zooAnimal;Animal animal1(1238, “Penguin”, key);zooAnimal.insert(animal1);Animal animal2(1138, “Panda”, key);zooAnimal.insert(animal2);Animal animal3(1078, “Tiger”, key);zooAnimal.insert(animal3);Animal animal4(1003, “Panda”, key);zooAnimal.insert(animal4);Animal animal5(1357, “Monkey”, key);zooAnimal.insert(animal5);

cout &lt;&lt; “The animals in the zoo are:
”;for (int i = 0; i &lt; zooAnimal.getLength(); i++)zooAnimal[i].print();cout &lt;&lt; endl;

return 0;}

Assuming that the list does not allow duplicate items, and no message will be shown to alert the user if the insert item already exists or the remove item cannot be found. Without actually executing the program in Visual C++, show your expected outputs for the above program when you enter the key as(a) 1

(b) 2

24. (3 points) Using the UnsortedList class (unsorted array-based list) you learned in lectures, write a function sublist which extracts elements that are smaller than a given item from the given list and forms a new list. The precondition of the function is: the list has been initialized and is not empty. The postconditions are: newList contains all the items of the list whose values are less than the given item. Implement the sublist function as a friend function of the UnsortedList class whose declaration is:friend void sublist(const UnsortedList&lt;ItemType&gt;&amp; list,const ItemType&amp; item,UnsortedList&lt;ItemType&gt;&amp; newList);(Hint: The UnsortedList class has private membersItemType list[MAX_LENGTH];int length;and the member functions getLength, resetList, insert, remove, etc.)

25. (3 points) Consider the linked list shown in the following figure. Assume that the nodes are in the usual info-next form. (Assume that first, p, q, and last are pointers to NodeType; NodeType is a struct consisting of an integer member variable info and a pointer variable next.) What are the outputs of the following statements?

(a) cout &lt;&lt; p-&gt;info;

(b) cout &lt;&lt; q-&gt;next-&gt;next-&gt;info;

26. (3 points) Consider the linked list given in Problem 25. Write a C++ code segment to insert a node containing the integer value 65 after the node pointed by q. (You may introduce additional pointers to NodeType.)

27. (3 points) Consider the linked list given in Problem 25. Write a C++ code segment to delete the node pointed by last. (Be sure to adjust first or last if necessary.)

28. (3 points) Without actually executing the program in Visual C++, what is the expected output of the following C++ code segment? Assume that the nodes are in the usual info-next form with the info of type int. (list and ptr are pointers to NodeType.)list = new NodeType;list-&gt;info = 18;ptr = new NodeType;ptr-&gt;info = 15;ptr-&gt;next = NULL;list-&gt;next = ptr;ptr = new NodeType;ptr-&gt;info = 25;ptr-&gt;next = list-&gt;next;list-&gt;next = ptr;ptr = list;while (ptr != NULL){cout &lt;&lt; ptr-&gt;info &lt;&lt; ” “;ptr = ptr-&gt;next;}
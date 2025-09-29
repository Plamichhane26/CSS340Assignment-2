Assignment Instructions – please read carefully.
1. This is a group assignment. You should work in groups of at most two students.
• You should work on the whole assignment together.
• You should not just partition the work between you.
• You should upload only one submission to canvas.
• You may check your team member on Canvas under People → Assignment Groups.
2. Written Parts:
• Please type your answers and hand them in as a PDF file through Canvas.
• Please type your answers for parts 1 & 4 and hand them in as a single PDF file
through Canvas.
• You should use a diagramming platform or program to create your class diagram.
• Please include your full names on the first page of the PDF.
• DO NO include the PDF file in the ZIP file, please submit it separately on
Canvas.
3. Coding Parts:
• Hand in all program source files softcopy using Canvas
• Be sure that they properly execute. Failure to do so will mean that your program
is not graded.
Note: assignments are graded using the terminal and C++11 standard.
• All source files should be compressed into a ZIP archive.
• Use the following naming format:
<firstNameLastname1>_<firstNameLastname2>_asmt<#>.zip.
Example: SaraElAlaoui_JaneDoe_asmt2.zip
• You must use the code provided on Canvas.
• Your ZIP file should include: (1) the folder LinkedBagDS, (2) EventTicketMain.cpp,
(3) all the classes .cpp and .h files, and (4) sample inputs/outputs input01.txt
and output01.txt, if you choose to do the extra credit part.
4. Please refer to the university integrity policy on the syllabus, and remember
that you should be able to explain and reproduce any code you write and
submit as part of this assignment.
1
CSC 340 Assignment 2 September 18, 2025
Assignment Goals and Objectives
1. Programming methodology:
• Analyze problem requirements.
• Generate a class diagram from the problem requirements.
2. C++ implementation:
• Implement classes, including base and derived classes.
• Analyze the linkedBag implementation of ADT Bag (similar to List).
• Implement functions to manipulate LinkedBags.
Problem definition
You will implement a simplified version of an event-ticketing system. Your program should
include:
1. a complete implementation of the main function,
2. definition and implementation files (.h and .cpp) for each class needed in the program,
3. at least one instance of inheritance,
4. an implementation of two additional functions to the linked-list implementation of the
ADT Bag (LinkedBag), and
5. at least one instance of using each of these functions in your program.
2
CSC 340 Assignment 2 September 18, 2025
Application requirements { EventTicket340
This is a very simple event-ticketing application that only implements one main aspect:
managing an organizer’s events.
Your application should allow a user to perform the following tasks:
1. create a profile: username, email address, password, short bio, and profile picture (a
string storing the path to an image),
2. display their information (it should not display their password),
3. modify their password,
4. create a new event,
5. display all their events,
6. display their kth event (e.g. their 3rd event),
7. modify an event: the organizer specifies the index of the event and can modify the
name and description,
8. Sell a ticket to an event (see specification below),
9. delete an event.
Events: Each event has a name, description, rating, and a count of how many tickets have
been sold. The application has two types of events: Virtual and Venue.
1. VirtualEvent
• In addition to the information above, a virtual event also has a streamLink and
audience.
• Selling tickets: When you sell a ticket to a virtual event, there is no capacity
update, but you should provide the user with a one-time access code.
2. VenueEvent
• In addition to the general information of an event, a venue event has a venue,
dateTime, and a capacity.
• Selling tickets: Unlike virtual events, when selling for a venue event you need to
check if seats are available. If successful, decrement capacity; otherwise, report
sold-out.
Organizer events: An organizer’s profile can only have one list containing all their events
(i.e. do not create two lists, one for VirtualEvent and one for VenueEvent).
Additional requirements: You must use LinkedBag instead of C++ standard libraries
like vector. Add two new functions (defined in Part 3) to LinkedBag.cpp to meet the
application’s requirements. All lists of objects should be stored and manipulated using
LinkedBag.
3
CSC 340 Assignment 2 September 18, 2025
Part 1 { 25 points, Due September 23rd
Generate a Class Diagram for your application using UML.
• It should include the following classes:
1. EventTicket340,
2. Organizer,
3. Event,
4. VirtualEvent,
5. VenueEvent
• Read the program requirements carefully to extract members of each class.
• The diagram should be created using software (not hand-drawn).
Note 1 : LinkedBag is a data structure separate from your program, so it is not to be
included in the class diagram.
Note 2 : https://draw.io/ is a great platform for creating diagrams.
Part 2 { 50 points Implement the classes identified in the diagram.
1. Main program source file: a skeleton of main is provided. It prints a menu with user
actions.
2. Header and source files for each class. Implementations should match the UML dia-
gram.
Part 3 { 20 points
Modify LinkedBag.cpp to add:
1. bool reverseAppendK(const ItemType& newEntry, const int& k): adds the ele-
ment to the kth position starting from the end of the LinkedBag, or to the beginning
if k is out of range.
2. Node<ItemType>* findKthItem(const int& k): returns a pointer to the kth element
from the beginning of the LinkedBag.
Part 4 { 15 points
Choose 2 OOP principles, describe how they are used in your program, and why they are
important.
Extra Credit { 5 points
Provide one non-trivial test case with sample input and expected output. Save input in
input01.txt and expected output in output01.txt. Include them in your ZIP.

Download Link: https://assignmentchef.com/product/solved-lab-program-3-pointers-strings-integers-cop3502-cs-1
<br>
Given an input file that contains a number of lists specified as the first number in the file and wherein each list will consist of a number of elements in the list, and a list of integers, or a list of strings, in any order, create a <em>singly linked list </em>of the numbers or in a separate list, the strings – and so on for however many lists there are in the input file. Then once the lists are completely linked, total the numbers in the mode described below. Likewise, concatenate the strings as described below. These tasks should be accomplished using <em>pointer manipulations only</em>, that is arrays are not allowed. Also, make sure to demonstrate good memory management techniques.

<h1>1          Objectives</h1>

1.1     Inputs

There are two basic inputs, the input file name, passed via the command line, and the input file data defined below.

<h2>1.1.1       Command Line arguments</h2>

The input file name will be input as follows:

<ul>

 <li>pointerFun filename.ext</li>

 <li>In the event that the input file is not available or there is an error finding the file, an appropriate error message shall be displayed. Use the example below for guidance.</li>

 <li>pointerFun ERROR: File “bogusFilename” not found.</li>

</ul>

<h2>1.1.2      Input File fields</h2>

The first line of the file will have a single positive integer <em>k</em>, representing the number of lists in the file. Each list will follow. The <em>first </em>line of each list will have an integer number that represents the number of elements to be read and added to the <em>linked list </em>created for this list of inputs. The <em>linked list </em>should preserve the order in which the elements are read in.

Please note that it is incumbent upon the program to determine if the list contains <em>strings </em>or <em>integers</em>. The input file will contain the appropriate number of elements corresponding to the <em>number </em>of elements specified for the test case.

HINT: If the list is a list of strings, it would be highly advantageous to create a <em>linked list structure </em>that contained a pointer to the <em>malloc’ed </em>string buffer. A list of integers could contain a <em>linked list structure </em>that contains <em>integer </em>data.

The input file, shown below, will <em>NOT </em>include comments. The comments and line spacing shown below are for <em>clarification</em>.

2                            //Number of test cases

4                                  //The count of numbers in the list

6                                //First number in the list

<ul>

 <li>//Second number in the list</li>

 <li>//Third number in the list</li>

 <li>//Fourth number in the list</li>

</ul>

4                                    //The count of strings in the list

“blue” //The first string in the list

“dog” //The second string in the list

“red” //The third string in the list

“cat” //The fourth string in the list

The actual file’s data would be as shown below:

2

4

6

4

5

6 4 blue dog red cat

<h1>2          Process</h1>

The program can assume that once a list of <em>integers </em>or <em>strings </em>has begun, the rest of the list will be of the appropriate type. That is a list of <em>integers </em>will always contain <em>integers </em>thru the end of the list. This will also be true for <em>strings</em>.

Also note that the program will have to <em>walk </em>the <em>singly linked list </em>to get every other element, then walk the list again to get the elements that were not totaled or concatenated in the first pass.

In the event the list contains <em>strings </em>make sure to create an output buffer that will be large enough for <em>every </em>string and the <em>terminating NULL</em>.

<h1>3          Outputs</h1>

The output of the program will be for however many lists were read in <em>and </em>the corresponding data for each list.

For the data shown above the outputs are shown below.

The total of the odd numbered numbers 6, 5 is 11

The total of the even numbered numbers 4, 6 is 10

The concatenation of (blue, red) is “blue red” The concatenation of (dog, cat) is “dog cat”
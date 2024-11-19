## Guidance
Answer the following questions considering the learning outcomes for Week 09

Make sure to record evidence of your processes. You can use code snippets, screenshots or any other material to support your answers.

Do not fill in the feedback section. The Founders and Coders team will update this with feedback on your progress.

## Assessment
 ### 1. Show evidence of some of the learning outcomes you have achieved this week.
> **[Learning outcomes...]**  
> [your evidence here]

This week was a reading week, which I took the time to learn with the Mircosoft and FreeCodeCamp acreditation for C#. Following along with the course I have completed the first part of the basics module:

> - Learning to write your first C# code

Using ```Console.WriteLine("Hello World!")``` to return ```Hello World``` in the console.

Learning that there is a difference with ```Console.WriteLine("Hello World!")``` , which returns the string with a new line after it and ```Console.Write("See you later!")``` which returns a string with the same line of another ```Console.Write```. 

For example:

```
Console.WriteLine("Hello!");
Console.Write("Have a good day.");
```

Will return:

```
Hello!
Have a good day.
```

Whereas if you used: 

```
Console.Write("Hello!");
Console.Write(" ");
Console.Write("Have a good day.");
```

Returns all statements on the same line. 

```
Hello! Have a good day.
```

Furthermore, C# requires you to add a semi-colon at the end of each line, which differs greatly from JavaScript which will understand that there is an implied semi-colon, and still allow code to run. 


> - Store and retrieve data using literal and variable values in C#

In C# you create a new variable by declaring the data type of the variable, then naming it. This seemed similar to typestript where the data type is written first. 

```
string firstName;
firstname = "Bob";
int age;
age = 30;
```

This code can also be further refactored:

```
string firstName = Bob;
int age = 30;
```

> - Perform basic string formatting in C#

This included using carriage and tab escape to formate strings on new lines ```\n``` or with tab spacing ```\t```. 

Concatenation and using string value via interpolation:

```Console.WriteLine($"Hello {firstName}!" + " you are {age} years old.")```

> - Guided project - Calculate and print student grades


Using all the basics in being taught in C# helped to complete the guided project to produce the expected answer.

```
Student     Grade
Sophia      94.6  A
Nicolas     83.6  B
Zahirah     83.4  B
Jeong       95.4  A
```

I think this was a good project to really break down a problem and how to solve it. Firstly, with the provided code, I tackled how to calculate the sum of each student, then the average, then format the scores and the students to get the above table. This really helped in prioritising how to break down a problem, and which part needs the most attention first. 


 ### 2. Show an example of some of the learning outcomes you have struggled with and/or would like to re-visit.
> [**Learning outcome...**]  
> [your evidence here]

I would like to, and will aim to complete the C# acreditation with FreeCodeCamp. I think it would be beneficial to continue understanding the language more in depth. 


## Feedback (For CF's)
> [**Course Facilitator name**]

Alexander

> [*What went well*]

Excellent practical learning of C# basics, with clear code examples demonstrating understanding of syntax differences from JavaScript. Good breakdown of the student grades project showing systematic problem-solving approach.

> [*Even better if*]

Include more specific challenges you encountered while learning C#, and outline a concrete plan for completing the FreeCodeCamp certification with particular areas you want to focus on.

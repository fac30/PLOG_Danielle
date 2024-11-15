## Guidance
Answer the following questions considering the learning outcomes for
- [Week 010](https://learn.foundersandcoders.com/course/syllabus/developer/week10-project05-DOTNET-intro/learning-outcomes/)

Make sure to record evidence of your processes. You can use code snippets, screenshots or any other material to support your answers.

Do not fill in the feedback section. The Founders and Coders team will update this with feedback on your progress.

## Assessment
 ### 1. Show evidence of some of the learning outcomes you have achieved this week.
> **[Learning outcomes...]**  

This week I have:

> - Learn how to create and run a project in .NET

With this week, I have spent the time learning about C# and .Net using the Microsoft acreditation course with Freecode camp. I would say my experience with this course has been pretty good. The materials have been comprehensive and easy to follow along. 

> - Learn C# basics

Learning C# basics has been a good experience. I think there are similarities with other languages (like JavaScript and React) that has helped with the transition in writing C# code. I think its been comprehensive enough that I've managed to follow along with the course and to skip ahead to the 'Create web apps and services with ASP.NET Core, minimal API, and .NET' course during this week. I feel like I managed to understand enough from the basics without being completely confused or unable to follow along.  

> - Learn to test an ASP.NET project with Swagger

Using Swagger was a great learning curve in solidifying my understanding with API's and endpoints, as well as being a good way to test directly in the browser without having to use Postman. 

Using Swagger I have: 

> - Managed to understand how to manipulate the json file within my PUT and my POST route.
> - I also managed to GET and DELETE what I had updated with my POST and PUT. 
> - I managed to understand how to persist data and to see it interact with my database on VScode.
> - I used enpoints to see my json on the local server.
> - Debug any issues as the status codes are presented. 

<img width="690" alt="Screenshot 2024-11-14 at 13 17 09" src="https://github.com/user-attachments/assets/8b14736a-5779-46fb-8f04-9c07c0d6f0a9">

Learning how to use minimal API's have also been helpful in visualising alongside swagger. I have used ChatGPT to help with further understanding and also creating other routes such as a post route to further understand syntax. 

For example:

```
var builder = WebApplication.CreateBuilder(args);
var app = builder.Build();

app.MapPost("/name", () => "Hello Danielle!");

app.Run();

```
Being able to change the type of route I want for a minimal API is very simple. Follwing C# syntax, I would modify the ```app.MapPost``` line of code to ```app.MapGet``` to a get request, or ```app.MapDelete``` to delete for example.

As a stretch goal, I am currently learning how to build a full stack application using both react and .NET, using a minimal API. This has been a really interesting experience especially as I am learning about a new software called Docker. 

<img width="667" alt="Screenshot 2024-11-14 at 13 20 59" src="https://github.com/user-attachments/assets/db1035bd-cfac-44a5-9f1b-20a412bea71b">

With Docker I have:

> - Created a container
> - Run and stopped a container
> - Created an image
> - Connected with my VScode so that changes are made / deployed to my docker container automatically.

I recognise that Docker is a timely stretch goal in implementing with my team, but I am interested in the theory of how I could implement it in future projects. I would like to explore it further. 

 ### 2. Show an example of some of the learning outcomes you have struggled with and/or would like to re-visit.
> [**Learning outcome...**]  
> [your evidence here]

As I am taking on backend this week, I am pleased to be able to discover new learnings on the backend and the database. I want to try to improve my knowledge on the EF core models used for database tables. I aim to implement this myself and to see it in action as I complete the fullstack stretch goal. 


## Feedback (For CF's)
> [**Course Facilitator name**]  
> [*What went well*]  
> [*Even better if*]

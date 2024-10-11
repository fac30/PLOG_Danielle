## Guidance
Answer the following questions considering the learning outcomes for
- [Week 05](https://learn.foundersandcoders.com/course/syllabus/developer/week05-project03-test-deploy/learning-outcomes/)

Make sure to record evidence of your processes. You can use code snippets, screenshots or any other material to support your answers.

Do not fill in the feedback section. The Founders and Coders team will update this with feedback on your progress.

## Assessment
 ### 1. Show evidence of some of the learning outcomes you have achieved this week.
> **[Learning outcomes: ]**

> - Gain experience in using the Cypress testing library with React

I tested the frontend of our app with Cypress, and created tests to nagivate the user journey successfully. 

<img width="355" alt="Screenshot of Cypress test" src="https://github.com/user-attachments/assets/95d60aee-9aec-4c6a-a99e-1ae9c00d2710">
 
> - Understand how and when to use component and end to end tests

My painpoint when it came to testing was the fact that our button component did not have a selector for me to be able to 'get' it on the page. 

My original test did not work: 
```
it('should find the button on the first page', () => {
    cy.get('button') 
  });
```

I separated this test from the rest of my testing with it.only, and found a solution:

```
it.only('checks for a button labeled "Start"', () => {
      cy.contains('button', 'Start') 
        .should('be.visible') 
        .click();
    });
```
By using cy.contains what the syntax was actually checking for relied primarily on the content:

```
cy.contains(selector, content)
``` 

Because there was no selector but the content was present ('Start'), my test successfully passed, and could then be re-introduced back into the e2e testing body. 


> - Understand how to write maintainable and readable test cases

By going through the previous steps, breaking down the testing into managable chunks helped to refactor it so that it covered the user journey. Once I'd established one test the following tests used the same logic.  

> - Gain experience in deploying a full-stack web application to a cloud platform

I found learning about AWS quite interesting and actually quite fun. I thought it was easy enough to use, and to get solutions when something went wrong. I managed to deploy both a front end and full stack project onto the platform with minor issues within the workshop. After the security scare I have also made note to turn of my instance. 

> - Understand the differences between development, staging, and production environments

I think this was a pretty straightforward concept to follow, and reflected the cycle of the three weeks of our project. 

> - Gain experience in using a continuous integration and deployment (CI/CD) pipeline.

I believe I achieved this with using Cypress, and continually having to update my testing when I faced issues such as no selector, or making sure that the url path for the next page when clicked through was correct. 

 ### 2. Show an example of some of the learning outcomes you have struggled with and/or would like to re-visit.
> [**Learning outcome...**]

I think looking back over the learning outcomes, what I would like to re-visit is understanding the backend testing. Even though I have used postman, I would like to gain more practice by using it in a more practical way like I did with cypress for our project. I also enjoyed using AWS more than I anticipated so that is something I would like to explore more in the future.  

## Feedback (For CF's)
> [**Course Facilitator name**]  
> [*What went well*]  
> [*Even better if*]

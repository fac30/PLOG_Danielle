## Guidance
Answer the following questions considering the learning outcomes for
- [Week 04](https://learn.foundersandcoders.com/course/syllabus/developer/week04-project03-frontend/learning-outcomes/)

Make sure to record evidence of your processes. You can use code snippets, screenshots or any other material to support your answers.

Do not fill in the feedback section. The Founders and Coders team will update this with feedback on your progress.

## Assessment
 ### 1. Show evidence of some of the learning outcomes you have achieved this week.
 The main focus of the week was Frontend development and using React. From in looking at the learning outcomes for the week I would say I achieved the following: 
> **[Learning outcomes]**  
> - Understand the concepts of components, props, and state in React.

I had some previous experience of React, however it had been a long time since using it. Despite this, I would say that I felt able to pick up the concepts and theory after practicing with the challenges and asking my peers for help. I would like to revist it to further solidify my understanding, and to explore more of the documentation around states and hooks.

> **[Software Architecture: ]**
> - Draw a diagram representing the flow of our application

This week was my first time properly using Figma and implementing / translating the ideas from the wireframe I created towards the components created with react. Using figma in creating the blueprint of the app's appearance was really helpful as it visually helped in seeing the types of components needed.

My process in creating components in figma, was to identify what would need to be consistent across each page of our app. Starting with the buttons, I created one button and then copied it over as many times as I needed for a page's design and then created a component for that. I did the same for the app display screen, then combined it with the buttons component to make one big component overall: 

<img width="152" alt="Screenshot 2024-10-04 at 11 21 03" src="https://github.com/user-attachments/assets/06f94e09-2b77-4df5-812b-433e2556bbb5">

Once I had done this, it was easy to then add the component to each screen of our app. Components were also created for the colors, and this was done for the background of the pages as well as the color of the buttons. In our tailwind config file, we created a 'root variable' colour, similar to what you would create in a css file, for the buttons which then made it easy to copy and paste in our tailwind code: 

<img width="665" alt="Screenshot 2024-10-03 at 12 50 18" src="https://github.com/user-attachments/assets/e1ae88ea-3e7d-4a91-90c1-a920fee40870">

Code for our buttons, as well as a custom font that we used for the screen display: 

```
export default {
  content: ["./index.html", "./src/**/*.{js,ts,jsx,tsx}"],
  theme: {
    extend: {
      colors:{
        'home-background': '#0F1A2E',
        'button-colour': '#FDC206',
        'background-gradient': '#3054AE',
      },
      fontFamily:{
        custom:["Pacifico", "sans-serif"],
      },
    },
  },
  plugins: [],
};
```

The tailwind we aplied to each of our pages for our background: 

```
 <div className='bg-gradient-to-b from-home-background to-background-gradient min-h-screen flex flex-col items-center justify-center text-white'>
```

The code that references the button concistency with our classes: 
```
return  <Button  label={option} key={option + index} onClick={()=>{handleClick(option)}} classes={buttonStyle} />
```

Using the wireframe this helped with creating components quickly in react which then helped with: 


> - Follow a consistent pattern for naming our folders, files and variables
>

Because of the wireframe, it was easy to discuss and establish what each page of the app should be named which then helped with paths between each page when following the user journey. We named files after the wireframe.   

Overall I would say I enjoyed the frontend week more than the backend. I think the concept of react is easier for me to understand as I interpret it as a 'reference' system. e.g. you import what you need from the react library, then you use the hook, then you export that component, then you import it in the app etc etc..
I also enjoyed learning about tailwind for the first time and found it really easy to understand and implement. I found the syntax quite intuitive, and enjoyed how much it cut down when compared to using a css file.

 ### 2. Show an example of some of the learning outcomes you have struggled with and/or would like to re-visit.
> [**Learning outcome...**]
> - Learn how to integrate TypeScript with a React

I would say that I would like to revist this a little better, as I havent felt that I've managed to implement typescript outside of react. I think its a concept I would like to build a better foundation on. 

Overall I would like to revisit all of the learning outcomes as I find it interesting, but just haven't had the time to play around with it. 

## Feedback (For CF's)
> [**Course Facilitator name**]

Alexander

> [*What went well*]

Good examples of your learnings, I like the combination of code snippets and screenshots.

> [*Even better if*]

You could go a bit more technical. I am not sure about your learnings on react

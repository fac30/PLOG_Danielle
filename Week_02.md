## Guidance
Answer the following questions considering the learning outcomes for
- [Week 02](https://learn.foundersandcoders.com/course/syllabus/developer/week02-project02-chatbot/learning-outcomes/)

Make sure to record evidence of your processes. You can use code snippets, screenshots or any other material to support your answers.

Do not fill in the feedback section. The Founders and Coders team will update this with feedback on your progress.

## Assessment
 ### 1. Show evidence of some of the learning outcomes you have achieved this week.

The main learning objectives for this week were primarily backend development, and looked a lot more into testing and asynchronous Javascript. 
From the learning outcomes I would say that I achieved the following: 

> * Writing code that executes asynchronously:
```
const array = [];
array.push('How do I feel? ')
setTimeout(() => array.push('Still not my favourite, but better than I thought'),500)
array;
```

I would say I understood from the execute programme what the setTimeout and clearTimeouts functions did, and could understand how they worked when returning code. After this I think it got a lot more challenging to understand the syntax, especially when it came to stacking .then() functions inside the setTimeout.
 
> * Use of the .map method

I didn't use the map method, but I understand it and why its needed from previous learnings on the execute programe. There wasn't a need for me to use it, but I understand it. 

> * Node.js set up

I have been familiar with node as well as npm previously in a personal project, so I felt okay in getting to grips with revisiting and relearning about its importance. 

> * Testing of our function.

Testing of our function mostly happened with pair programming, and just seeing if a connection could be established between the server and the openAI. Once that was established, testing between the server and the discord bot was disconnected from me, until everything was tested through the server. 

> * * Writing tests in the workshops:

When it came to testing, I would say I mostly achieved the majority of it within pair programming to get the server connected to the openAI. Personally, I would say the workshops was where I did more of my own testing which didnt seem as complicated as I thought. Understanding that testing just needs to be as simple as testing for both an expected and unexpected item helped to clear up my understanding of how hard it would be. I think thats an improvement on last week as there was a lack of testing for the project, but because there was no visual element this week, it was necessary.  

Overall, I would say looking at the learning outcomes, I achieved more than I expected but maybe not as much when it came down to the learning objectives for the js section. Instead what I would say is that I achived the following instead: 

> * Reasearching about the OpenAI calls and what it does:

The platform document helped a lot, and provided a good blueprint to get our openAI to work. The javascript syntax was a lot easier to manage than I expected. What I found interesting was the code snippet: 

```
messages: [
        { role: "system", content: "You are a helpful assistant."}
        {"role": "user", "content": "write a haiku about ai"}
    ]
```
I think it really helped in realising that a lot of the work in changing the system's personality was as easy as changing its content. Even though this wasn't done in our group, I think it would be interesting to explore what you could come up with in the future, and if it would stay consistent. It also added helpful context for how much of the backend I couldn't see. As the openAI all it was achieving was the connection between the information(server) and the user, and all I had to do was just change the system content to fit the expecations of the user.   

> * Understood a little more about the relationship between npm and node:

Node.js is used to run javascript locally, whilst npm is the 'package manager' where you can get/source other people's code for a project. 

> * Wrote and learned about the code needed to get an openAI call to work
>   * and then modifying the code to add a 'content' function to our system's responses:
>
```
let conversationHistory = [
  { role: "system", content: "You are a helpful assistant." }
];

async function chatPrompt(message) {

  conversationHistory.push({"role": "user", "content": message})

  try {
    const completion = await openai.chat.completions.create({
      model: "gpt-3.5-turbo",
      messages: conversationHistory,
      temperature: 0.7,
    });

    const chatResponse = completion.choices[0].message.content;

    conversationHistory.push({"role": "assistant", "content": chatResponse});

    console.log("Assistant Response:", chatResponse);
    return chatResponse;

  } catch (error) {
    console.error("OpenAI Error:", error);
    return "I'm sorry, I encountered an error while processing your request.";
  }
}
```

>     
> * Pair programmed when it came to solving errors and testing the openAI call.

This again helped with understanding the connection between the server and the openAI, and making sure that it was getting the relevant information correct. 

I think overall what I learned was still valuable in approaching backend development. I had limited knowledge beforehand, but I think it still helped with understanding the context of what we were trying to achieve. Learning about the openAI and changing its code was not as daunting as I anticipated it would be, and it seemed to just be like vanilla js when it came down to understanding what each part did. 



 ### 2. Show an example of some of the learning outcomes you have struggled with and/or would like to re-visit.
> * Use the fetch method to make HTTP requests and receive responses
> * Configure the options argument of the fetch method to make GET and POST requests
> * Write tests to mimic the behaviour of a user performing different actions
> *  Organise tests using descriptive names and groupings to clarify their purpose and outcomes

I would say I would like to revist a bit more about asynch functions in javascript. Although I would say I have an understanding about the why and the reasonings about using a asynch function, I don't think I felt very comfortable in understanding them as much as I would like. The execute programme felt confusing at times, especially when it was going through a lot of other methods before finally showing us another way to use async functions with the async and await partnership. 

## Feedback (For CF's)
> [**Course Facilitator name**]  
> [*What went well*]  
> [*Even better if*]

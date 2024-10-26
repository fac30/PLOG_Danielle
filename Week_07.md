## Guidance
Answer the following questions considering the learning outcomes for
- [Week 07](https://learn.foundersandcoders.com/course/syllabus/developer/week07-project04-authentication/learning-outcomes/)

Make sure to record evidence of your processes. You can use code snippets, screenshots or any other material to support your answers.

Do not fill in the feedback section. The Founders and Coders team will update this with feedback on your progress.

## Assessment
 ### 1. Show evidence of some of the learning outcomes you have achieved this week.
> **[Learning outcomes...]**
 
>  - Understand the principles of authentication and authorisation in web applications

I would say that I have a good grasp of the principles of authentication from reading the workshop material. Learning about hashing and salting passwords really helped me to understand and gain a depth of knowledge on how webpages handle senstive data, and why its good practice to make sure that user data is secured. Following on from this, though I didnt put much practice into establishing authentication, I felt confident in asking questions because I felt I had a good blueprint of knowledge to work from. 

I would say outside of the set learning outcomes, I have:
>- improved my debugging skills. 
>- managed to successfully connect to a backend api. 

During this week I have been focused on connecting our front end to our backend api so that our dropdown menu is able to be populated with our atists name, and then when you click on that artist name, their data populates the artist page. 

<img width="352" alt="Screenshot 2024-10-18 at 12 52 48" src="https://github.com/user-attachments/assets/7b6b10c5-6928-447f-897c-6b0af0b8c8df">

<img width="352" alt="Screenshot 2024-10-24 at 10 05 08" src="https://github.com/user-attachments/assets/a7c027d8-1c93-4260-b2b1-625abeca3001">

I anticipated our first problem which was a a CORS issue as the frontend and backend were on different local hosts. Our frontend was running on 5173 and our backend was running on 3000. However when it came to amending our CORS origin, we were only pulling in data from our instance. However because the instance was running from our frontend, and our frontend did not have any data, this meant that there was just no data being pulled. 

<img width="352" alt="Screenshot 2024-10-24 at 12 04 47" src="https://github.com/user-attachments/assets/dc521edf-c81b-4865-b76c-f71803aa93eb">

This meant having to modify our origin to an ```* universal selector``` temporarily.

After the CORS issue was rectified, problems were still on the frontend, as the endpoints established caused confusion. 

On our backend server, ```localhost:3000/artists``` worked, and provided the names of all our artists in our database. When providing an id endpoint, e.g. ```localhost:3000/artists/1``` this failed. However when removing the ```s``` from artists the backend enpoint worked:


<img width="310" alt="Screenshot 2024-10-26 at 15 25 05" src="https://github.com/user-attachments/assets/ed266746-fecd-4d89-9f2d-3065f4bff203">

<img width="310" alt="Screenshot 2024-10-26 at 15 25 35" src="https://github.com/user-attachments/assets/5053b140-f194-414f-aee3-d59ff6066703">

<img width="310" alt="Screenshot 2024-10-26 at 15 27 53" src="https://github.com/user-attachments/assets/a6407fb4-64b6-4a28-82ef-1c792e110c63">

<br />

However, after establishing the correct semantics for the word artist, in the front end there was still an issue as the id endpoint was returned as undefined when clicking on the dropdown of the artist names. Trying to manually change the endpoing also resulted in an error as there was still no data coming from the backend for the artists id. Looking closer at the backend and how we called the data solved the issue. 

<img width="352" alt="Screenshot 2024-10-24 at 11 44 59" src="https://github.com/user-attachments/assets/ef8248e2-4784-497a-888a-2b69d1fffbea">

As we were specific in only calling the name endpoints from our database, it mean we were not calling the id data. Once this was rectified, our endpoints were no longer undefined and selecting from the dropdown menu would result in the artist endpoints being both name and id ```localhost:5173/artist/1```. 


 ### 2. Show an example of some of the learning outcomes you have struggled with and/or would like to re-visit.
> [**Learning outcome...**]

- I would say that I would probably like to put into practice the authentication side of things. I wouldn't say I struggled with understanding it, but I would like to use it practically.

- I would also like to practice more my react hooks, props etc. I think it was a challenge to debug the issue that we had because I kept trying to see things from a components perspective. Also, as we didnt have a homepage, it was a challenge to try and establish that a route also had to be created from our navbar as this was what needed to lead us to individual artist pages.

- I would also like to delve more into useContext. I am a little unsure of how this project may need to implement it, but I would like to build my knowledge both practically and theoretically in it. 

## Feedback (For CF's)
> [**Course Facilitator name**]  
> [*What went well*]  
> [*Even better if*]

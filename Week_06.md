## Guidance
Answer the following questions considering the learning outcomes for
- [Week 06](https://learn.foundersandcoders.com/course/syllabus/developer/week06-project04-databases/learning-outcomes/)

Make sure to record evidence of your processes. You can use code snippets, screenshots or any other material to support your answers.

Do not fill in the feedback section. The Founders and Coders team will update this with feedback on your progress.

## Assessment
 ### 1. Show evidence of some of the learning outcomes you have achieved this week.
> **[Learning outcomes]**  
> - Be comfortable with SQL syntax and how to use SELECT and INSERT queries

I would say I have found SQL clear and straightforward to learn from execute programme. Thought I havent been able to put it into much practice, I think the syntax has been concise and logical.

> - Gain proficiency in using React to create dynamic and responsive user interfaces

This week as I have focused on the frontend, I'd say that my comprehension in react has grown and I have been able to revise a lot of ideas I had previously encountered, though using it alongside typescript has been pedantic as I have to remember to make it 'typescript compliant'. 

The overall goal for the frontend was to make a mvp before presenting on Thursday. Taking this step by step, I started by using the figma designs for our website project as a reference for what could become components, where I would need functionality, and how I could establish routes that mimicked our user journey.

<img width="342" alt="Screenshot 2024-10-17 at 12 13 23" src="https://github.com/user-attachments/assets/e502c43d-fc99-498c-9a41-bbe9e93ab003">

<img width="342" alt="Screenshot 2024-10-17 at 12 13 40" src="https://github.com/user-attachments/assets/216f1e86-23c7-4d32-821e-cb15ce76f91a">

With the artist page, I focused on creating components for the navigation bar, and then the gallery as these were both that I felt would be more in demand with the progression of the project. 


Gallery Code snippet: 

```

const Gallery: React.FC = () => {
    const images: ImageData[] = [
        {src: "https://th.bing.com/th/id/R.80048c94faacac8b7ff6af18efa3d92a?rik=Ac82coHKVHLVyg&riu=http%3a%2f%2fwonderfulengineering.com%2fwp-content%2fuploads%2f2016%2f01%2fnature-wallpapers-8.jpg&ehk=GoUR7nA3jNm0gIdWFJoMVL1iu%2bJuWOU7Nu7KkgKZzeQ%3d&risl=&pid=ImgRaw&r=0", caption: "Image One"},
{src: "etc etc"},
{src: "etc etc"},

    ];

    return ( 
        <section className="container m-28 py-4">
            <div className="grid grid-cols-3 gap-4">
                {images.map((image, index) => (
                    <div key={index} className="text-center">
                        <img 
                            className="h-40 w-full rounded-lg object-cover object-center md:h-60 shadow-lg" 
                            src={image.src}
                            alt={image.caption}
                        />
                        <p className="mt-2 text-gray-600">{image.caption}</p>

                        <Link to='/products'>
                        <button className='buttonStyling'>View More...</button> //styling component here
                        </Link>
                    </div> 
                ))}
            </div>
        </section>
     );
}

```

Within the gallery code I created a 3 column grid and applied styling for each of the images. The map function iterates over each image of the array, and returns a different image into each column. I used the gallery component twice to render a six grid gallery similar to our design in the artist page, however upon reflection I think it would be better to refactor the gallery component code to create a 6 grid gallery, and just populate it according to the amount of images needed on the page. 

```
<Layout>
      <ArtistBio />
      <Gallery />
      <Gallery />
</Layout>
```

For the button I use a styling component which made it easier to code and helped me to consider D.R.Y practices more and more. 

```
@layer components {
  .buttonStyling {
    @apply m-2 p-3 border-solid border-2 border-gray-900 hover:bg-gray-400
  }
}
```
Creating styling components really helped with following a consistency between both pages, and meant I could change all the elements without having to go through each component.

<img width="500" alt="Screenshot 2024-10-18 at 12 10 54" src="https://github.com/user-attachments/assets/6ccadd5a-ddeb-4533-8d54-e513546de1fa">

<img width="500" alt="Screenshot 2024-10-18 at 12 12 43" src="https://github.com/user-attachments/assets/3ed45279-dc1a-4437-bd9c-164ed068134c">


 ### 2. Show an example of some of the learning outcomes you have struggled with and/or would like to re-visit.
> [**Learning outcome **]

I would say one of the main challenges I have struggled with in react, is being able to translate the concept of how it seems that both js and html are on the same page. Before when HTML, CSS and JS were separate pages, it now seems that the code is blended into one and that you have to return a function instead of linking that function in a html file. Though I find components incredibly useful and helpful in separating the page more granularly into what section does what, and where I can render the compenent again, Ive also found it that sometimes I have fallen into a trap of turning an element into a component when it doesn't need to be a component and having to take a step back and think about best practices. 

For example our h1, navbar and footer need to be on every page but was missing when I was coding the product page. My initial thought was to make the h1 a component and to render it on every page alongside the navbar and footer. However after some research it was advised that though it made logical sense it was not best practice to have a component that only rendered a small piece of code. To solve this issue and to follow best practice I created a layout component instead, and absorbed the h1 into another bigger component:

```
const Layout: React.FC <{children: React.ReactNode }> = ({children}) => {
    return ( 
        <>
        <NavBar />
        <main>{children}</main>
        <Footer />
        </>
     );
}
 
```
Now in each of my pages all I have to ensure is that the layout component wraps around all of my return code. 

Another issue I had was linking of the pages. Initially I thought that the browser router needed to be imported on every page however this caused problems where the pages didnt render at all. For now, the simplest solution is:

```
<Routes>
  <Route path="/" element={<ArtistPage />} />
  <Route path="/products" element={<ProductPage />} />
</Routes>
```

Because there are only two pages, I have made the home route path the artists page and then the products page link to the products page. For now this is fine, but I am unsure whether this will run into problems as more pages are built out. 

On a further side note, I also had issues with link selections from our dropdown menu: 

<img width="390" alt="Screenshot 2024-10-18 at 12 52 48" src="https://github.com/user-attachments/assets/7c555cb9-203e-4821-88c9-8167f596b011">

Though there is no page with content it still rendered the h1 element on a blank page. This was fine because it meant the routes did work, but then after removing the import browser router from the navbar component, it 'broke' and failed to render the h1. This is because you cannot add a <Link /> to a custom elements like ```<li>```, but you **can** for DOM elements (e.g. divs, buttons, span etc). This meant having to wrap that specfic li in the dropdown in the navigation component in a div. 

I think overall I have vastly improved my react skills, but I would like practices on fully nailing down the syntax and the functions without as much LLM help. 

Moving foward, I would like to also put into practice sql and database knowledge. 

## Feedback (For CF's)
> [**Course Facilitator name**]  
> [*What went well*]  
> [*Even better if*]

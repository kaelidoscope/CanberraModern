# Canberra Modern - 11841 Project 2 
https://canberramodernkael.netlify.app/

## Development Process
### Setup
After attending the in-class tutorials, I felt rather confident in being able to tackle the assignment task. When finally sitting down to play around with the Nuxt frame work and divvy up some website pages and code, I ran into a few errors. At first, I thought these were due to the initial setup I had used to create my project directory, which resulted in a cavalcade of Russian nesting dolls of folders-within-folders-within-folders, etc. 
After troubleshooting those, I kept receiving an error message when attempting to install the yarn dependencies. When I finally read the error message, I discovered it was due to my PC's execution policies being set to restricted. This was circumvented with a simple CLI code:

`Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser`

This enabled me to install the yarn dependencies, and launch the Nuxt builder on a local server.
        
> Snaps for Elle Woods!

After all that, I double-checked the repository was working with GitHub and began coding.

### Pages
I ran into some trouble with extrapolating the dynamic page routing using Nuxt. After attempting to recreate the data sync, I ended up seeking help. During a 1-on-1 Zoom tutorial with Ben, we discovered I was using an outdated template for rendering the page contents after fetching the API data. 

After fixing the `<script>` code and correcting the file names, the pages all loaded from the data.
I then edited the `index.vue` file, as Nuxt uses this as the landing page for the project. 

I added the Canberra Modern Logo, and copied the text inside the `<p>` tags from the current Home Page.

### Nav Component
I then had to edit the Navigation component and attempt some styling. I managed to find some documentation that explained how to use CSS styling to create an interactive navbar in Nuxt. I edited the code to apply the Canberra Modern colour palette to the styling, and corrected the positioning to make it more aesthetic according to UxD principles. I also made sure the Nuxtlink file pathways were correct.

### CSS Styling
I created an assets folder to hold both the CSS and images folders. I copied the Canberra Modern Logo into `images` folder and created a new `style.css` file. I then edited the `nuxt.config.js` file to use the new global stylesheet. Inside the stylesheet, I attempted to recreate the Canberra Modern style guide, giving the heading tags their own property values, and importing a URL to download the Futura BT font face.

### Final Editing
After a bit of time had passed, I dove back into the project to make sure the pages looked decent enough, and that the links and images all loaded correctly.
While the finished project feels a bit basic, I'm not mad at what I've produced, as I did feel like I struggled a lot with some of the Framework concepts and Nuxt coding and terminology. Searching for inspiration online seemed only to add to the confusion, and I definitely feel I was able to follow along better with video tutorials and demonstrations.

### Deploying the Project
To deploy my project, I used the `yarn build` command in the CLI terminal to generate the static site. I then followed along with the [Netlify & Nuxt](https://explorers.netlify.com/learn/get-started-with-nuxt/nuxt-generate-and-deploy) Tutorial outlined in the Canvas Modules, and used Netlify to drag & drop my `/dist` folder onto NETLIFY deployment site. The resulting URL: [Kael's Canberra Modern](https://canberramodernkael.netlify.app/) website. 

## Design Inspiration
As far as inspiration goes, I didn't investigate too thoroughly. I was more invested in having a functional API project above anything else. The few sites I did look at featured on the [Nuxt Showcases](https://nuxtjs.org/showcases/) site were:

- [Zernonia](https://www.zernonia.com/) Transitions and Neomorphism I liked.
- [Monopo|London](https://monopo.london/) Interactive backgrounds, transitions, and design layout.
- [Part Time Studio](https://part-time.studio/) Interactive capabilities and component designs.

## Final Reflection
Grasping with a lot of the concepts of rendering dynamic data, and frameworks was more challenging than I expected. I do feel at times I was either deviating too wide from the tutorial exercises I was following along with, or just making careless syntax/spelling errors that would break the coding when I tested it. 
I would have like to stylise the site a bit more, like adding transitions between pages, and displaying images of the buildings listed would have catered more towards the project brief. 
I did tend to confuse myself or overreach some of the inner workings of the framework, but will endeavour to implement some of the more exciting style options and trends available in Project 3. 
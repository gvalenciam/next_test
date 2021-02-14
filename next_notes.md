# Create app

- npx create-next-app ${app_name}

# Run server (inside project folder)

- npm run dev

# Create new route (https://www.mywebpage.com/new-route)

- Add js file inside pages folder (pages/new-route.js)
- Works for nested routes (pages/new-route-group/new-route.js)

# Navigate through pages

- Use **Link** component to wrap the <a> tag
- Add **href** attribute in the Link component
- Add other attributes such as className to the <a> tag

# Static assets

- Every static asset goes inside the public directory

# Images

- Use the **Image** component from Next
- Image optimization, lazy load, resposiveness are handled

# Metadata (title)

- Use the **Head** component from Next

# CSS

- CSS can be added using **modules**
- Create a css file with the extension **module.css** and import it inside the component to style
- SASS is also supported but extra config is needed

# Global CSS

- Create a **pages/\_app.js** file
- Create top level **styles** folder and add a **global.css** file
- Import the **global.css** file into the **pages/\_app.js**

# Static generation with data

- Create component and add the async function **getStaticProps**
- This functions can fetch external data and pass **props** parameter to the component

# Server Side Rendering (SSR)

- Create component and add the async function **getServerSideProps**
- Receives **context** parameter that contains request specific parameters (req, res, query, etc)
- Should return a **props** object (required), **notFound** boolean (optional) and **redirect** optional object ({destination: string, permanent: boolean})

# Dynamic URLs

- Next build app → getch external data → generate pages
- Create file with [] name ([id.js]) inside the pages folder
- Add the async function **getStaticPaths** → that returns all the possible values for the path name (id)
- Implement **getStaticProps** to fetch the data. This function receives {params} with the path name (id)

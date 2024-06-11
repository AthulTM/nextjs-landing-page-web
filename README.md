Next.js Web Application

This is a simple web application built with Next.js that fetches data from a RESTful API and displays it in a user-friendly manner. The application implements Static Site Generation (SSG) and includes responsive and interactive user interfaces.

Features:
Server Site Rendering (SSR): Efficiently fetches data from the API during build time.
API Integration: Fetches data from a public API using fetch by using SSR.
Responsive UI: Ensures the application is accessible on various devices.
Interactive Elements: Includes a search bar for enhanced user experience.
Performance Optimization: Implements lazy loading for images and optimizes resource loading.
Framer Motion Cool Animations: I include the framer motion & gsap as well animation which makes the website visual appealing and cool.
Project Setup
Prerequisites
Ensure you have the following installed on your local machine:
Node.js (v12 or higher)
npm (v6 or higher) or yarn (v1.22 or higher)
Installation
Clone the Repository:
git clone https://github.com/AthulTM/nextjs-landing-page-web
cd my-next-app


Install Dependencies:
npm install
# or
yarn install

Run the Development Server:
npm run dev
# or
yarn dev


Open http://localhost:3000 with your browser to see the result.

Building and Running for Production
Build the Application:
npm run build
# or
yarn build

Start the Production Server:
npm start
# or
yarn start


Project Structure
nextjs-webapp/
├── components/
│   ├── Header.jsx
│   ├── TableList.jsx
│   ├── Footer.jsx
│   └── [Other Components]
├── pages/
│   ├── index.js
│   └── _app.js
├── public/
│   └── [Static Files]
├── styles/
│   ├── globals.css
│   └── I used the tailwind css
├── .gitignore
├── package.json
├── README.md
└── [Other Config Files]




API Integration
This project uses a public API to fetch data. The data is fetched using Axios and displayed on the homepage. Error handling is implemented to manage API request failures.
Example API

We use a sample public API from the  Placholder json "(https://jsonplaceholder.typicode.com/users)"
Static Site Generation
We use Next.js's SSR to fetch data during build time. This ensures faster load times and better SEO.
// pages/index.js
import axios from 'axios';

const getData = async () => {
  const response = await fetch('https://jsonplaceholder.typicode.com/users');
  if (!response.ok) {
    throw new Error('Failed to fetch data');
  }
  return response.json();
};



User Interface Development
The UI is built using HTML, CSS, and JavaScript. It includes:
A main layout with a header, main content area, and footer.
A search bar for filtering posts.
Lazy loading for images to optimize performance.
Data Integrity and Optimization
We ensure data integrity by validating the data fetched from the API.


Documentation

Setup Instructions: Included in the installation section.
Libraries Used: Listed in package.json.
Challenges Faced: Documented in this README.
Challenges Faced
API Rate Limiting: Implemented error handling to manage rate limits and ensure the application remains functional even if the API fails.
Responsive Design: Ensured the application is responsive across different devices by testing on various screen sizes.
Performance Optimization: Achieved through SSG and lazy loading.
Conclusion
This Next.js web application efficiently fetches and displays data from a public API with enhanced user experience through interactive elements and performance optimizations.
For any questions or further information, please feel free to contact me.
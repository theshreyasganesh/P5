# P5
Project 5 - Team STANN
# Photo Sharing Application
This project is a Single Page Application (SPA) built using ReactJS and Material-UI. It allows users to view a list of users, view details of a specific user, and explore photos uploaded by users. The application utilizes React Router for navigation and provides a Master-Detail pattern layout.
# Setup
Make sure you have Node.js and npm installed on your system. If not, follow the installation instructions in Project 0. Clone the repository and navigate to the project directory. Run the following command to install the required dependencies:

npm install
Start the web server and the webpack build process using the following command:


node webServer.js & npm run build:w
Access the application at http://localhost:3000/photo-share.html.

# Problem 1: Implement Photo Sharing Application
Components:
# UserList:
Displays a list of user names.
Clicking on a name switches the content view to display the details of that user.
# UserDetail:
Displays detailed information about a user.
Includes a link to switch the view area to the photos of the user.
# UserPhotos:
Displays all photos belonging to a specific user.
Shows each photo, its creation date/time, and associated comments.
Comments include the date/time, user name, and comment text.
User names in comments are clickable and lead to the user detail page of the respective user.
# TopBar:
Displays your name on the left side.
Reflects the current context on the right side (user's name or "Photos of [user's name]").
# Problem 2: Fetch Model Data from Web Server
Implemented a function FetchModel(url) in lib/fetchModelData.js to fetch model data from the web server using XMLHttpRequest. The function returns a Promise that resolves with the response data or rejects with an error object containing HTTP status and statusText in case of an error.

Modified components to use the FetchModel function to request data from the server. Removed direct accesses to window.models.

# API Endpoints:
/test/info: Returns version information.
/user/list: Returns a list of users.
/user/:id: Returns details of a specific user.
/photosOfUser/:id: Returns photos belonging to a specific user.
# Extra Credit: Advanced Features
Introduced "Enable Advanced Features" checkbox in the toolbar.
When enabled, the application displays a single photo at a time with stepper functionality to navigate through the user's photos.
Implemented bookmarking and sharing of individual photos using browser's URL.
Handled deep linking to individual photos, ensuring the stepper functionality works as expected.
# Project Structure
components/topBar/TopBar.css: Styles for the top bar component.
components/topBar/TopBar.jsx: Implementation of the top bar component.
components/userDetail/userDetail.css: Styles for the user detail component.
components/userDetail/userDetail.jsx: Implementation of the user detail component.
components/userList/userList.css: Styles for the user list component.
components/userList/userList.jsx: Implementation of the user list component.
components/userPhotos/userPhotos.css: Styles for the user photos component.
components/userPhotos/userPhotos.jsx: Implementation of the user photos component.
lib/fetchModelData.js: Functionality to fetch model data from the web server.
photo-share.html: HTML file loading the React application.
photoShare.jsx: Main entry point for the React application.
styles/main.css: Global styles for the application.
# Running the Application
Ensure Node.js and npm are installed.
Clone the repository and navigate to the project directory.
Run npm install to install dependencies.
Start the web server and webpack build process: node webServer.js & npm run build:w.
Access the application at http://localhost:3000/photo-share.html.
# Additional Notes
Make sure to run ESLint before submitting the code.
The application uses Material-UI components for a consistent design.
Deep linking and navigation should work seamlessly, including browser refresh.
Enjoy exploring the Photo Sharing Application! 📸✨

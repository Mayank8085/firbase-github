# Firebase GitHub Integration Project

This project is a full-stack web application that integrates Firebase services with a React frontend to deliver secure authentication, real-time database interactions, and seamless hosting. Additionally, it utilizes the GitHub API to dynamically fetch and display repositories, providing an interactive interface that highlights user projects in real-time.

## Live Demo

Experience the application here: [Live Demo](https://mayankgithub.netlify.app/)

## Features

- **User Authentication**: Secure login and registration powered by Firebase Authentication.
- **Real-Time Database**: Efficient data storage and synchronization using Firebase Realtime Database.
- **Firestore Integration**: Structured data management and retrieval via Firestore.
- **GitHub API Integration**: Dynamically fetches and displays repositories from GitHub profiles.
- **Hosting**: Deployed using Netlify for fast, reliable, and scalable hosting.
- **Responsive Design**: Fully responsive design ensuring accessibility and usability across all devices.

## Technologies Used

- **Frontend**: React.js
- **Backend**: Firebase Realtime Database and Firestore
- **Authentication**: Firebase Authentication
- **Deployment**: Netlify
- **API**: GitHub REST API (for fetching repository data)

## Getting Started

To run this project locally, follow these steps:

### Prerequisites

- Node.js installed
- Firebase account setup
- GitHub account for API access

### Installation

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/Mayank8085/firbase-github.git
   cd firbase-github
   ```

2. **Install Dependencies**:

   ```bash
   npm install
   ```

3. **Configure Firebase and GitHub API**:

   - Create a Firebase project in the [Firebase Console](https://console.firebase.google.com/).
   - In the project directory, create a `.env` file and add your Firebase and GitHub configuration:

     ```env
     REACT_APP_API_KEY=your_api_key
     REACT_APP_AUTH_DOMAIN=your_project_id.firebaseapp.com
     REACT_APP_DATABASE_URL=https://your_project_id.firebaseio.com
     REACT_APP_PROJECT_ID=your_project_id
     REACT_APP_STORAGE_BUCKET=your_project_id.appspot.com
     REACT_APP_MESSAGING_SENDER_ID=your_messaging_sender_id
     REACT_APP_APP_ID=your_app_id
     REACT_APP_GITHUB_USERNAME=your_github_username
     REACT_APP_GITHUB_API_URL=https://api.github.com/users/
     ```

4. **Start the Application**:

   ```bash
   npm start
   ```

   Open [http://localhost:3000](http://localhost:3000) to view it in the browser.


## GitHub API Usage

The application leverages the GitHub API to fetch and display repositories dynamically. This functionality enhances the user experience by showcasing their latest GitHub projects in real-time. The API endpoint used is:

```bash
https://api.github.com/users/{username}/repos
```

### Example Code (Fetching GitHub Repositories):

```javascript
const fetchRepos = async (username) => {
  const response = await fetch(`${process.env.REACT_APP_GITHUB_API_URL}${username}/repos`);
  const data = await response.json();
  return data;
};
```

Repositories are dynamically listed on the page, providing real-time visibility into the user's project portfolio.


## Acknowledgements

- [Firebase](https://firebase.google.com/) for backend services.
- [React](https://reactjs.org/) for the frontend framework.
- [Netlify](https://www.netlify.com/) for hosting services.
- [GitHub API](https://docs.github.com/en/rest) for repository data.

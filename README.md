# EventFlow v2

[![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)](https://react.dev/)
![CSS](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JS](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

**EventFlow v2** is an enhanced React-based Event Management System, building on the success of the original EventFlow application. With new features such as event deletion, improved field validation, and real-time feedback, this version offers a more polished and comprehensive experience. Designed with React Router, it showcases advanced concepts like dynamic routing, state feedback, and seamless backend integration.

## Features

### EventFlow v2 Enhancements:

- Added support for deleting events.
- Improved input validation and error handling.
- Enhanced UI feedback for loading and submission errors.
- Optimized code for modularity and reusability.
- Added user Authentication using API tokens so users who aren't authenticated can't edit , delete or add new events and updated the UI accordingly

### Core Functionalities:

- **Create Events**: Add new events by providing a title, image URL, date, and description.
- **Edit Events**: Update existing event details dynamically with support for URL-based PATCH actions.
- **Delete Events**: Effortlessly remove events, complete with UI feedback for success or errors.
- **Form Validations**: Built-in validation for required fields and error prompts for invalid inputs.
- **Real-time Feedback**: Loading indicators during submission and graceful error handling on failures.

### Additional Features:

- **Dynamic Navigation**: Effortless redirection using `useNavigate()` for cancel actions or after form submissions.
- **State Feedback**: Real-time submission states via `useNavigation()`.
- **Error Boundaries**: Comprehensive error handling with fallback UI for invalid routes or server errors.
- **API Integration**: Reliable backend communication using `fetch()` for CRUD operations.
- **Reusable Components**: Modular React components for events listing, event detail views, and navigation.

### Authentication Features Used

- **Secure User Authentication**: Integrated backend authentication ensuring only authorized users can create, edit, or delete events.
- **JWT Tokens**: Utilizes JSON Web Tokens (JWT) for secure and scalable user sessions.
- **Token-based Communication**: Ensures that all frontend-backend interactions are authenticated and validated.
- **Protected Routes**: React Router protects event pages, redirecting unauthorized users to the login page.
- **User Session Handling**: Automatic session expiration and token management to maintain secure user sessions.

### React Router Concepts Utilized:

- **Dynamic Routing**: Conditional rendering of forms for new, edit, and delete actions.
- **`useNavigate()`**: Enables smooth navigation across different views.
- **`useNavigation()`**: Tracks form submission progress to provide feedback.
- **Action Functions**: Simplifies backend requests for creating, updating, and deleting events.
- **Form Component**: Utilizes React Router's `<Form>` for efficient form handling and validation.

### Project Overview :

- **Overview**:
  ![All Events Overview](/frontend/public/home.png)

- **Registration Overview**:
  ![All Events Overview](/frontend/public/register.png)

- **All Events Overview**:
  ![All Events Overview](/frontend/public/allevents.png)

- **Event Details Overview**:
  ![Event Details Overview](/frontend/public/event.png)

- **Edit Event Overview**:
  ![Edit Event Overview](/frontend/public/editevent.png)

- **New Event Overview**:
  ![New Event Overview](/frontend/public/newevent.png)

## Project Structure

```
EventFlow v2
│      package-lock.json
│      README.md
│
└───backend
│   │    .gitignore
│   │    app.js
│   │    events.json
│   │    package-lock.json
│   │    package.json
│   │
│   └─── data
│   │    events.js
│   │    users.js
│   │    util.js
│   │
│   └─── routes
│   │    auth.js
│   │    events.js
│   │
│   └─── util
│        auth.js
│        error.js
│        validation.js
│
└─── fronted
      │
      │  .gitignore
      │  package-lock.json
      │  package.json
      │  README.md
      │
      └───public -------> All Images's Sources
      │
      └─── src
         │   App.js
         │   index.js
         │   index.css
         │
         ├─── components
         │     AuthForm.js
         │     AuthForm.module.css
         │     EventForm.js
         │     EventForm.module.css
         │     EventItem.js
         │     EventItem.module.css
         │     EventsList.js
         │     EventsList.module.css
         │     EventsNavigation.js
         │     EventsNavigation.module.css
         │     MainNavigation.js
         │     MainNavigation.module.css
         │     NewsletterSignup.js
         │     NewsletterSignup.module.css
         │     PageContent.js
         │     PageContent.module.css
         │
         │
         ├─── pages
         │      Authentication.js
         │      EditEvent.js
         │      Error.js
         │      EventDetail.js
         │      Events.js
         │      EventsRoot.js
         │      Home.js
         │      Logout.js
         │      NewEvent.js
         │      Newsletter.js
         │      Root.js
         │
         ├─── util
         │      auth.js
         │
```

## Installation

To get started with the project locally:

1. Clone the repository:
   ```bash
   git clone https://github.com/SalahShallapy/EventFlow-v2.git
   ```
2. Navigate to the project directory:
   ```bash
   cd EventFlow-v2
   ```
3. Navigate to the backend directory:
   ```bash
   cd backend
   ```
4. Install backend dependencies:
   ```bash
   npm install
   ```
5. Run the backend server:
   ```bash
   npm start
   ```
6. Navigate out of the backend directory to the main project directory:
   ```bash
   cd ..
   ```
7. Navigate to the Frontend directory:
   ```bash
   cd frontend
   ```
8. Install Frontend dependencies:
   ```bash
   npm install
   ```
9. Run the project:
   ```bash
   npm start
   ```

## Note

- This project's backend is locally setup and is not running on a server so you have to follow the installing steps and start the backend server in order to see the fetched data on the frontend UI

## API Endpoints

### 1. Create Event (Add New Event)

curl -X POST http://localhost:8080/events

### 2. Update Event (Edit Existing Event)

curl -X PATCH http://localhost:8080/events/:eventId

## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks!

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

   <p align="right">(<a href="#top">back to top</a>)</p>

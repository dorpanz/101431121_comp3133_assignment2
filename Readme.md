README - COMP3133 Assignment 2 Submission



---

🔗 LINKS

1. **Frontend (Vercel):**  
https://101431121-comp3133-assignment2.vercel.app/login
2. **Backend (Railway):**  
https://101431121-comp3133-assignment2-production.up.railway.app/graphql

# Sample Login:
destowq - password1234

# COMP3133_Assignment2
 The goal of the assignment is to build a frontend application using Angular that communicates with a GraphQL backend. The application allows for user authentication, employee management (CRUD operations), search functionality, and file uploads.

The frontend will interact with the backend developed in Assignment I, which is responsible for handling data via GraphQL.

## Features

- **Login and Signup Screens**: Forms for user authentication with validation.
- **Session Management**: Store user session token to manage authentication state.
- **Employee Management**: 
  - View a list of employees.
  - Add, update, and delete employee records.
  - View employee details in a modal.
  - Search employees by department or position.
- **File Upload**: Ability to upload employee profile pictures.
- **Responsive UI**: Designed with Angular Material for a professional and responsive UI/UX.
- **Routing and Navigation**: Use Angular Router for navigating between components like login, signup, and employee management screens.
- **Logout and Redirection**: Clear session on logout and redirect to the login screen.

## GraphQL Integration

The frontend communicates with a GraphQL backend for employee management. The following GraphQL operations are supported:

- **Add Employee**: A mutation for adding a new employee.
- **Update Employee**: A mutation for updating employee details.
- **Delete Employee**: A mutation for deleting an employee record.
- **Get Employees**: A query for fetching the list of employees.
- **Search Employees**: A query for filtering employees by department or position.

### Example GraphQL Query

```graphql
query {
  getAllEmployees {
    _id
    first_name
    last_name
    email
    designation
    department
    salary
  }
}

```

### Example GraphQL Mutation

```graphql
mutation {
  addEmployee(
    first_name: "Dina"
    last_name: "Johnkl"
    email: "dina@gmail.com"
    gender: "Female"
    designation: "Manager"
    salary: 5000
    date_of_joining: "2024-02-15"
    department: "HR"
  ) {
    _id
    first_name
    last_name
    email
    department
  }
}

```

## Technologies Used

- **Angular**: For building the frontend application.
- **GraphQL**: For data fetching and interaction with the backend.
- **Angular Material**: For UI components and styling.
- **RxJS**: For handling asynchronous operations.
- **Bootstrap** (or custom CSS): For responsive layout and UI components.

## Authentication and Session Management

1. **Login**: After successful login, a user session token is stored in the service to manage user authentication.
2. **Logout**: Clicking the logout button will clear the session and redirect the user to the login screen.
3. **Session Persistence**: The session token is used for authenticated API calls.

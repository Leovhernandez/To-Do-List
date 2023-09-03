# To-Do-List

## Description
A comprehensive web application that assists users in organizing and managing their tasks. Built using Python (either Flask or Django) for the backend, ReactJS for the frontend, and PostgreSQL for data storage. Containerized for development and deployment using Docker and orchestrated using Kubernetes.

## Features & Functionalities:

User Authentication and Authorization:
- Registration: Allow new users to create accounts using an email and password.
- Login/Logout: Existing users can log in and out.
- Password Recovery: Users can recover forgotten passwords via email.

Task Management:
- Create: Users can add new tasks, set descriptions, and specify deadlines.
- Read: Display an organized list of tasks. Tasks close to their deadlines can be highlighted.
- Update: Users can edit existing tasks' names, descriptions, or deadlines.
- Delete: Remove tasks when they're completed or no longer needed.

Task Categorization:
- Categories: Tasks can be grouped into categories (e.g., Work, Personal, Urgent).
- Filtering: Users can view tasks by category.

Notifications & Reminders:
- Email Alerts: Send email notifications for tasks nearing their deadline.
- In-app Notifications: Display reminders within the app for upcoming tasks.

Search Functionality:
- Users can search for specific tasks using keywords.

Data Storage with PostgreSQL:
- Secure Storage: All tasks and user data are securely stored in a PostgreSQL database.
- Data Relations: Ensure data integrity with properly defined relations (e.g., a user has many tasks).

Responsive UI with ReactJS:
- Dynamic Rendering: The user interface dynamically updates as tasks are added, edited, or deleted.
- Mobile Responsive: The design adjusts for mobile and desktop views.

Containerization and Orchestration:
- Docker: Both frontend and backend components of the app are containerized using Docker, ensuring consistent environments for development, testing, and deployment.
- Kubernetes: Utilizes Kubernetes for orchestrating and scaling the application containers.

Extra Functionalities (Optional for advanced implementations):
- Task Prioritization: Users can prioritize tasks (High, Medium, Low).
- Collaboration: Allow tasks to be assigned to different users or share tasks with other registered users.
- Dark Mode: Provide a toggle to switch the app's theme.

## Getting Started

### Prerequisites

- Docker
- Kubernetes
- kubectl

### Installing

1. **Clone the repo**:
    ```bash
    git clone https://github.com/Leovhernandez/To-Do-List
    ```

2. **Navigate to the project directory**:
    ```bash
    cd To-Do-List
    ```

3. **Build Docker images**:
    ```bash
    docker build -t to-do-list/backend -f Dockerfile-backend .
    docker build -t to-do-list/frontend -f Dockerfile-frontend .
    ```

4. **Push Docker images**:
    ```bash
    docker push to-do-list/backend
    docker push to-do-list/frontend
    ```

5. **Deploy to Kubernetes**:
    ```bash
    kubectl apply -f backend-deployment.yaml
    kubectl apply -f frontend-deployment.yaml
    kubectl apply -f db-deployment.yaml
    ```

## Contributors
Leonardo Hernandez

## License
This project is licensed under the MIT License - see the (LICENSE.md) file for details

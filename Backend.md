# Communa - Frontend
Communa is a web3 platform for freelancing that connects businesses with talented professionals worldwide, making remote work more convenient than ever before. 
- [https://communa.network/](https://communa.network/)
- [https://github.com/communa](https://github.com/communa)

## Intro
The purpose of this document is to outline the technical requirements for a Node.js backend application that will serve API services for client applications written in Node.js and Typescript - a widely used technologies that provides static typing, enhances code readability and making it easier to maintain and scale. 

## Methodology

Our development prioritizes the development of an API before the UI offering now faster development cycles, improved scalability, and better collaboration. We concentrate on the core functionality without being concerned about the UI, which enables us to create a more robust and scalable API that can be utilized across various platforms and devices. And once the API is developed, we can build the UI around it, resulting in a more efficient and faster development process.

This involves designing and producing a set of API endpoints that our client applications can use to access and manipulate data.

## API endpoints

### Authentication

As part of our ongoing technical development, we have a one-click blockchain login authentication process involving: nonce generation, usage of wallets like MetaMask for user validation, transmitting data securely with JWT, and validating cryptographic signatures on Ethereum.

- Nonce:
    - GET **/auth/nonce**: This endpoint generates a unique nonce (number used once) that can be used to authenticate a user's request against the Ethereum blockchain.
- Refresh:
    - **POST /auth/refresh**: This endpoint allows a user to refresh their JSON Web Token (JWT) without having to log in again. JWTs are commonly used for authentication and authorization in web applications, and refreshing the token helps to maintain the user's session and prevent unauthorized access.
- Login:
    - **POST /auth/login**: lets users authenticate themselves with the system verify user credentials and grant access to protected resources.
- Registration:
    - **POST /auth/registration**: lets users register for a new account and store user information in the system.

### Users

- Searching:
    - **POST /user/search**: lets everyone search for other users based on various criteria such as name, location, interests, etc. This API can be clients find freelancers with needed skills and connect with them directly.
- Reading:
    - **POST /user/{id}**: lets everyone retrieve their profile information or the profile information of other users. This API can be used to display user profiles on a website or application or to retrieve user information for a variety of purposes.
- Editing:
    - **PUT /user**: lets both clients and freelancers update their profile information. This API can be used to allow users to change their profile picture, update their bio, or any other relevant information.
- Removal:
    - DELETE **/user**: lets users permanently delete their accounts and all associated data.

### Projects

We also need to unpublish projects that are older than 30 days, since they can clutter the platform and make it difficult for clients to find relevant and active projects.

- Searching:
    - **POST /project/search**: lets users search for job postings based on specific keywords. The API would accept a list of possible keywords to filter by and return a list of job postings that match the search criteria.
- Posting:
    - **POST /project**: lets employers post new job openings on the platform -  employers can provide details such as job title, description, location, salary range, and required qualifications.
- Editing:
    - **PUT /project/{id}**: lets employers make changes to existing job postings - employers would be able to update details such as job title, description, location, salary range, and required qualifications.
- Removal:
    - **DELETE /project/{id}**: lets employers remove job postings from the platform if a job opening has been filled or is no longer available.
- Applying:
    - **POST /project/{id}/apply**: lets freelancers apply for job openings directly through the platform. Freelancers would be able to submit their resumes and cover letter, and clients would be able to review and respond to applications.

### Time logging

These endpoints provide the necessary features for time-tracking to send reports of user activity, including searching, posting, editing, and removal of time-tracking reports.

- Searching
    - **POST /time/search**: this endpoint allows the freelancer to search for time-tracking reports based on the start and end time of the activity, as well as the project ID. The freelancer can specify the startAt and endAt parameters as Unix timestamps and the projectId parameter as an integer.
- Posting
    - **POST /time**: this endpoint allows the user to post a new time-tracking report. The user needs to provide the following information in the request body:
        - startAt: Unix timestamp of the start time of the activity
        - endAt: Unix timestamp of the end time of the activity
        - projectId: ID of the project associated with the activity
        - description: Optional description of the activity
- Editing
    - **PUT /time/{id}**: This endpoint allows a freelancer to edit an existing time-tracking report. The freelancer needs to provide the ID of the report in the URL, and the updated information in the request body. The freelancer can update the startAt, endAt, projectId, and description fields.
- Deleting
    - **DELETE /time/{id}**: this endpoint allows the freelancer to delete an existing time-tracking report. The user needs to provide the ID of the report in the URL.

### **Files**

- Uploading:
    - **POST /file:** this endpoint can be used to upload an image file. The request should include the image file as a binary payload. The response will include a unique identifier for the uploaded image.
- Editing:
    - **PUT /file/{id}: t**his endpoint can be used to update the metadata associated with an image. The request should include the updated metadata in the request body. The response will include the updated metadata.
- Reading
    - **GET /file/{id}:** this endpoint can be used to retrieve the metadata associated with an image. The response will include the metadata.
- Deleting:
    - **DELETE /file/{id}:** this endpoint can be used to delete an image. The response will indicate whether the deletion was successful.
    

## E-mails

Email notifications are an important tool for platforms to engage, retain, and acquire users, as well as to communicate with them effectively.

- Welcome email
    - Introduce your platform and provide a brief overview of how it works. Encourage freelancers to complete their profiles and start browsing available projects.
- Project updates:
    - Notify freelancers when new projects are posted that match their skills and interests. Include details about the project, such as the budget, timeline, and requirements.
- Proposal submission confirmation
    - Let freelancers know that their proposal has been received and is being reviewed by the client. Provide an estimated timeline for when they can expect to hear back.
- Project award notification:
    - Congratulate freelancers when they are awarded a project and provide details about the next steps, such as setting up a contract and payment terms.
- Payment reminders
    - Send reminders to clients and freelancers when payments are due or overdue. Include instructions on how to make a payment and any penalties for late payments.
- Feedback requests
    - Ask clients and freelancers to provide feedback on their experience using your platform. Use this feedback to improve your platform and attract more freelancers.
- Platform updates
    - Notify freelancers of any updates or changes to your platform, such as new features or improvements to the user interface. Encourage freelancers to provide feedback on these changes.

## Methodologies

### REST

Building modern web applications is made easier with the use of REST API, which is a widely accepted industry standard. REST APIs utilize HTTP as their underlying protocol, making them easily integrable with existing web technologies. They are lightweight, scalable, and simple to implement, making them the go-to choice for developers when building web applications. Additionally, APIs are highly secure, as they use standard HTTP protocols to transmit data.

### **CICD**

We use CIDC (Continuous Integration and Continuous Deployment) to automate the deployment process, ensuring that your application is always up-to-date and running smoothly. We also use GitHub for version control, making it easy to collaborate with your team and track changes.

### **Code Quality**

Linters and code quality are crucial on the backend side because the backend is responsible for handling sensitive data and performing complex operations. Any errors or bugs in the code can lead to security vulnerabilities, data breaches, and system failures. The code is often written by more then just one developer, making it more challenging to maintain consistency and readability. Linters help ensure that the code follows best practices, is free of syntax errors, and adheres to a consistent style. This not only improves the quality of the code but also makes it easier to maintain and debug in the future.

### TDD

By following Test-Driven Development (TDD) approach, which means that we write tests before writing code, we ensure that our code is thoroughly tested and free of bugs, resulting in a more stable and reliable application.

### 12-factor App

The backend framework follows the 12 Factor app methodology, which is a set of best practices for building scalable and maintainable, by that we ensure that our backend is highly scalable, easily deployable, and can be maintained with minimal effort.

## Libraries

### **OpenAPI**

OpenAPI is a specification for building APIs. It provides a standardized way to describe the structure of an API, including the endpoints, parameters, and responses. OpenAPI is important because it allows developers to build APIs that are easy to understand and use. It also makes it easier to build tools that can work with any API that adheres to the OpenAPI specification.

### **Swagger**

Swagger is a set of tools for building and documenting APIs that adhere to the OpenAPI specification. It includes a user interface for exploring and testing APIs and tools for generating client code in various programming languages. Swagger is important because it makes it easy for developers to build and document APIs that are easy to use and understand.

### Type**ORM**

We use TypeORM, a powerful ORM that simplifies database management and allows for seamless integration with various databases, including Postgres. This ensures that your data is stored securely and efficiently, with minimal downtime.

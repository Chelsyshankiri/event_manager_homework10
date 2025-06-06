# Event Manager Company: Software QA Analyst/Developer Onboarding Assignment

Welcome to the Event Manager Company! As a newly hired Software QA Analyst/Developer and a student in software engineering, you are embarking on an exciting journey to contribute to our project aimed at developing a secure, robust REST API that supports JWT token-based OAuth2 authentication. This API serves as the backbone of our user management system and will eventually expand to include features for event management and registration.

## Submissions:
 
 ### Learnings from the Assignments
 Through this assignment, I have got the valuable details about technical and collabarative aspects about the software development. 
 
On the technical side, working on this project helped me strengthen my understanding of concepts like API debugging, design, and testing. I got hands-on experience acting like a QA Analyst—running the test suite, identifying failing test cases, and tracing issues within the project. This process also helped me better understand the project's dependencies and architecture.

When it came to fixing those issues, I often had to research best practices, which really sharpened both my problem-solving and coding skills. Linking commits to specific issues taught me the importance of maintaining traceability and clear documentation in a codebase.

Overall, the challenges I faced during this assignment taught me how valuable systematic debugging, effective error resolution, and proper version control are. It also gave me a stronger foundation and a clearer perspective on the importance of collaboration in software development.
 
 ### Project Image deployed to docker hub
 [DockerHub Repository Link](https://hub.docker.com/repository/docker/chelsy688/event_manager/general)
 
 ![dockerhub deployment image](./docker_hub.png)
 
 ### Test Coverage
 
   Added Testcases to increase the test coverage upto 95% on the Pytest coverage run. 
   Coverage report afer the successful workflow run.
   ```bash
   ---------- coverage: platform linux, python 3.10.12-final-0 ----------
Name                                       Stmts   Miss  Cover
--------------------------------------------------------------
app/__init__.py                                0      0   100%
app/database.py                               16      3    81%
app/dependencies.py                           39      3    92%
app/main.py                                   16      3    81%
app/models/user_model.py                      49      0   100%
app/routers/__init__.py                        0      0   100%
app/routers/user_routes.py                    84     40    52%
app/schemas/link_schema.py                     8      0   100%
app/schemas/pagination_schema.py              20      1    95%
app/schemas/token_schema.py                    7      0   100%
app/schemas/user_schemas.py                   67      1    99%
app/services/__init__.py                       0      0   100%
app/services/email_service.py                 18      1    94%
app/services/jwt_service.py                   18      2    89%
app/services/user_service.py                 164     11    93%
app/utils/__init__.py                          0      0   100%
app/utils/api_description.py                   3      0   100%
app/utils/link_generation.py                  24      0   100%
app/utils/nickname_gen.py                      7      0   100%
app/utils/security.py                         21      0   100%
app/utils/smtp_connection.py                  27      0   100%
app/utils/template_manager.py                 25      0   100%
settings/__init__.py                           0      0   100%
settings/config.py                            41      0   100%
tests/__init__.py                              0      0   100%
tests/conftest.py                            134      2    99%
tests/test_api/test_users_api.py             126      0   100%
tests/test_conftest.py                        51      0   100%
tests/test_dependencies.py                    43      0   100%
tests/test_email.py                            7      0   100%
tests/test_link_generation.py                 39      0   100%
tests/test_models/test_user_model.py          85      0   100%
tests/test_schemas/__init__.py                 0      0   100%
tests/test_schemas/test_user_schemas.py       49      0   100%
tests/test_security.py                        43      0   100%
tests/test_services/test_user_service.py     131      5    96%
--------------------------------------------------------------
TOTAL                                       1362     72    95%
   ```
 
 ### Issues Addressed:
   Issue #7: [UUID is not passed correctly](https://github.com/Chelsyshankiri/event_manager_homework10/issues/7)
  
   Issue: Instead of passing UUID that will be unique for response data.Passing a unique-id-string which is a string as its own
   
   Resolution: Fixed the issue by ensuring that the UUID was correctly passed in while creating response data. After testing it is confirmed that it is working fine.
 
   Issue #4: [SMTPServerDisconnected : Connection unexpectedly closed running email functionalities](https://github.com/Chelsyshankiri/event_manager_homework10/issues/4)
 
   Issue: SMTPServerDisconnected: Connection unexpectedly closed running email functionalities
 
   Resolution: I have added the environment varibales of username and password for this and passed the same in the workflow code to make the SMTP connection stable. Test cases have shown that after doing this the connection is stable and the test cases are passed.
 
   Issue #3 [In Tests, Missing fixtures for user admin and manager tokens](https://github.com/Chelsyshankiri/event_manager_homework10/issues/3)
 
   Issue: Missing Fixtures: user_token, admin_token, and manager_token in Tests.
 
   Resolution: Added the code for the missing fixtures like admin_token, user_token and manager_token that are the cause for failure in multiple test cases. After the running the test suite we have ensured that all the token dependent code is working fine.
 
   Issue #2 [PydanticValidationError on LoginRequest](https://github.com/Chelsyshankiri/event_manager_homework10/issues/2)
 
   Issue: pydantic ValidationError for LoginRequest
 
   Resolution: There are few validation errors that are identified and I have corrected the schema for LoginRequest to align with expected fields. Updated the input validation logic and added unit tests to cover edge cases.
 
   Issue #1 [UserData Fetch is failing](https://github.com/Chelsyshankiri/event_manager_homework10/issues/1)
 
   Issue: UserData fetch Failure
 
   Resolution: A few details like nickname,username and UUID are not correctly fetched and passed to add or get the data which in result makes the model formation wrong.


## Assignment Objectives

1. **Familiarize with REST API functionality and structure**: Gain hands-on experience working with a REST API, understanding its endpoints, request/response formats, and authentication mechanisms.

2. **Implement and refine documentation**: Critically analyze and improve existing documentation based on issues identified in the instructor videos. Ensure that the documentation is up-to-date and accurately reflects the current state of the software.

3. **Engage in manual and automated testing**: Develop comprehensive test cases and leverage automated testing tools like pytest to push the project's test coverage towards 90%. Gain experience with different types of testing, such as unit testing, integration testing, and end-to-end testing.

4. **Explore and debug issues**: Dive deep into the codebase to investigate and resolve issues related to user profile updates and OAuth token generation. Utilize debugging tools, interpret error messages, and trace the flow of execution to identify the root cause of problems.

5. **Collaborate effectively**: Experience the power of collaboration using Git for version control and GitHub for code reviews and issue tracking. Work with issues, branches, create pull requests, and merge code while following best practices.

## Setup and Preliminary Steps

1. **Fork the Project Repository**: Fork the [project repository](https://github.com/yourusername/event_manager) to your own GitHub account. This creates a copy of the repository under your account, allowing you to work on the project independently.

2. **Clone the Forked Repository**: Clone the forked repository to your local machine using the `git clone` command. This creates a local copy of the repository on your computer, enabling you to make changes and run the project locally.

3. **Verify the Project Setup**: Follow the steps in the instructor video to set up the project using [Docker](https://www.docker.com/). Docker allows you to package the application with all its dependencies into a standardized unit called a container. Verify that you can access the API documentation at `http://localhost/docs` and the database using [PGAdmin](https://www.pgadmin.org/) at `http://localhost:5050`.

## Testing and Database Management

1. **Explore the API**: Use the Swagger UI at `http://localhost/docs` to familiarize yourself with the API endpoints, request/response formats, and authentication mechanisms. Swagger UI provides an interactive interface to explore and test the API endpoints.

2. **Run Tests**: Execute the provided test suite using pytest, a popular testing framework for Python. Running tests ensures that the existing functionality of the API is working as expected. Note that running tests will drop the database tables, so you may need to manually drop the Alembic version table using PGAdmin and re-run migrations to ensure a clean state.

3. **Increase Test Coverage**: To enhance the reliability of the API, aim to increase the project's test coverage to 90%. Write additional tests for various scenarios and edge cases to ensure that the API handles different situations correctly.

## Collaborative Development Using Git

1. **Enable Issue Tracking**: Enable GitHub issues in your repository settings. [GitHub Issues](https://guides.github.com/features/issues/) is a powerful tool for tracking bugs, enhancements, and other tasks related to the project. It allows you to create, assign, and prioritize issues, facilitating effective collaboration among team members.

2. **Create Branches**: For each issue or task you work on, create a new branch with a descriptive name using the `git checkout -b` command. Branching allows you to work on different features or fixes independently without affecting the main codebase. It enables parallel development and helps maintain a stable main branch.

3. **Pull Requests and Code Reviews**: When you have completed work on an issue, create a [pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests) to merge your changes into the main branch. Pull requests provide an opportunity for code review, where your team members can examine your changes, provide feedback, and suggest improvements. Code reviews help maintain code quality, catch potential issues, and promote knowledge sharing among the team.

## Specific Issues to Address

In this assignment, you will identify, document, and resolve five specific issues related to:

1. **Username validation**: Investigate and resolve any issues related to username validation. This may involve handling special characters, enforcing length constraints, or ensuring uniqueness. Proper username validation is essential to maintain data integrity and prevent potential security vulnerabilities.

2. **Password validation**: Ensure that password validation follows security best practices, such as enforcing minimum length, requiring complexity (e.g., a mix of uppercase, lowercase, numbers, and special characters), and properly hashing passwords before storing them in the database. Robust password validation protects user accounts and mitigates the risk of unauthorized access.

3. **Profile field edge cases**: Test and handle various scenarios related to updating profile fields. This may include updating the bio and profile picture URL simultaneously or individually. Consider different combinations of fields being updated and ensure that the API handles these cases gracefully. Edge case testing helps uncover potential issues and ensures a smooth user experience.

Additionally, you will resolve a sixth issue demonstrated in the instructor video. These issues will test various combinations and scenarios to simulate real-world usage and potential edge cases. By addressing these specific issues, you will gain experience in identifying and resolving common challenges in API development.

## Submission Requirements

To complete this assignment, submit the following:

1. **GitHub Repository Link**: Ensure that your repository is well-organized and includes:
  - Links to five closed issues, each with accompanying test code and necessary application code modifications.
  - Each issue should be well-documented, explaining the problem, the steps taken to resolve it, and the outcome. Proper documentation helps others understand your work and facilitates future maintenance.
  - All issues should be merged into the main branch, following the Git workflow and best practices.

2. **Updated README**: Replace the existing README with:
  - Links to the closed issues, providing easy access to your work.
  - Link to project image deployed to Dockerhub.
  - A 2-3 paragraph reflection on what you learned from this assignment, focusing on both technical skills and collaborative processes. Reflect on the challenges you faced, the solutions you implemented, and the insights you gained. This reflection helps solidify your learning and provides valuable feedback for improving the assignment in the future.

## Grading Rubric

| Criteria                                                                                                                | Points |
|-------------------------------------------------------------------------------------------------------------------------|--------|
| Resolved 5 issues related to username validation, password validation, and profile field edge cases                      | 30     |
| Resolved the issue demonstrated in the instructor video                                                                 | 20     |
| Increased test coverage to 90% by writing comprehensive test cases                                                      | 20     |
| Followed collaborative development practices using Git and GitHub (branching, pull requests, code reviews)              | 15     |
| Submitted a well-organized GitHub repository with clear documentation, links to closed issues, and a reflective summary | 15     |
| **Total**                                                                                                               | **100**|

## Resources and Documentation

- **Instructor Videos and Important Links**:
 - [Introduction to REST API with Postgres](https://youtu.be/dgMCSND2FQw) - This video provides an overview of the REST API you'll be working with, including its structure, endpoints, and interaction with the PostgreSQL database.
 - [Assignment Instructions](https://youtu.be/TFblm7QrF6o) - Detailed instructions on your tasks, guiding you through the assignment step by step.
 - [Git Command Reference I created and some explanation for collaboration with git](git.md)
 - [Docker Commands and Running The Tests in the Application](docker.md)
 - Look at the code comments:
    - [Test Configuration and Fixtures](tests/conftest.py)
    - [API User Routes](app/routers/user_routes.py)
    - [API Oauth Routes - Connection to HTTP](app/routers/oauth.py)
    - [User Service - Business Logic - This implements whats called the service repository pattern](app/services/user_service.py)
    - [User Schema - Pydantic models](app/schemas/user_schemas.py)
    - [User Model - SQl Alchemy Model ](app/models/user_model.py)
    - [Alembic Migration - this is what runs to create the tables when you do alembic upgrade head](alembic/versions/628adcb2d60e_initial_migration.py)
    - See the tests folder for all the tests

 - API Documentation: `http://localhost/docs` - The Swagger UI documentation for the API, providing information on endpoints, request/response formats, and authentication.
 - Database Management: `http://localhost:5050` - The PGAdmin interface for managing the PostgreSQL database, allowing you to view and manipulate the database tables.

- **Code Documentation**:
 The project codebase includes docstrings and comments explaining various concepts and functionalities. Take the time to read through the code and understand how different components work together. Pay attention to the structure of the code, the naming conventions used, and the purpose of each function or class. Understanding the existing codebase will help you write code that is consistent and integrates well with the project.

- **Additional Resources**:
 - [SQLAlchemy Library](https://www.sqlalchemy.org/) - SQLAlchemy is a powerful SQL toolkit and Object-Relational Mapping (ORM) library for Python. It provides a set of tools for interacting with databases, including query building, database schema management, and data serialization. Familiarize yourself with SQLAlchemy's documentation to understand how it is used in the project for database operations.
 - [Pydantic Documentation](https://docs.pydantic.dev/latest/) - Pydantic is a data validation and settings management library for Python. It allows you to define data models with type annotations and provides automatic validation, serialization, and deserialization. Consult the Pydantic documentation to understand how it is used in the project for request/response validation and serialization.
 - [FastAPI Framework](https://fastapi.tiangolo.com/) - FastAPI is a modern, fast (high-performance) Python web framework for building APIs. It leverages Python's type hints and provides automatic API documentation, request/response validation, and easy integration with other libraries. Explore the FastAPI documentation to gain a deeper understanding of its features and how it is used in the project.
 - [Alembic Documentation](https://alembic.sqlalchemy.org/en/latest/index.html) - Alembic is a lightweight database migration tool for usage with SQLAlchemy. It allows you to define and manage database schema changes over time, ensuring that the database structure remains consistent across different environments. Refer to the Alembic documentation to learn how to create and apply database migrations in the project.

These resources will provide you with a solid foundation to understand the tools, technologies, and concepts used in the project. Don't hesitate to explore them further and consult the documentation whenever you encounter challenges or need clarification.

## Conclusion

This assignment is designed to challenge you, help you grow as a developer, and prepare you for the real-world responsibilities of a Software QA Analyst/Developer. By working on realistic issues, collaborating with your team, and focusing on testing and quality assurance, you will gain valuable experience that will serve you throughout your career.

Remember, the goal is not just to complete the assignment but to embrace the learning journey. Take the time to understand the codebase, ask questions, and explore new concepts. Engage with your team members, seek feedback, and learn from their experiences. Your dedication, curiosity, and willingness to learn will be the key to your success in this role.

We are excited to have you on board and look forward to seeing your contributions to the project. Your fresh perspective and skills will undoubtedly make a positive impact on our team and the quality of our software.

If you have any questions or need assistance, don't hesitate to reach out to your mentor or team lead. We are here to support you and ensure that you have a rewarding and enriching experience.

Once again, welcome to the Event Manager Company! Let's embark on this exciting journey together and create something remarkable.

Happy coding and happy learning!

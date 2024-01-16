# Social-Media-Analytics---ST


**Main Goal:**

Develop a comprehensive REST API application for social media analytics. This application aims to gather, analyze, and present insightful data about social media activities, enabling users to make informed decisions based on real-time and historical analytics.

**Key Technologies:**

- Spring Boot: A robust Java-based framework for building scalable and efficient web applications, providing a solid foundation for the backend.
- MongoDB: Chosen as the database management system for its flexibility and scalability in handling unstructured data typical in social media analytics.
- Swagger: Utilized for API testing and documentation, offering a user-friendly interface for exploring and interacting with the API endpoints.
- React: Utilized for building a responsive and user-friendly frontend, offering a modern interface for users to interact with social media analytics data.

**Development Process:**

1. Backend Setup (Spring Boot and MongoDB): Set up the backend server, define data models, and integrate with MongoDB to store social media analytics data efficiently.
2. Database Design and Schema: Design a schema that accommodates various types of social media data, including user activities, engagement metrics, and post content.
3. Implementing RESTful Endpoints: Develop RESTful endpoints to handle operations like fetching analytics data, user engagement metrics, and historical trends.
4. Testing with Swagger: Utilize Swagger for API testing to ensure all endpoints function as expected, handling various types of requests and providing accurate responses.
5. Frontend Development (React): Create user interfaces for visualizing social media analytics data, displaying engagement metrics, and allowing users to customize data views.
6. Integration of Frontend and Backend: Connect the frontend and backend to ensure seamless communication, allowing users to interact with social media analytics in a cohesive manner.

**Benefits:**

- Real-time Analytics: Provide users with real-time insights into social media activities, enabling them to stay updated on the latest trends.
- User-friendly Interface: Utilize React to create an intuitive and visually appealing interface, enhancing the overall user experience.
- Scalable Data Storage: MongoDB ensures scalability in handling diverse and unstructured social media data, accommodating the growing volume of information.
- Comprehensive Testing: Thoroughly test the API using Swagger to ensure reliable and precise handling of social media analytics, minimizing the risk of errors.

**Entities:**

1. Java Classes: Develop entities like SocialMediaUser, Post, EngagementMetrics to represent various aspects of social media data.
2. Repositories: Implement Spring Data MongoDB repositories for entities such as SocialMediaUserRepository and PostRepository.
3. Service Layer: Create services like SocialMediaService and AnalyticsService to encapsulate business logic related to social media data.
4. Controller Layer: Establish controllers like SocialMediaController and AnalyticsController with methods for API endpoints.
5. Request and Response DTOs: Define DTOs for efficient data transfer in API requests and responses, catering to the specific needs of social media analytics.
6. Exception Handling: Implement exception handling to manage scenarios like bad requests, resource not found, etc.
7. Security: Utilize Spring Security for authentication and authorization, ensuring secure access to social media analytics data.
8. Documentation: Incorporate Swagger for comprehensive API documentation, aiding users and developers in understanding and utilizing the API.
9. Dependency Management: Use Maven or Gradle for dependency management, including dependencies such as Spring Boot Starter Web, Spring Data MongoDB, etc.

Swagger Sample Code:

![ED282D7E-89FE-46F6-9908-9E22F7941F8B](https://github.com/denisamarr/Social-Media-Analytics/assets/99808017/8d39baaf-70ee-429c-b1c5-33dacec70fb2)

![2AFC3267-B1C1-4DD1-9B82-525E3C1348D3](https://github.com/denisamarr/Social-Media-Analytics/assets/99808017/ffbc39f7-d849-4c26-b187-63c1f5614f7f)


**Elastic Mapping:**


![5E534D5F-D07F-4457-855C-7BAAA3CF6B9E](https://github.com/denisamarr/Social-Media-Analytics/assets/99808017/b449871e-610c-4652-a5ba-7d61e2ccd80d)


1. 		Field: userId
    - Type: keyword
    - Description: Optimized for exact match queries, crucial for identifying specific user IDs.
2. 		Field: username
    - Type: text with a keyword sub-field
    - Description: The text field is suitable for full-text searches, and the keyword sub-field is ideal for exact match queries. The analyzer property is set to "standard" for tokenization.
3. 		Field: followers
    - Type: integer
    - Description: Stores the number of followers for a social media user.
4. 		Field: posts
    - Type: nested
    - Description: Nested type for handling an array of posts. Each post has properties like postId, content, likes, and comments.
5. 		Field: engagementMetrics
    - Type: nested
    - Description: Nested type for handling engagement metrics, including properties like likes, comments, and shares.


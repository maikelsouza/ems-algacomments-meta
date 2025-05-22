# ems-algacomments-meta

This project is an exercise from the AlgaWorks microservices course.

The task is to develop a system composed of two microservices that communicate synchronously via HTTP/REST using Spring RestClient.
The system will be responsible for receiving user comments, validating them against forbidden words, and storing only the approved ones.

## Project Diagram

![img.png](img.png)

## Microservice: Comment

This microservice is responsible for:

- Create a new comment and submit it for moderation
- View the details of an approved comment
- List approved comments with pagination

### Endpoints

There are three endpoints:

- **POST** `/api/comments`  
  Creates a new comment.

- **GET** `/api/comments/{id}`  
  Retrieves a comment by its ID.

- **GET** `/api/comments`  
  Retrieves all comments with pagination.

## Microservice: Moderation

This microservice is responsible for:

- Expose a REST API for creating and querying comments
- Submit new comments for moderation via synchronous POST using RestClient
- Store only approved comments
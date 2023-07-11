# social-network

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/siennameow/social-network-API/blob/main/LICENSE)

## Description 📝

The Social Network Web Application API is designed to provide a comprehensive platform for users to connect, share thoughts, react to their friends' thoughts, and manage their friend lists. This readme file serves as a guide to understand the technologies and tools used in the development of this API.
It uses `Express.js` for routing, a `MongoDB` database, the `Mongoose` ODM, and `Moment.js` to format timestamps. The seed data is created using `Insomnia`.
Walk-through demonstration video - https://drive.google.com/file/d/1XhKFqWquari67OGmdWZlJVQvmsOtaWQK/view?usp=sharing

## Table of Contents 📖

- [Application Preview](#application-preview-)
- [Features ](#features-)
- [Installation](#installation-)
- [Usage](#usage-)
- [Technologies](#technologies-)
- [Tests](#tests)
- [Contribution](#contribution-)

## Installation

- Download or clone repository to use this application on local machine.
- `Node.js` and `MongoDB` is required to run the application
- To install necessary dependencies, navigate to the root directory and run the following command:
  `npm i`

## Usage

After installation :

- To invoke the application, run `npm start`.
- When the server is started, the Mongoose models are synched to the MongoDB database.
- Open MongoDB and connect to the MongoDB URI `mongodb://localhost:27017`. On the list of databases, click on `socialDB` to see `thoughts` and `users` data.
- To create seed data and test the API routes, use [Insomnia](https://insomnia.rest/download). Also, see the Tests section below.

**USER**

- Create a new user: `POST /api/users`
- Get all users: `GET /api/users`
- Get a single user by its `id`: `GET /api/users/:userId`

- Update a user by its `id`: `PUT /api/users/:userId`

- Delete a user by its `id`: `DELETE /api/user/:userId`

**FRIEND**

- Add a new friend to a user's friend list: `POST /api/users/:userid/friends/:friendId`
- Delete a friend from a user's friend list: `DELETE /api/users/:userid/friends/:friendId`

**THOUGHT**

- Create a new thought: `POST /api/thoughts/`
- Get all thoughts: `GET /api/thoughts/`
- Get a single thought by its `id`: `GET /api/thoughts/:thoughtId`
- Update a thought by its `id`: `PUT /api/thoughts/:thoughtId`
- Delete a thought by its `id`: `DELETE /api/thoughts/:thoughtId`

**REACTION**

- Create a reaction: `POST /api/thoughts/:thoughtId/reactions`
- Delete a reaction by the `reactionId`: `DEL /api/thoughts/:thoughtId/reactions/:reactionId`

## Technologies

- [Express.js](https://expressjs.com/)
  This API utilizes the powerful Express.js framework for routing purposes. It offers a flexible and efficient solution for handling HTTP requests and responses, ensuring seamless communication between the client and the server. </br>
- [MongoDB](https://www.mongodb.com/)
  The data for this API is stored in a MongoDB database, which provides scalability and flexibility for handling various types of data. MongoDB's document-oriented model allows for easy organization and retrieval of user information and social interactions.</br>
- [Mongoose](https://mongoosejs.com/)
  To simplify the interaction between the Node.js application and the MongoDB database, the Mongoose Object Data Modeling (ODM) library is employed. Mongoose provides an elegant solution for defining data schemas, performing validation, and executing database queries.</br>
- [Insomnia](https://insomnia.rest/)
  The seed data for this API is created using Insomnia, a popular REST client. Insomnia allows for easy and efficient testing of API endpoints during the development process, ensuring the integrity and correctness of the data.</br>
- [Moment.js](https://www.npmjs.com/package/moment)
  The API relies on Moment.js to format timestamps accurately. This library simplifies the manipulation and display of dates and times, ensuring a consistent and user-friendly experience when dealing with time-related data.</br>

## Tests

Insomnia is an invaluable tool for testing REST API calls and ensuring the functionality and correctness of our endpoints. In order to demonstrate the usage of Insomnia and provide a comprehensive understanding of how data is added and tested using this tool, I have prepared walk-through demonstration video - https://drive.google.com/file/d/1XhKFqWquari67OGmdWZlJVQvmsOtaWQK/view?usp=sharing

## Contribution

If you would like to contribute to this project reach out to me on `khyati296@gmail.com`

# Timestamp Microservice

This project is an [exam](https://www.freecodecamp.org/learn/apis-and-microservices/apis-and-microservices-projects/timestamp-microservice) part of the freeCodeCamp Back End Development and APIs curriculum. It is a Timestamp Microservice built using Node.js and Express. The application provides an API endpoint that returns the current timestamp or a timestamp for a given date string. The structure of the project including the index.HTML was cloned from freeCodeCamp, I wrote the index.js code.

You can view the live demo of the project [here](https://timestamp-microservice-aaa1392706ce.herokuapp.com/).

## Table of Contents

- Introduction
- Features
- [Technologies Used](#technologies-used)
- [Setup and Installation](#setup-and-installation)
- Usage
- [Project Structure](#project-structure)
- [API Endpoints](#api-endpoints)
- Troubleshooting
- Contributing
- License

## Introduction

The Timestamp Microservice is a web application that provides a simple API for returning timestamps. It is built using Node.js and Express. This project is part of the freeCodeCamp Back End Development and APIs curriculum.

## Features

- **Current Timestamp**: Get the current timestamp in both Unix and UTC formats.
- **Date String Timestamp**: Get the timestamp for a given date string in both Unix and UTC formats.
- **Error Handling**: Returns an error message for invalid date strings.
- **CORS Enabled**: Allows cross-origin requests for remote testing.

## Technologies Used

- **Node.js**: JavaScript runtime environment.
- **Express**: Web framework for Node.js.
- **CORS**: Middleware for enabling CORS.

## Setup and Installation

To set up and run this project locally, follow these steps:

1. **Clone the repository**:
    ```bash
    git clone https://github.com/your-username/timestamp-microservice.git
    cd timestamp-microservice
    ```

2. **Install dependencies**:
    ```bash
    npm install
    ```

3. **Start the server**:
    ```bash
    npm start
    ```

4. **Open the application**:
    Open your web browser and go to [`http://localhost:3000`](http://localhost:3000).

## Usage

- **Get Current Timestamp**: Access the root endpoint `/api` to get the current timestamp.
- **Get Timestamp for Date String**: Access the endpoint `/api/:date_string` with a valid date string to get the timestamp for that date.

## Project Structure

```
timestamp-microservice/
│
├── public/                 # Public assets
│   ├── index.html          # Main HTML file
│   └── ...
│
├── views/                  # View templates
│   ├── index.html          # Main HTML file
│   └── ...
│
├── index.js                # Main server file
├── package.json            # Project dependencies and scripts
└── README.md               # Project documentation
```

## API Endpoints

- **GET `/api/hello`**: Returns a greeting message.
  - Response: `{ "greeting": "hello API" }`

- **GET `/api/:date_string?`**: Returns the timestamp for the given date string or the current timestamp if no date string is provided.
  - Response: `{ "unix": <timestamp>, "utc": <UTC string> }`
  - Error Response: `{ "error": "Invalid Date" }`

## Troubleshooting

If port 3000 is already in use, you can find the process ID (PID) and kill it using the following steps:

1. **Find the PID**:
    ```bash
    lsof -i :3000
    ```

    This command will list the processes using port 3000. Look for the PID in the output.

2. **Kill the process**:
    ```bash
    kill -9 <PID>
    ```

    Replace `<PID>` with the actual process ID you found in the previous step.

3. **Restart the server**:
    ```bash
    npm start
    ```

## Contributing

Contributions are welcome! If you have any suggestions or improvements, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add some feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Open a pull request.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

---

Thank you for checking out my Timestamp Microservice project! If you have any questions or feedback, feel free to reach out.

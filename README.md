#  Chat360 SDE-1 and SDE Intern Assignment

## Assignment

**Quality Log Control**

---
# Screenshot

![Screenshot (18)](https://github.com/Ayushgadre/Chat360-SDE-Assignment/assets/84783296/224e946d-d8cb-493a-bfa7-aa575c36cca2)


# How to Run

Give the following command:

Install necessary plugins by the command: npm install

For starting the backend server: npm start

For The searching page (UI): a. open the browser b. go to http://localhost:3000/


## Overview

This project implements a Quality Log Control system which ingests logs from multiple APIs and provides a query interface to search these logs based on various criteria.

## Technologies Used

- **Node.js**: JavaScript runtime environment.
- **Express**: Web framework for Node.js.
- **Morgan**: HTTP request logger middleware for Node.js.
- **EJS**: Embedded JavaScript templating.
- **HTML/CSS**: For the frontend interface.

## Installation

1. **Clone the Repository**:
    ```sh
    git clone https://github.com/Ayushgadre/log-control-system.git
    cd log-control-system
    ```

2. **Install Dependencies**:
    ```sh
    npm install
    ```
## Usage

### Log Ingestion

1. **Start the Server**:
    ```sh
    npm start
    ```

2. **Add Logs**:
   Use an API client like Postman to send POST requests to the server.

   - **URL**: `http://localhost:3000/log/{source}`
   - **Method**: POST
   - **Body**:
     ```json
     {
         "level": "error",
         "log_string": "Failed to connect to database"
     }
     ```

### Log Query Interface

1. **Open the Browser**:
   Navigate to `http://localhost:3000/`.

2. **Search for Logs**:
   Use the search form to query logs based on:
   - **Level**
   - **Log String**
   - **Start Date**
   - **End Date**
   - **Source**

---

## Sample Logs and Queries

### Adding Sample Logs

- **Log 1**:
  - **URL**: `http://localhost:3000/log/log1`
  - **Method**: POST
  - **Body**:
    ```json
    {
        "level": "error",
        "log_string": "Failed to connect to database"
    }
    ```

- **Log 2**:
  - **URL**: `http://localhost:3000/log/log2`
  - **Method**: POST
  - **Body**:
    ```json
    {
        "level": "info",
        "log_string": "User logged in"
    }
    ```

### Sample Queries

- **Find all logs with the level set to "error"**:
  - **Level**: `error`

- **Search for logs with the message containing the term "Failed to connect"**:
  - **Log String**: `Failed to connect`

- **Filter logs between specific dates**:
  - **Start Date**: `2023-09-10T00:00:00Z`
  - **End Date**: `2023-09-15T23:59:59Z`

---

## Advanced Features

These features aren’t compulsory but can enhance the functionality of your project:

- Implement search within specific date ranges.
- Utilize regular expressions for search.
- Allow combining multiple filters.
- Provide real-time log ingestion and searching capabilities.
- Implement role-based access to the query interface.

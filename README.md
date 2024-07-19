# File Management API

This project provides a simple API for creating and listing text files with the current timestamp.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
  - [Create File](#create-file)
  - [List Files](#list-files)
- [Dependencies](#dependencies)

## Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-directory>

2. Install the dependencies:
    ```bash
    npm install
3. Start the server:
    ```bash
    npm start

The server will be running on http://localhost:3001.

## Usage

### Create File

- **Endpoint**: `/create-file`
- **Method**: `POST`
- **Response**:
  - **Status**: `201 Created`
  - **Body**:
    ```json
    {
      "message": "File created successfully",
      "fileName": "<timestamp>.txt"
    }
    ```

### List Files

- **Endpoint**: `/list-files`
- **Method**: `GET`
- **Response**:
  - **Status**: `200 OK`
  - **Body**:
    ```json
    {
      "files": [
        "<timestamp>.txt",
        ...
      ]
    }
    ```

## API Endpoints

### Create File

#### Request

- **Method**: `POST`
- **URL**: `/create-file`

#### Response

- **Status**: `201 Created`
- **Body**:
  ```json
  {
    "message": "File created successfully",
    "fileName": "<timestamp>.txt"
  }

### Example
```sh
curl -X POST http://localhost:3001/create-file
```
## List Files

- **Request**
  - **Method**: `GET`
  - **URL**: `/list-files`

- **Response**
  - **Status**: `200 OK`
  - **Body**:
    ```json
    {
      "files": [
        "<timestamp>.txt",
        ...
      ]
    }
    ```
### Example
```sh
curl -X POST http://localhost:3001/list-files
```

## Dependencies

- **express**: Fast, unopinionated, minimalist web framework for Node.js.
- **fs**: Node.js file system module.
- **path**: Node.js path module.


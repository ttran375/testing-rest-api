# Rest API

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/ttran375/testing-rest-api)

The repository contains:

* Distributed code from **eCentennial**: `HTML`, `JS`, and `CSS` files used to build a **MERN** application.
* `/.devcontainer`: Configuration file used by **Codespaces** to determine operating system.
* `/.vscode`: Configuration file used by **Codespaces** to configure Visual Studio Code settings.
* `/client/.eslintrc`: Settings for [ESLint](https://eslint.org/) included for code consistency and quality.
* `/client/.prettierrc`: Settings for [Prettier](https://prettier.io/) used to format code.
* `package.json` and `yarn.lock`: Defines the application information for [Node.js](https://nodejs.org/), dependent packages, and the versions needed for each.

## MERN Skeleton

This is a **MERN (MongoDB, Express, React, Node.js)** stack application. It's designed to be easily set up and run in a development environment using **GitHub Codespaces**.

### Getting Started

Select **Open in GitHub Codespaces** and then **Create codespace**. **GitHub** will prepare the development environment.

### Install Packages

Install the necessary dependencies for both the server and client parts of the application.

* **For the server:**

  Open the integrated terminal and run:

  ```sh
  yarn
  ```

* **For the client:**

  Navigate to the client directory and run:

  ```sh
  cd client
  yarn
  ```

### Update .env File

Update the `.env` file located in the `client` directory with the `MongoDB URI` and any other required environment variables.

1. Navigate to the `client` directory.
2. Open the `.env` file. The example provided in `client/.env.example` can be used as a reference.
3. Update the `MONGODB_URI` with the necessary credentials.

   ```.env
   MONGODB_URI=mongodb+srv://your_user:your_password@your_cluster.mongodb.net/YourDatabase?retryWrites=true&w=majority&appName=YourApp/yourcollection
   ```

### Start the Server

After setting up the environment variables, start the server and client concurrently.

* **From the client directory**, run:

  ```sh
  yarn dev
  ```

The **MERN** stack application should now be running. The client application could be accessed  in the browser with the workspace forwarded port.

## Test the REST API

### Testing the API with Thunder Client

1. **Open Thunder Client:**
   * Open **Thunder Client** readily installed in **Codespaces** by clicking on its icon on the sidebar.

2. **Create a New Request:**
   * In **Thunder Client**, click on the **New Request** button to start setting up the API request.
   * Enter the API endpoint URL in the URL field: `http://localhost:3000/api/users`.
   * Select the HTTP method `POST` from the dropdown next to the URL field.

3. **Configure Request Headers (if needed):**
   * If the API requires headers (like `Content-Type: application/json` or authentication tokens), click on the "Headers" tab below the URL field and add them accordingly.

4. **Set Up Request Body:**
   * Click on the "Body" tab, choose the content type, and enter the JSON data. Example:

    ```json
    {
        "name": "James",
        "email": "james@yahoo.com",
        "password": "jamesjames"
    }
    ```

5. **Send the Request:**
   * Click the "Send" button to execute the request. **Thunder Client** will display the response from the API, including status code, response time, and the body.

6. **Review the Response:**
   * On **MongoDB Cloud**, click on the **Database** section then **Browse Collections**.

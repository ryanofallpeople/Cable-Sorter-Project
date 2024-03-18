# Cable Catalog WebApp API

This API is designed to catalog various cables for later searchability. It utilizes Node.js and a JSON database to store and manage cable data.

## Dependencies

- Node.js
- Express.js
- jsonfile (for interacting with JSON files)

## Setup Instructions

1. Clone this repository to your local machine.
2. Navigate to the project directory.
3. Install dependencies using npm:
   ```bash
   npm install
   ```
4. Start the server:
   ```bash
   npm start
   ```
5. The API will be accessible at `http://localhost:3000`.

## API Endpoints

### 1. Retrieve All Cables

- **Endpoint:** `GET /cables`
- **Description:** Retrieves all cables from the database.
- **Response:** Array of cable objects.

### 2. Retrieve Cable by ID

- **Endpoint:** `GET /cables/:id`
- **Description:** Retrieves a cable by its unique identifier.
- **Parameters:** `id` (string) - The ID of the cable.
- **Response:** Cable object.

### 3. Add a New Cable

- **Endpoint:** `POST /cables`
- **Description:** Adds a new cable to the database.
- **Request Body:** JSON object with cable attributes:
  ```json
  {
    "sideAConnector": "Type A",
    "sideAGender": "Male",
    "sideBConnector": "Type B",
    "sideBGender": "Female",
    "length": "3m",
    "dataOrPowerOnly": "Data",
    "audioType": "Balanced",
    "location": "Box 123"
  }
  ```
- **Response:** Newly added cable object.

### 4. Update Cable Information

- **Endpoint:** `PUT /cables/:id`
- **Description:** Updates the information of an existing cable.
- **Parameters:** `id` (string) - The ID of the cable.
- **Request Body:** JSON object with updated cable attributes.
- **Response:** Updated cable object.

### 5. Delete a Cable

- **Endpoint:** `DELETE /cables/:id`
- **Description:** Deletes a cable from the database.
- **Parameters:** `id` (string) - The ID of the cable.
- **Response:** Success message.

## Connecting to Front End

To connect this API to an existing front end template, you can use a simple HTML, CSS, and JS setup. You would need to make AJAX requests to the appropriate API endpoints to retrieve, add, update, or delete cables as needed. You can refer to the API documentation above to understand how to structure these requests. Additionally, you may need to handle form submissions and user interactions in your front end code accordingly.

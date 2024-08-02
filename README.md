
# API with React Frontend

This project consists of a simple Flask API and a React frontend component for interacting with the API.

## Project Structure

### Frontend

- `src/BfhlComponent.js`: A React component that allows users to input JSON data, sends it to the API, and displays the response.
- `src/App.js`: The main React component that renders `BfhlComponent`.

### Backend

- `app.py`: A Flask application with the following endpoints:
  - `POST /bfhl`: Accepts JSON data, processes it to separate numbers and alphabets, and returns the highest alphabet.
  - `GET /bfhl`: Returns a JSON object with an operation code.

## Getting Started

### Prerequisites

- Node.js and npm for the frontend
- Python and Flask for the backend

### Setup

#### Frontend

1. Navigate to the `frontend` directory.
2. Install the dependencies:
   ```bash
   npm install
   ```
3. Start the development server:
   ```bash
   npm start
   ```

#### Backend

1. Navigate to the `backend` directory.
2. Install the dependencies:
   ```bash
   pip install flask flask-cors
   ```
3. Start the Flask server:
   ```bash
   python app.py
   ```

### API Endpoints

- **POST /bfhl**
  - **Request Body**: JSON object with a `data` key containing an array of strings.
  - **Response**: JSON object containing:
    - `is_success`: A boolean indicating success.
    - `user_id`: Sample user ID.
    - `email`: Sample email address.
    - `roll_number`: Sample roll number.
    - `numbers`: List of numbers extracted from the input data.
    - `alphabets`: List of alphabets extracted from the input data.
    - `highest_alphabet`: The highest alphabet from the input data.

- **GET /bfhl**
  - **Response**: JSON object with an `operation_code` key set to `1`.

## Troubleshooting

- Ensure the Flask server is running before interacting with the React frontend.
- Check for CORS issues if the frontend is unable to communicate with the backend.

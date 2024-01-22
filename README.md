# Cafe Explorer Web App

This is a simple Flask web application for exploring cafes. It provides functionality to retrieve random cafes, view all cafes, search for cafes by location, add new cafes, update cafe prices, and delete cafes. The cafes are stored in a SQLite database.

## Setup

Before running the application, make sure to install the required packages by executing the following command in the terminal:

```bash
pip install -r requirements.txt
```

## Database Configuration

The application uses SQLAlchemy to connect to a SQLite database named `cafes.db`. The database schema includes a `Cafe` table with various attributes such as name, location, map URL, image URL, seating capacity, and more.

## Usage

- **Home**: Access the home page by navigating to the root URL ("/"). This serves the "index.html" template.

- **Get Random Cafe**: Retrieve information about a random cafe by making a GET request to "/random".

- **Get All Cafes**: Obtain a list of all cafes by making a GET request to "/all".

- **Search for Cafes**: Search for cafes in a specific location by making a GET request to "/search" with the location as a parameter.

- **Add a New Cafe**: Add a new cafe to the database by making a POST request to "/add" with the required form parameters.

- **Update Cafe Price**: Update the price of a cafe by making a PATCH request to "/update-price/<cafe_id>" with the new price as a query parameter.

- **Delete Cafe**: Delete a cafe from the database by making a DELETE request to "/report-closed/<cafe_id>" with an API key for authentication.

## Running the Application

Run the Flask application by executing the following command:

```bash
python app.py
```

The application will run in debug mode, and you can access it by navigating to [http://127.0.0.1:5000/](http://127.0.0.1:5000/) in your web browser.

## API Key for Deletion

To delete a cafe, an API key ("TopSecretAPIKey") is required for authentication. Include the API key as a query parameter in the DELETE request.

## Note

Make sure to modify the database URI in the code if you want to use a different database.

```

# weather-api
This Flask application provides a backend API for retrieving weather information based on user input location. It utilizes the OpenWeatherMap API to fetch weather data for a specified city and presents it in a JSON format.

Usage
To retrieve weather data for a specific city, make a GET request to the /weather endpoint with the city name as a parameter.

Bash
curl -X GET http://localhost:5000/weather?city=London
Use code with caution. Learn more
Response Format
The API returns a JSON object containing the following information:

JSON
{
  "city": "London",
  "temperature": 282.31,
  "description": "Light rain"
}
Use code with caution. 
Error Handling
If the city name is not provided, the API returns an error message.

JSON
{
  "error": "City parameter is required"
}
Use code with caution. Learn more
If an error occurs while fetching weather data from the OpenWeatherMap API, the API returns an internal server error message.

JSON
{
  "error": "Could not fetch weather data"
}
Use code with caution. Learn more
Running the API
To run the API, you will need to replace a5d4067060fcbcdbe1f858edd5d90b65 with your OpenWeatherMap API key. You can then run the following command:

Bash
python weather_api.py
Use code with caution. 
This will start the Flask application, and it should listen for requests on http://127.0.0.1:5000.

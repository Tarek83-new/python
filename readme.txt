WeatherApp
WeatherApp is a simple Python application that fetches and displays weather data for a specified city using the OpenWeatherMap API.

Features
Fetches current weather data for any city.
Displays temperature, humidity, pressure, weather description, and wind speed.
Handles errors such as invalid API keys and city not found.
Requirements
Python 3.x
requests library
Installation
Clone the repository (if applicable):

git clone https://github.com/yourusername/weatherapp.git
cd weatherapp
Install the requests library:

pip install requests
Usage
Obtain an API key from OpenWeatherMap:

Sign up for an account.
Generate an API key.
Replace the placeholder API key in the code with your actual API key:

api_key = "your_openweathermap_api_key"  # Replace with your OpenWeatherMap API key
Run the application:

python weather_app.py
Enter the city name when prompted:

Enter city name: London
View the weather data:

City: London
Temperature: 15°C
Humidity: 80%
Pressure: 1012 hPa
Weather: clear sky
Wind Speed: 3.6 m/s
Code Explanation
WeatherAPI Class
__init__(self, api_key): Initializes the class with the API key and base URL.
get_weather(self, city): Makes a GET request to the OpenWeatherMap API with the specified city and API key, and returns the JSON response. Handles invalid API key errors.
WeatherApp Class
__init__(self, api_key): Initializes the class with an instance of WeatherAPI using the provided API key.
display_weather(self, city): Fetches the weather data for the specified city and prints it in a user-friendly format. Handles errors by checking the response code.
Main Block
API Key: Your OpenWeatherMap API key is set here.
Creating an Instance: An instance of WeatherApp is created with the API key.
User Input: The user is prompted to enter a city name.
Displaying Weather: The display_weather method is called to fetch and display the weather data for the entered city.
Example Output
Enter city name: London
City: London
Temperature: 15°C
Humidity: 80%
Pressure: 1012 hPa
Weather: clear sky
Wind Speed: 3.6 m/s
Error Handling
The script includes basic error handling to check if the API returns an error code. If the API key is invalid or the city is not found, it will print an error message:

if weather_data.get('cod') != 200:
    print(f"Error: {weather_da
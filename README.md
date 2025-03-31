# Weather Dashboard

## Overview
The **Weather Dashboard** is a Python-based project that automates weather data collection using the OpenWeather API and securely stores it in an AWS S3 bucket. This project demonstrates API integration, cloud storage, and automation.

## Features
- Fetches live weather data from OpenWeather API.
- Saves weather data as JSON files in AWS S3.
- Automates data collection for multiple cities.
- Error handling for failed API requests and AWS interactions.

## Technologies Used
- **Python 3**
- **OpenWeather API**
- **AWS S3 (Boto3 SDK)**
- **Requests Library**
- **Dotenv for Environment Variables**

## Prerequisites
Ensure you have the following before running the project:
- **Python 3+ installed**
- **AWS account** with an S3 bucket
- **OpenWeather API key** (Get one from [OpenWeather](https://openweathermap.org/))
- **Required Python libraries** (Install with `pip install boto3 requests python-dotenv`)

## Setup Instructions
### 1. Clone the Repository
```sh
git clone https://github.com/yourusername/weather-dashboard.git
cd weather-dashboard
```

### 2. Create a `.env` File
Create a `.env` file in the project directory and add the following credentials:
```
OPENWEATHER_API_KEY=your_openweather_api_key
AWS_BUCKET_NAME=your_s3_bucket_name
```

### 3. Install Dependencies
```sh
pip install -r requirements.txt
```

### 4. Run the Script
```sh
python weather_dashboard.py
```

## Code Overview
### Main Functions
- **`fetch_weather(city)`** - Fetches weather data from OpenWeather API.
- **`create_bucket_if_not_exists()`** - Ensures the S3 bucket exists before storing data.
- **`save_to_s3(weather_data, city)`** - Saves weather data as a JSON file in AWS S3.
- **`main()`** - Runs the script for predefined cities and automates data storage.

## Example Output
```
Fetching weather for Lagos...
Temperature: 85°F
Feels like: 88°F
Humidity: 70%
Conditions: Clear sky
Successfully saved data for Lagos to S3!
```

## Future Enhancements
- Schedule automated data collection using **AWS Lambda**.
- Create a **Streamlit dashboard** for visualizing weather trends.
- Use **AWS Athena** for querying stored weather data.

## Contributing
Feel free to fork the repository and submit pull requests to improve the project!

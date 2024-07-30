# Flask Hand Tracking Application

This project is a Flask web application that uses MediaPipe and OpenCV to track hand gestures through a webcam feed. The application detects the number of fingers raised and sends this data to an Arduino server.

## Project Structure


    projects/
    │
    ├── app.py
    ├── requirements.txt
    ├── static/
    │ └── (static files like CSS, JS, images)
    └── templates/
    └── index.html




## Requirements

- Python 3.6+
- Flask
- OpenCV
- MediaPipe
- Requests

## Installation

1. Clone the repository or download the project files.

2. Navigate to the project directory.

3. Create a virtual environment and activate it:
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

4. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

## Running the Application

1. Start the Flask application:
    ```bash
    python app.py
    ```

2. Open your web browser and go to `http://127.0.0.1:5000` to see the application.

## Usage

- The application will access your webcam to track hand gestures.
- Place your hand inside the on-screen square to detect and count the number of fingers raised.
- The detected number of fingers will be sent to the Arduino server specified by the `server_ip` in `app.py`.

## Endpoints

- `/` - Home page.
- `/start` - Start video capture.
- `/stop` - Stop video capture.
- `/video_feed` - Video feed endpoint.

## Arduino Server

Ensure your Arduino server is running and accessible at the IP address specified in the `server_ip` variable in `app.py`.

## License

This project is licensed under the MIT License.

# kafka-docker-sentiment-dashboard
A real-time sentiment analysis dashboard that processes Reddit data using Kafka and Docker. The project consumes Reddit posts from a specified subreddit, performs sentiment analysis on the text, and stores the results in a Kafka stream. The dashboard visualizes the sentiment in real-time.

Description
This project is a real-time sentiment analysis dashboard that collects Reddit posts from a specified subreddit, performs sentiment analysis on the posts, and visualizes the sentiment in real-time using a Kafka-based pipeline. The project is containerized using Docker, making it easy to deploy and run in any environment.

Key Features:

Collects Reddit data in real-time using Kafka producers and consumers.
Performs sentiment analysis on Reddit posts.
Streams data to Kafka and visualizes results using a Python dashboard.
Dockerized for easy deployment with pre-configured Docker Compose services.
Technologies Used
Kafka: Distributed streaming platform used for real-time data processing.
Docker: Containerization platform used to create and manage containers for the application.
Python: Programming language used for sentiment analysis and handling data processing.
Docker Compose: Used to manage multi-container Docker applications (Kafka, Zookeeper, and your consumer/producer scripts).
pandas: Data manipulation library for processing data.
Matplotlib: Visualization library for generating graphs and charts.
Prerequisites
Before running this project, ensure you have the following installed:

Docker (with Docker Compose)
Python 3.x (with pip)

#Setup Instructions

##Clone the repository:

˜bash
git clone https://github.com/yourusername/kafka-docker-sentiment-dashboard.git
cd kafka-docker-sentiment-dashboard
Set up Kafka and Zookeeper using Docker:

##Make sure Docker Desktop is running on your system.
Start the Kafka and Zookeeper containers using Docker Compose:
˜bash
docker-compose up -d
Install required Python libraries:

##Create a virtual environment (optional but recommended):
˜bash
python3 -m venv venv
source venv/bin/activate  # On Windows, use venv\Scripts\activate


##Install dependencies:
˜bash
pip install -r requirements.txt
Execution Steps
Run Kafka Producers:

##Ensure Kafka and Zookeeper are running.

##Run the producer script to start sending data (Reddit posts) to Kafka:
˜bash
python3 producer_script.py
This will start sending Reddit data to the Kafka topic.
Run the Consumer Script:

##Run the consumer script to consume data from Kafka and process the sentiment:
˜bash
python3 consumer_script.py
Real-time Sentiment Analysis:

###The consumer script will process the data, perform sentiment analysis, and print out the results (or store them in a data structure or database).
You can modify the consumer script to visualize or export the analysis results (e.g., using matplotlib for visualizing the sentiment scores).

#Project Structure
˜bash
kafka-docker-sentiment-dashboard/
│
├── consumer_script.py       # Kafka consumer for sentiment analysis
├── producer_script.py       # Kafka producer to fetch Reddit posts
├── requirements.txt         # Python dependencies
├── docker-compose.yml       # Docker Compose configuration for Kafka and Zookeeper
├── Dockerfile               # Dockerfile for building the consumer/producer container
├── README.md                # Project documentation (this file)


Additional Notes
You can modify the Kafka producer to pull data from any subreddit by adjusting the Reddit API URL and parameters.
The sentiment analysis model can be customized to improve accuracy by training on more specific datasets.

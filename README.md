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

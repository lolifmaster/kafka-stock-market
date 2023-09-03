# Kafka to Azure Blob Storage Data Pipeline

This project demonstrates the setup and implementation of a data pipeline using Apache Kafka, Apache ZooKeeper, and Microsoft Azure Blob Storage. The pipeline involves a Kafka producer that ingests data from a CSV file and a Kafka consumer that subscribes to this data stream, processes it, and then writes it into Azure Blob Storage.

## Project Components

### 1. Azure Virtual Machine (VM)

We utilize an Azure Virtual Machine to host the Kafka server and ZooKeeper, providing the infrastructure for our data pipeline. The VM serves as the central hub for data ingestion and processing.

### 2. Apache Kafka

Kafka is a distributed event streaming platform that allows for the ingestion, storage, and real-time processing of large volumes of data. In this project, Kafka is used to handle data streams.

### 3. Apache ZooKeeper

ZooKeeper is a distributed coordination service that helps manage and synchronize distributed systems. It is an integral part of the Kafka ecosystem and ensures the coordination of Kafka brokers.

### 4. Kafka Producer

The Kafka producer is responsible for reading data from a CSV file and sending it as messages to a Kafka topic. It simulates data ingestion into the pipeline.

### 5. Kafka Consumer

The Kafka consumer subscribes to the Kafka topic where data is being produced. It processes the incoming data and writes it into Azure Blob Storage for long-term storage and analysis.

### 6. Azure Blob Storage

Azure Blob Storage is a scalable object storage service provided by Microsoft Azure. It is used for storing the processed data from the Kafka consumer, making it available for future analysis and retrieval.

## Setup and Configuration

To run this project, follow these steps:

1. **Azure VM Setup**: 
   - Create an Azure Virtual Machine and configure it as the Kafka server and ZooKeeper node.
   - Ensure you have the necessary network and firewall rules in place to allow communication.

2. **Kafka and ZooKeeper Installation**:
   - Install Kafka and ZooKeeper on the Azure VM.
   - Configure Kafka topics and ZooKeeper for coordination.

3. **Kafka Producer**:
   - Implement the Kafka producer code to read data from a CSV file and send it to the Kafka topic.

4. **Kafka Consumer**:
   - Implement the Kafka consumer to subscribe to the Kafka topic and write data to Azure Blob Storage.

5. **Azure Blob Storage Configuration**:
   - Set up Azure Blob Storage and create containers to store the data.
   - Ensure you have the necessary Azure credentials for accessing the storage account.

6. **Run the Pipeline**:
   - Start the Kafka server and ZooKeeper on the Azure VM.
   - Run the Kafka producer to ingest data.
   - Run the Kafka consumer to process and store data in Azure Blob Storage.

## Dependencies

List any dependencies and libraries used in your project.

- Apache Kafka
- Apache ZooKeeper
- Azure Blob Storage SDK
- Any other relevant libraries

## Usage

Provide instructions on how to run and use your project.

```bash
# Example commands
./start_kafka.sh   # Start Kafka and ZooKeeper on the Azure VM
python kafka_producer.py   # Run the Kafka producer
python kafka_consumer.py   # Run the Kafka consumer

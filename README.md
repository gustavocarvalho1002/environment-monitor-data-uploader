# Real-Time Environment Monitor - Data Uploader
**"Cloud-powered sensor tracking with Raspberry Pi technology."**

This repository contains the **Data Uploader**, a core service within the Real-Time Environment Monitor project. The entire solution comprises multiple apps designed to collect, process, and display environmental sensor data. This specific repository handles uploading the locally stored data to the cloud.

## Overview
The **Data Uploader** is a .NET Worker Service running on the Raspberry Pi. It retrieves sensor data from the local SQLite database every 2 minutes and uploads it to the cloud via a REST API.

## Features
- Periodically reads data from the local SQLite database.
- Sends batches of data to the **Data Ingestion API** hosted on Azure.
- Configurable upload interval (default: every 2 minutes).

## Requirements
- .NET SDK (version X.X)
- SQLite installed locally on the Raspberry Pi.
- Access to the **Data Ingestion API** in Azure Cloud.

## How to Run
1. Clone this repository to your Raspberry Pi.
2. Navigate to the project directory.
3. Build and run the worker:
    ```bash
    dotnet build
    dotnet run
    ```

## Configuration
The REST API URL and upload interval can be configured in the `appsettings.json` file.

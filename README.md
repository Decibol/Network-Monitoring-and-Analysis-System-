
# Network Monitoring and Analysis System

This project contains scripts to monitor and analyze network statistics, focusing on tracking network throughput, packet success rate, and packet loss in real time. The system collects network activity data and stores it in an Excel file for further analysis and visualization.


## Introduction

The **Network Monitoring System** provides a set of tools to monitor network performance metrics like throughput and packet loss in real time. It logs the data into an Excel file and visualizes the performance over time.

## Features

- **Real-Time Monitoring**: Track network activity with live updates on bytes sent/received and packet success rates.
- **Data Logging**: Store network performance data in an Excel file for historical analysis.
- **Visualizations**: Graph network throughput, packet success rate, and packet loss over time.
- **Asynchronous Monitoring**: Leverage Python's `asyncio` for efficient, non-blocking data collection.

## Installation

### Prerequisites

- Python 3.x
- Required libraries: Install the dependencies using `pip`:

    ```bash
    pip install pandas openpyxl matplotlib seaborn psutil
    ```

### Setup

1. Clone the repository:
    ```bash
    git clone https://github.com/tusharahlawat/Network-Monitoring.git
    ```

2. Navigate to the project directory:
    ```bash
    cd Network-Monitoring
    ```

3. Install the dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

### 1. Data Collection

The **data collection** script asynchronously collects network statistics (bytes and packets sent/received) and logs them into an Excel file (`network_stats.xlsx`).

To start the data collection:
```bash
python data_collection.py
```

This will begin logging the data every second (configurable) into the Excel file.

### 2. Monitoring

For real-time monitoring of network throughput and packet statistics, use the **monitoring script**.

To monitor network data:
```bash
python monitoring.py
```

This script reads the logged data from `network_stats.xlsx`, calculates throughput and packet statistics, and visualizes them using plots.

### 3. Clearing Data

If you want to reset the network data and clear the existing logs in the Excel file, use the **clear script**:
```bash
python clear.py
```

This script will remove all entries from `network_stats.xlsx` so you can start fresh.

### 4. Visualization

The **monitoring script** also generates visualizations for the following metrics:
- **Throughput**: Bytes sent and received over time.
- **Packet Success Rate**: Percentage of successful packet deliveries.
- **Packet Loss**: The number of packets lost over time.

The visualizations will automatically display when running `monitoring.py`.

## File Descriptions

- **`app2.py`**: Placeholder for additional functionality or future extensions related to the network monitoring system.
- **`clear.py`**: Clears the data from `network_stats.xlsx`, allowing a fresh start.
- **`data_collection.py`**: Asynchronously collects network statistics and writes them to `network_stats.xlsx`.
- **`monitoring.py`**: Reads data from the Excel file, calculates throughput, packet success rates, and packet loss, and visualizes them with plots.
- **`network_stats.xlsx`**: The Excel file where network statistics are logged and stored for analysis.


## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

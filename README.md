# 📊 Data Capture and Analysis with Classic Patterns Using Mastodon API

## 🚀 Objective
The goal of this project is to demonstrate the implementation of classic data capture and analysis patterns in a real-world environment using the **Mastodon API**. This includes leveraging real-time data processing techniques, such as request/response patterns, temporal aggregations, and incremental analysis of streaming data. The focus is on collecting raw social media data, processing it efficiently, and visualizing trends to derive actionable insights.

---

## 🛠️ Workflow

### 1. **Environment Setup**
To get started, the following steps are required:

- **Register an application in Mastodon**: Obtain credentials (Client Key, Client Secret, Access Token) to interact with the API.
- **Install libraries**:
  - `mastodon.py` for API interactions.
  - `pandas` for data analysis.
  - `matplotlib` for visualization.
- **Configure the Python environment**: Ensure the development environment is ready and can connect to a Mastodon instance (e.g., `mastodon.social`).

---

### 2. **Data Capture with Request/Response Pattern**

- Use Mastodon API methods to fetch data:
  - **Timeline data** or **Search data** by hashtag/keyword.
  - Process returned **JSON objects** and extract relevant fields like:
    - `created_at`: Timestamp of the toot.
    - `account`: User information.
    - `content`: Text content of the toot.
  
- **Example queries**:
  - Fetch the latest toots for a specific hashtag (e.g., `#war`).
  - Extract metadata like the number of **favorites** and **followers**.

---

### 3. **Data Transformation and Tabular Analysis**

- **Transform JSON data** into **Pandas DataFrames**:
  - Extract useful columns: `created_at`, `content`, `favorite_count`.
  - **Group and summarize** data (e.g., count toots per day).
  
- **Advanced Pandas operations**:
  - **Groupby** operations to aggregate by time or user.
  - Use filters to clean the data.

---

### 4. **Streaming Data Capture**

- **Real-time data collection**:
  - Capture new data at fixed intervals (e.g., every 7 seconds).
  - Remove duplicates based on toot IDs to avoid redundant processing.
  
- **Handle live data** with in-memory buffers:
  - Capture toots with a specific hashtag in real time and display them dynamically.

---

### 5. **User and Metadata Analysis**

- **Aggregate user information**:
  - Count the total number of toots created by each user.
  - Track followers and interaction metrics.
  - Identify the most **active or influential** users based on their activity.
  
- Store user data in **Python dictionaries** for analysis and aggregation.

---

### 6. **Visualization**

- **Generate visualizations** using **Matplotlib**:
  - **Bar charts**: Display toot distribution by user.
  - **Time series**: Show hashtag activity trends over time.

- **Transform data for visualization**:
  - Convert timestamps to human-readable formats.
  - Aggregate data into appropriate time intervals.

---

### 7. **Temporal Analysis and Sliding Windows**

- **Handle timestamps**:
  - Convert and process UTC timestamps from the API.
  
- **Implement sliding windows** to analyze data within specific time frames (e.g., the last 15 minutes):
  - **Example**: Count toots generated within a 15-minute window.

---

## 📝 Key Exercises

1. **Extract the 10 most recent toots with a hashtag**:
   - Display information like date, author ID, and toot content.
   - Track unique users using a set.

2. **Calculate user-specific statistics**:
   - Number of toots created.
   - Follower count.
   - Visualize toot distribution by user with a **bar chart**.

3. **Build a time series**:
   - Analyze hashtag frequency over time.
   - Create **line plots** for temporal aggregations.

4. **Continuous Streaming Capture**:
   - Fetch new data every 7 seconds and remove duplicates.
   - Show toots in real-time.

5. **Real-Time Analysis**:
   - Count toots related to a hashtag every 10 seconds in **sliding windows** (15 minutes).
   - Update the results continuously.

---

## 🧰 Technologies and Libraries Used

- **Python**: The primary language for the implementation.
- **mastodon.py**: For API interactions and data extraction.
- **Pandas**: For efficient data manipulation and transformation.
- **Matplotlib**: To create charts and visualizations.
- **Datetime**: For working with time-based data and implementing sliding windows.

---

## 📈 Results

This project demonstrates the implementation of **classic data capture patterns** and **real-time data stream processing**. By using the Mastodon API, the project simulates a data pipeline that can capture, analyze, and visualize real-time social media activity.

The project provides a practical application of:
- **API integrations** for data collection.
- **Data wrangling** techniques to clean and format raw data.
- **Real-time data processing** for continuous data capture and analysis.
  
Through this project, essential skills for working with **streaming data** and **API-based systems** are developed and demonstrated in an interactive manner.

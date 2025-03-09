
# Logistics Performance Index (LPI) Agentic Application

**Submitted by: Gift Ahmed**

---

## Overview

This repository contains a Jupyter Notebook that demonstrates an end-to-end solution for a Logistics Performance Index (LPI) graph analytics application. The project covers the following:

- Data processing and conversion of an LPI dataset into a graph.
- Persistence and loading of the graph data into ArangoDB.
- Visualization of the graph and subgraphs using NetworkX and Matplotlib.
- An Agentic Application that dynamically retrieves and processes natural language queries based on intent (using AQL and NetworkX/cuGraph safe paths).
- Integration of multiple agent tools (Simple AQL queries, Complex Analytics via NetworkX/cuGraph, and Hybrid queries) to provide robust query handling.

Additionally, this project includes a 5-10 minute public YouTube video that details the development process and functionality of the application.

---

## YouTube Video Overview

The YouTube video demonstrates:
- **Background and Motivation:**  
  My background and why I participated in this challenge.
- **Dataset Selection and Business Problem:**  
  An explanation of the chosen LPI dataset, the business problem it addresses (e.g., assessing global logistics performance and identifying areas for improvement).
- **Data Conversion:**  
  How I converted the LPI dataset into a graph, including preprocessing steps and attribute mapping.
- **Persistence & Loading:**  
  Steps taken to persist the graph into ArangoDB and then load it back for analysis.
- **Graph Visualization:**  
  A sample visualization of the graph and key subgraphs.
- **Agentic Application Walk-through:**  
  A detailed explanation of the Jupyter Notebook components, including the different agent tools used (Simple AQL, Complex Analytics, Hybrid Queries).
- **Real-Time Demo:**  
  A live demo showing how the agentic app processes natural language queries and retrieves graph insights and visualizations.

Watch the video here: [YouTube Video Link](https://youtu.be/your_video_link)

---

## Repository Structure

- **notebook.ipynb**  
  The main Jupyter Notebook containing the full solution, including data preprocessing, graph building, persistence in ArangoDB, visualization, and agentic query processing.

- **README.md**  
  This documentation file.

- **requirements.txt**  
  A list of Python dependencies required to run the project.

---

## Installation and Setup

1. **Clone the Repository:**

   ```bash
   https://github.com/giftahmed/Logistics-Performance-Index-LPI-Agentic-Application.git
   ```

2. **Set Up a Virtual Environment (Optional but recommended):**

   ```bash
   python3 -m venv venv
   source venv/bin/activate  # For Linux/Mac\nvenv\\Scripts\\activate  # For Windows
   ```

3. **Install Dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

4. **Configure ArangoDB:**

   Ensure that you have an ArangoDB instance running and update the connection settings in the notebook (or a configuration file) accordingly.

5. **Run the Notebook:**

   Launch the Jupyter Notebook:

   ```bash
   Gift_Ahmed_Agentic_Graph_Querying_with_LangChain_&_cuGraph_AQL_&_GPU_Accelerated_Analytics (1).ipynb

   ```

---

## Usage

The solution is organized as follows:

- **Data Preprocessing:**  
  The notebook cleans and preprocesses the LPI dataset, maps and renames columns, and handles missing values.

- **Graph Building:**  
  The preprocessed data is converted into a graph using NetworkX. Country nodes and Year nodes are added with their respective attributes. Edges are created to represent relationships (e.g., a country’s performance in a specific year).

- **Graph Persistence:**  
  The notebook demonstrates how to persist and load the graph data into ArangoDB.

- **Visualization:**  
  Various visualization techniques are used to display the graph and subgraphs using NetworkX and Matplotlib.

- **Agentic Application:**  
  The application includes multiple tools to handle natural language queries:
  - **Simple AQL Queries:** Direct lookups from the dataset.
  - **Complex Analytics Queries:** Advanced graph algorithms using NetworkX/cuGraph.
  - **Hybrid Queries:** A combination of AQL and graph analytics.
  
  The agent dynamically processes queries based on intent. Users can input any query through the Gradio interface, and the system will return a natural language answer.

- **Real-Time Demo:**  
  The Gradio app is deployed, allowing users to enter queries and see the corresponding responses in real-time.

---

## Example Queries

Below are a few examples used in the demo (also explained in the YouTube video):

### Simple AQL Queries
- **"Get LPI Score for Germany"**  
- **"Show the LPI details for Singapore for the most recent year available."**

### Complex Analytics Queries
- **"Identify the most influential country in the global logistics network based on LPI metrics from 2017 to 2023."**  
- **"What is the shortest path between the United States and China in the logistics network?"**

### Hybrid Queries
- **"Retrieve Countries with LPI Score Above 4.0 in the year 2023."**  
- **"List Top 5 Countries by Customs Score."**

---

## Running the Gradio App

To launch the Gradio application that handles natural language queries:

```python
import gradio as gr
gr.Interface(
    fn=hybrid_query_to_text,
    inputs="text",
    outputs="text",
    title="Graph Query Agent",
    description="Enter your query to retrieve insights from the LPI graph."
).launch(share=True)
```

---

## Contact

For any questions or further collaboration, please contact [giftahmed2@gmail.com](mailto:giftahmed2@gmail.com).

---
Thank you, kindly Like and share.
Happy coding!

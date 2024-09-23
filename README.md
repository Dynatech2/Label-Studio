# Label-Studio

Label Studio is a versatile open-source data labeling tool that allows you to annotate images, video, audio, text, and more. This guide provides instructions on how to install, set up, and use Label Studio for annotating datasets to train YOLOv8 models for object detection tasks.

## Table of Contents
- [Installation](#installation)
- [Launching Label Studio](#launching-label-studio)
- [Multiple Users](#multiple-users-to-acess-label-studio)
- [Annotating Data](#annotating-data)
- [Exporting Annotations for YOLOv8](#exporting-annotations-for-yolov8)
- [Useful Links](#useful-links)

----

## Installation

### Prerequisites
- Python 3.7 or higher
- pip (Python package installer)

### Step-by-Step Guide

1. **Create a virtual environment**:
   ```
   python -m venv env
   ```
2. **Activate the Virtual Environment**:

   - **Windows**:
      ```
      .\env\Scripts\Activate
      ```
   - **Linux**:
      ```
      source env/bin/activate
      ```
3. **Install Label Studio**:
   
   ```
   python -m pip install label-studio
   ```
---
## Launching Label Studio    

1. **Activate the Virtual Environment**:

   - **Windows**:
      ```
      .\env\Scripts\Activate
      ```
   - **Linux**:
      ```
      source env/bin/activate
      ```
3. **Start Label Studio** by running the following command in your terminal:
   ```
   label-studio
   ```
4. Once the application starts, open your web browser and navigate to http://localhost:8080. You will see the Label Studio interface.
5. **Create an account** or log in to Label Studio to access your project dashboard.

----
## Multiple Users

To allow multiple users to access Label Studio on the same network, follow these steps:

1. **Run Label Studio on the Host Machine**:
   
   Ensure that Label Studio is running on a machine connected to the local network. To start Label Studio, use:
   ```
   label-studio
   ```
2. **Find Your Local IP Address**
   
   **Windows**:
   
   - Open Command Prompt and run:
     ```
     ipconfig
     ```
   **Linux**:

   - Open a terminal and run:
  
     ```
     ifconfig
     ```
3. **Obtain the Access Token**

   1. **Log in to Label Studio**:
      - Open your browser and navigate to http://localhost:8080.
      - Log in with your credentials.

   2. **Navigate to Account & Settings**:
      - Click on your profile icon in the top right corner.
      - Select Account & Settings.

   3. **Find the Access Token**:
      - In the API Tokens or Access Tokens section, your access token will be listed. If it’s not there, generate a new token

   4. **Copy the Access Token**:
      - Copy the token for later use.

4. **Construct the Access URL for Users**

   Use the following format to create the access URL for others:
   ```
   http://<IP_address>:<Port>/?token=<Access_Token>
   ```
   **Example**:
   If the IP address is 192.168.35.9, the port is 8080, and the token is bFTm4Ur10q1hl2Eno8XXAKWHj148YP366y80E7rV, the URL will be:
   ```
   http://192.168.35.9:8080/?token=bFTm4Ur10q1hl2Eno8XXAKWHj148YP366y80E7rV
   ```

5. **Share the Access URL with Users**
   Provide the constructed URL to other users who need to access Label Studio.

6. **User Access**
   - Ensure that all users are connected to the same Wi-Fi network as the host machine.
   - Users can access Label Studio by entering the provided URL in their web browsers.
   
----
## Annotating Data

1. **Create a new project**:
   - Click **Create Project** in the top-right corner.
   - Enter a **Project Name** (required) and an optional description.
   - Click **Save** to create the project.
2. **Import Data**:
   - Upload local files directly or configure cloud storage for larger datasets.
   - You can import data immediately or later from the **Data Import** tab.
3. **Set Up Labeling Interface**:
   - Choose a template for annotation. For object detection, use the **Bounding Boxes** template.
   - Add label names for the objects you’ll be annotating (e.g., "Class1", "Class2").
   - Click **Save** once you're done.

**Labeling Guide**

Now that your project is set up, you can start annotating your data:
1. Open your project in Label Studio.
2. Click **Label All Tasks** to start labeling the data.
3. Use your mouse or keyboard shortcuts to draw bounding boxes and assign labels.
4. Submit each annotation as you complete it.
5. You can collaborate with other annotators to improve data quality.




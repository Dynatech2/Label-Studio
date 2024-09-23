# Label-Studio

Label Studio is a versatile open-source data labeling tool that allows you to annotate images, video, audio, text, and more. This guide provides instructions on how to install, set up, and use Label Studio for annotating datasets to train YOLOv8 models for object detection tasks.

## Table of Contents
- [Installation](#installation)
- [Launching Label Studio](#launching-label-studio)
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




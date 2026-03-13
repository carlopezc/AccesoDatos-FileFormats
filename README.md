# 📂 Java Data Persistence & Formats

![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Data Persistence](https://img.shields.io/badge/Data%20Persistence-000000?style=for-the-badge)

> A Java application demonstrating data modeling, interoperability, and persistence across multiple file formats (TXT/CSV, Binary, XML/SVG, and JSON).

---

## 🎯 Project Overview

This project was developed for the "Acceso a Datos" (Data Access) module of my higher degree studies. The main objective is to understand and implement reading, writing, and validation of data using various standard file formats. 

The application revolves around an "Integrator Case" where a graphical scene (composed of a canvas and geometric shapes like rectangles, circles, and lines) is represented, parsed, and exported across four completely different data structures.

## 🛠️ Features & Implementation

The core logic handles a generic data model (the "Scene") and translates it back and forth between the following formats:

* **TXT / CSV (Text files):**
    * Line-by-line parsing and field extraction.
    * Implementation of basic data validation rules (handling corrupted or incorrectly formatted files).
    * *Use case:* Simple, human-readable logging and basic sensor data.
* **Binary & Object Serialization:**
    * Direct serialization of Java objects to binary files.
    * *Use case:* Exact state recovery, efficient storage, and configuration backups where data doesn't need to be human-editable.
* **XML (DOM to SVG):**
    * Mapping the internal data model to a hierarchical XML tree using the DOM API.
    * Exporting the data as a valid, renderable `.svg` image file.
    * *Use case:* Structured configuration, vector graphics, and interoperability with design tools.
* **JSON:**
    * Converting the scene into a structured, lightweight JSON object.
    * *Use case:* Standard data exchange format for Web/Mobile APIs and modern frontend applications.

## ⚙️ How it works

The project manages a central `FileManager` class that coordinates the import and export operations. 

For example, a simple text input defining a scene:
```txt
dimensiones 500 500
rectangulo 10 10 400 400 #aaaaaa
circulo 250 250 120 #aaaaaa

# Grazioso Salvare Dashboard - README

## Project Overview
This project involves building an interactive web dashboard for Grazioso Salvare, a company specializing in rescue-animal training. The dashboard allows users to filter, view, and analyze data from animal shelters to identify potential rescue dogs. The project was developed using **Dash (Plotly)** for the web interface and **MongoDB** for database management, with a **CRUD Python module** to facilitate communication between the dashboard and the database.

## Required Functionality
The dashboard provides the following key functionalities:
- **Interactive Filtering Options:** Users can filter dogs based on rescue type:
  - Water Rescue
  - Mountain or Wilderness Rescue
  - Disaster or Individual Tracking
  - Reset (returns to the unfiltered state)
- **Data Table:** Displays real-time shelter data based on user selection.
- **Geolocation Map:** Displays the selected dog's location.
- **Pie Chart Visualization:** Shows breed distribution based on the filtered data.
- **Grazioso Salvare Branding:** The dashboard includes the company's logo linked to their website.
- **Unique Identifier:** Displays the developer's name for identification.

## Screenshots (Proof of Functionality)
The following screenshots demonstrate that all functionalities were successfully implemented:
1. **Starting State of the Dashboard:** Shows filter options, data table, and charts before applying any filters.
2. **Water Rescue Filter Execution:** Displays dogs meeting the criteria for water rescue.
3. **Mountain or Wilderness Rescue Filter Execution:** Displays dogs suitable for mountain or wilderness rescue.
4. **Disaster or Individual Tracking Filter Execution:** Displays dogs ideal for disaster or tracking operations.
5. **Reset Functionality:** Demonstrates that all widgets return to their original, unfiltered state.

## Tools Used and Rationale
### **Programming Languages & Frameworks**
- **Python:** Used for backend development and data manipulation.
- **Dash (Plotly):** Provides an interactive web-based dashboard framework.
- **Pandas:** Used for data handling and transformation.
- **Dash Leaflet:** Integrated for geolocation mapping.
- **Plotly Express:** Used for data visualization (pie chart representation of breeds).

### **Database & Connectivity**
- **MongoDB:** Chosen as the backend database due to its:
  - **Flexibility:** Handles dynamic, document-based structures.
  - **Scalability:** Supports efficient querying and large dataset storage.
  - **Seamless Python Integration:** Enables CRUD operations through **PyMongo**.
- **CRUD Python Module:** A reusable module that connects the database to the dashboard and ensures efficient data retrieval and updates.

## **How the CRUD Python Module Helps Maintainability**
The **CRUD Python module** from **Project One** enabled efficient communication between MongoDB and the dashboard in **Project Two**. Instead of writing repetitive database queries, the module encapsulates common operations (Create, Read, Update, Delete), making the code:
- **Maintainable:** Changes to the database structure only require updates in the module.
- **Readable:** Separates data logic from the user interface, making it easier to debug.
- **Adaptable:** The module can be reused for future applications involving MongoDB.

This module can be extended in the future for other projects requiring data retrieval and filtering from MongoDB databases.

## **Approach to Problem-Solving as a Computer Scientist**
To meet **Grazioso Salvare’s** database and dashboard requirements, the approach included:
1. **Understanding Requirements:** Reading through specifications to identify the key features needed.
2. **Modular Development:** Creating a reusable **CRUD module** for easy database interaction.
3. **Testing and Debugging:** Running queries directly in MongoDB before implementing them in the Python code.
4. **User-Centered Design:** Ensuring the dashboard is intuitive and meets client needs.

This project differed from previous assignments as it required **real-world problem-solving**:
- Working with **real-time data** rather than static files.
- Implementing a **full-stack solution** connecting a database to a live dashboard.
- **Interacting with APIs and MongoDB** for filtering and dynamic content updates.

For future projects, similar strategies such as **modular programming, thorough database design, and efficient debugging techniques** will be used to meet client requirements.

## **Why Computer Science Matters**
Computer scientists design and implement systems that **automate processes, analyze data, and provide insights** to businesses. This project illustrates how computational thinking can:
- Improve **data accessibility** for companies like Grazioso Salvare.
- Enable **better decision-making** by visualizing trends in animal shelter data.
- Reduce **manual workload** by **automating data retrieval and filtering**.

Through projects like this, companies can efficiently identify and train rescue dogs, ultimately **saving lives and improving rescue operations.**

## **Steps to Reproduce the Project**
1. **Import the Dataset into MongoDB:**
   ```sh
   mongoimport --username="${MONGO_USER}" \
   --password="${MONGO_PASS}" --port=${MONGO_PORT} \
   --host=${MONGO_HOST} --db AAC2 --collection animals \
   --authenticationDatabase admin --type csv --headerline --drop ./aac_shelter_outcomes.csv

# Project Title: Djenga

## Project Overview
Extracting material information from BIM models in real-time.

## Business and Market Demands
Architects, builders, designers, and quantity surveyors need immediate access to material information for their structures to better manage design and financial outcomes.

## Sustainable Development Goals
- Sustainable Cities and Communities (SDG 11)
- Responsible Consumption and Production (SDG 12)

## Long-Term Objective
- To completely democratise access to real-time material information for buildings.
- To enhance the optimisation of building materials for each project by 50%.

## Success Metrics
- Achieve a 30% improvement in material optimisation and secure 400 active users per month.

## Strategic Advantage
- Exploit the decentralised nature of construction technology to lead the building materials sector in East Africa.

## User Journey Mapping

### Define the User
- Target Users: Architects, Designers, Quantity Surveyors, Contractors, Builders, Master Builders
- The Modeler: Creates Revit models

### Define the Actions
- **Architect**: Designs and generates models, obtains material data, compares different types of slabs, and optimises the design for material use.
- **Contractor**: Calculates the quantity of materials needed to build a wall, slab, etc.
- **Quantity Surveyor**: Receives an Excel spreadsheet detailing all material quantities to update and input appropriate rates.
- **Client/Builder**: Receives a spreadsheet with all material quantities for procurement and pricing from various suppliers.

### Pain and Benefit Analysis
- **Task**: Obtain Material Data
- **Challenges**: Traditionally, material data is provided only after the design phase rather than during it. Quantity surveyors calculate materials from drawings and estimate the needed quantities for each component.
- **Benefits**: Gain real-time material data from BIM models, receive precise material estimates, and optimise material usage early in the design process.

## Features to Develop

### User Requirements:
- Real-time data on the quantities of materials needed for constructing elements, starting with floor slabs and potentially extending to other structures such as bungalows.

### User Desires:
- Details on materials required for different elements.
- Generate an Excel sheet with all material quantities and an empty column for rates.
- Track changes in material quantities throughout the design process (each request for material data saves a previous version).
- Generative design to optimise the installation and placement of each material.

## Development Tools
- Python 2.7/IronPython/RevitPythonShell
- Pyrevit
- RevitAPI
- Autodesk Revit 2022/Revit Lookup
- Panda

## Development Process - Iteration 01
- Extract the area, thickness, perimeter, and volume of the ground slab from the Revit Model using RevitAPI.
- **DPM (Damp Proof Membrane)**: Function to determine the required length of DPM and the remaining length.
- **BRC Mesh**: Function to determine the length of BRC Mesh required (to cover the entire slab and the number of rolls needed), and the remaining length of BRC Mesh.
- **Concrete**: Function to calculate the volume of sand, ballast, and cement required, and the number of cement bags needed.
- **Data Sharing**: Project details (project name, project unit area); element details (element category, element type); and material details (noting that the type of element affects the materials used).
- **An add-in/plugin with these features**:
  - **Element Selection**: User chooses an element for analysis, such as a floor.
  - **Element Type**: User specifies the type of element, such as a concrete floor slab.
  - **Element Breakdown**: Generates a list of all required materials, including their quantities and units, e.g., cement, cement volume, number of cement bags.
  - **Element Export**: Export to PDF or Excel for quoting, pricing, and sharing; save the list to Excel using Panda.


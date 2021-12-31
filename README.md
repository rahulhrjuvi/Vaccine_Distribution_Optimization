# Vaccine Distribution Optimization Model

## Business Context
Build a linear optimization model which identifies potential vaccine distribution center locations among the cities within each state in the US and allocates each city to a distribution center in its vicinity.

## Model
- Optimization model is built on python and an instance of the model for Wisconsin state is illustrated in Excel
- The python file is named Vaccine_Distribution_Model.ipynb and the Excel model is named Excel_Model.xlsx
- Python is used to build the model because of its ability to scale in order to include all cities, towns and villages in the state provided we have population       census data
- Python library pyomo is used to formulate and solve the optimization model
- Google maps API is employed to construct the distance matrix for all the cities, towns and villages with the provided population data

## Input Parameters
- Cities and their population for the State under consideration
- Number of distribution centers allocated to state by the
  government
- Number of vaccine vials per shipment
- Google maps API key to access and create distance matrix for the cities

## Sample Input and Output
Sample inputs (Python Model)

<img width="187" alt="Screen Shot 2021-12-31 at 6 27 29 PM" src="https://user-images.githubusercontent.com/89796629/147841026-9b773cf0-6475-4cc4-b77a-5ac80f4f07a8.png">

<img width="538" alt="Screen Shot 2021-12-31 at 6 27 51 PM" src="https://user-images.githubusercontent.com/89796629/147841028-7df338ae-22d4-480d-8b17-94deb6b785f6.png">

Sample Output (Python Model)

<img width="658" alt="Screen Shot 2021-12-31 at 6 28 14 PM" src="https://user-images.githubusercontent.com/89796629/147841030-7feddcb9-af5d-4e72-8c72-92bbbdd10e91.png">

Screenshot of Excel Model

<img width="1105" alt="Screen Shot 2021-12-31 at 6 28 47 PM" src="https://user-images.githubusercontent.com/89796629/147841033-2856cd30-cf19-4a04-9e36-f8820db34a9d.png">

## How does the model work?
- The python model reads the state population data by city (excel file) and creates the distance matrix using Google maps API.
- Model calculates the number of trips required to meet vaccine requirement for each city based on its population and vials per shipment.
- Pyomo utilizes the distance matrix and number of trips required, applies constraints and minimizes the objective and gives the potential distribution centers     and cities assigned to them.

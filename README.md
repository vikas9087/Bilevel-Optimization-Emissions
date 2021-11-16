# Bilevel-Optimization-Emissions
Proposed a mathematical model for optimizing the profits and emissions while setting dynamic prices of electricity. A bilevel & multi-objective model is proposed for maximizing profits of retailer, minimizing the emissions produced, & minimizing the total cost of customers. Our models use [Time-of-Use(TOU)](https://news.energysage.com/understanding-time-of-use-rates/) price structure of [Demand Response Management](https://www.energy.gov/oe/activities/technology-development/grid-modernization-and-smart-grid/demand-response). We use following as the input data parameters.
1. `demand_profile.csv` contains the hourly demand for electricity in kWh. The Rows represent customers & each column corresponds hours beginning from 00:00 to 23:00.
2. `fuel_properties.csv` contains the attributes of fuels used in the thermal power plants. The attributes are unit costs, unit electricity produced, unit emissions prodcued.


`Model Building.ipynb` contains the Python script for data storing and optimization building. Here I have built several user defined function to solve the models. __Please note here to execute this file you first need to install the mathematical solver Gurobi__. For installation please visit [Gurobi](https://www.gurobi.com/)
  * There is one variable in 'Model Building.ipynb' `capacities` which means --> maximum percentage of supply available of each fuel type. For example, capacities = [.50, .60, .20] means that 50% of total electricity demand of customer can be satisfied using coal and similarly 60% by natural gas and so on.

Use `Data Visualization.ipynb` for the visualzation & summary of the results obtained from the models. For any further queries please contact me.

## Related Resources:
* This model is a work of Masters' thesis titled 'Bilevel and Multi-objective Optimization of Electricity Price Setting with Carbon Emission Consideration'. To read [click here](https://tigerprints.clemson.edu/cgi/viewcontent.cgi?article=4393&context=all_theses)
## Note:
I have written this python code as a novice and it can be improved or made efficient to some extent.

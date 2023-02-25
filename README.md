# transport_simulator
Java application consisting in a transport simulation through nodes in a network

# Description of the proposed problem
The problem of freight transportation management for a transportation company is to be addressed. The software allows to minimize the costs and time related to the shipment of goods with an optimal exploitation of the available resources through an intelligent store of the orders received; the orders are simulated (theoretically received from external sources in the case in question) in different cities in the database, saved on the database and, from this, are read to generate a useful graph for the creation of a number of fleets (consisting of planes, trains or trucks depending on the inputs) with associated constraints that will follow a specific path depending on the different goods they will receive. The path that the fleets will follow will occur on a graph having Italian cities as nodes. The application makes it possible to perform a simulation of the entire freight transport system from given input requirements, finally to save the day's statistics to the database; it is also possible to create a daily history so as to compare the days of the week in different weeks or, for example, to consider the comparison between months.

# Description of the management relevance of the problem
The problem to be addressed is a typical management problem of cost and time optimization in traversing a network of nodes, as well as purely forecasting; by creating fleets based on certain inputs and orders received, it is possible to have a better use of space, weight and cost of the available routes in each fleet with respect to the associated constraints and a specific optimal route for each of them that minimizes the time spent and the route taken in transporting all goods. Finally, the purpose of the application is to allow comparison of the results obtained from the simulation in different preset time periods so that decisions can be made for the future.

# Description of the data-sets for evaluation
The data-set used consists of:
- A "routes" table consisting of the routes from one city to another with the number of kilometers and emissions for different means with:
1.	City of departure
2.	City of arrival
3.	Distance in km
(In the case of road means, depending on the value of this distance, the arc of the graph may or may not be a highway, so the highest speed will be taken into account)
4) Means of transportation (bus, train, airplane)
5) Emissions (g)
Preliminary description of the algorithms involved
The algorithms involved are those related to graph problems on the computation of costs and paths typical of operations research:
- Minimum path problem: to minimize the number of nodes traversed (in the case of basic users)
DIJKSTRA ALGORITHM
- Minimum cost flow problem
SIMLEX ALGORITHM OR OTHER

# Preliminary description of the functionality provided for the software application.
Upon opening the application, the user is prompted to choose from 4 fields an option (days, weeks, months, years) with associated with each an input field that allows the user to enter the exact number of days or weeks or months or years for the simulation, after which the "SIMULATE ORDERS" button is enabled, which allows the user to simulate orders (with a city-to-city pattern) in the cities in the database with a certain weight and volume in the time instants included in the chosen period. The result of the simulation of orders is visible in the first output field immediately below. At this point, a drop-down is enabled in which the user can scroll through different types of transportation means (truck, train, airplane) and, with each of them, 4 input fields are associated (number, maximum transportable weight, average speed, hourly fuel cost) and a drop-down field in which the city from which the means (or means) depart(s) can be chosen; having entered all the parameters for a type of vehicle, it is possible to press an "ADD" button that allows the chosen vehicles to be added to the simulation for the generation of the various fleets (with this method it is also possible to add multiple vehicles of the same type but with different specifications, or with different source cities); an output field allows the created vehicles to be viewed line by line. Once the vehicles have been created, the "GENERATE GRAPH AND FLEETS" button is enabled, which allows you to create an undirected weighted graph having as nodes the cities present in the database and as arcs the distances in km between each connected city (always present in the database) and, in addition, to organize the vehicles into fleets based on the orders; in the same output field as before, it is possible to have confirmation of the correct creation of the graph and fleets. Finally, the "START SIMULATION" button is enabled, with which it is possible to launch the simulation of deliveries and have in output the results of all deliveries. A final "COMPARE" button allows you to organize the results on the basis of the first time inputs (if you chose "days," for each day there is information such as: number of orders received, number of deliveries made, total cost, average time taken, total emissions; if you chose months you will do the same thing on the basis of months, and so again regarding years); the results of the comparison are visible in an output field.

A demonstration of the use of the application: https://www.youtube.com/watch?v=5N6vxgUKjaM&t=18s

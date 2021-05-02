# Drone-Delivery-Stochastic-Simulation
Simulating the impacts of adverse weather events on a proposed drone delivery system.

This project is based off the paper “Analysis of Future UAS-Based Delivery – Balaban, Mastaglio, Lynch”.  The paper assessed the commercial use of UAS (Unmanned Aerial System) by small businesses via distribution centers.  A future operation model was envisioned based on factors such as drone velocity, flying altitude, number of drones, delivery demand and number of orders completed.

This project aims to refine the modeling approach using more sophisticated data and techniques to evaluate the impact of weather on a drone-based delivery system.  Orders will be sampled from population data representing the Greater Toronto Area (GTA) and weather conditions sampled from historical data sourced from Environment Canada.  Random adverse weather events will be modeled using historical wind gust data sourced from the German National Meteorological Service.  Different operating policies will be compared to evaluate the impact of weather conditions on a drone delivery system.  

Population data source from Canada census:

![image](https://user-images.githubusercontent.com/71515789/116816467-0a07df00-ab30-11eb-8a75-deaab3d756de.png)

Wind gust model, risk of wind gusts exceeding 50km/h for June 2020:

![image](https://user-images.githubusercontent.com/71515789/116816494-2572ea00-ab30-11eb-86bf-6be6c208bbbd.png)

Non-Stationary Poisson Process Thinning Algorithm Arrival Rates:

![image](https://user-images.githubusercontent.com/71515789/116816510-33c10600-ab30-11eb-926d-93e84e84630c.png)

System Response to Wind Speed:

![image](https://user-images.githubusercontent.com/71515789/116816528-463b3f80-ab30-11eb-8d6a-16221a942b3e.png)
![image](https://user-images.githubusercontent.com/71515789/116816537-4b988a00-ab30-11eb-8c05-a12b56fab638.png)
![image](https://user-images.githubusercontent.com/71515789/116816540-4fc4a780-ab30-11eb-9814-f9fae45a31d3.png)

Delivery Coordinates (blue) and Distribution Center (Red):

![image](https://user-images.githubusercontent.com/71515789/116816551-60751d80-ab30-11eb-8ba5-ae2320a1d48a.png)

Conclusions:
This simulation was designed to stay faithful to real world conditions.  To accomplish this the most accurate drone specifications, population data and historical weather data were leveraged.  The results suggest that the adverse effects of weather do not have a significant impact on the delivery output of drones over the course of a year.  Commercial drones with 80km/h top speeds are capable of handling wind gusts up to 50km/h and on any given day the risk of a wind gusts is so low that it is difficult to differentiate between a Naïve policy and a risk averse policy.  

Weather effects are notable in that they can force drones into emergency landings, and policies are required to mitigate these additional operating costs.  This study found that policies which leverage wind gust models and binomial probabilities can maintain delivery throughput while reducing lost drones by up to 40% under normal operating conditions.  Furthermore, when focusing exclusively on inclement weather conditions, the risk averse policies can improve system throughput by more than 10% while minimizing the number of lost drones by up to 60%.  

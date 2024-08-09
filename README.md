Vessel Proximity Detection

Aims

The aim of this project is to identify cases where one vessel approaches another in a marine area. This process, which is known as ‘vessel proximity’, employs vessels’ positions, timestamps and MMSI numbers.

Background

Marine vessels include container ships, cargo ships or passenger ships, all of which have one thing in common – they are assigned with a unique 9-digit number known as Maritime Mobile Service Identity (MMSI). For this project, the data supplied will be processed by us to recognize those instances where two different MMSIs come closer than a specific distance during a period of time.


Input Data

A CSV file is the input data with the following columns:

1.latitude: Where a ship is positioned.
2.longitude: Longitudes of the vessel’s position
3.timestamp: The time when this position was recorded.
4.mmsi: Maritime Mobile Service Identity number.

Task Overview

Develop an algorithm which detects all instances where two vessels (each having MMSI) come closer within a given period of time and reach a threshold distance. To determine the distance between two ships, use Haversine formula.

Enhancements:
1.Vectorization can be used for optimizing distance calculations.
2.Quadtree-based Approach: This will be considered as an approach for efficiently querying nearby vessels in future.


Approach
1. Haversine Formula
The Haversine formula is employed to calculate the great-circle distance between two points on the Earth's surface given their latitude and longitude.

2. Algorithm Development
Load the Data: Read the CSV file into a Pandas DataFrame.
Data Preprocessing: Convert the latitude and longitude to radians for the Haversine formula.
Distance Calculation: Calculate distances between vessels and identify proximity events.
Efficiency Enhancements: Vectorized operations are used to calculate distances for multiple vessels simultaneously.

3. Output
The output is a DataFrame containing:

mmsi: The MMSI of the vessel.
vessel_proximity: A list of MMSI numbers of vessels that came into proximity.
timestamp: The timestamp of the proximity event.

Installation
List of libraries are used in this project
. Pandas
. Numpy
. cKD Tree
. poltly


Conclusion
This project successfully identifies and records proximity events between vessels in a marine region using the Haversine formula for distance calculation. The approach leverages vectorization for efficient data processing, providing an effective solution for monitoring vessel interactions in real-time. Future enhancements, such as integrating spatial indexing with a Quadtree, could further optimize the algorithm's performance. This tool is valuable for maritime traffic management and safety monitoring, ensuring vessels operate at safe distances from one another.


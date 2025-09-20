# Analysis of a Sewing Line of a RMG Factory using Arena
This project presents a detailed simulation model of an assembly line in a Ready-Made Garment (RMG) factory, built using Rockwell Arena. The primary focus is to analyze the performance of operators and helpers, understand the associated costs, and propose alternative arrangements to improve the line's efficiency.

## 📝 Problem Statement
We are examining an assembly line that consists of 15 distinct processes, operated by a team of 6 operators and 6 helpers. The management wants to determine the performance of the operators and analyze the costs involved in the current setup. The simulation team is tasked with modeling this system to identify areas for improvement and suggest better alternatives.
The hourly costs for labor are as follows:
Operator: 100 Taka/hour
Helper: 70 Taka/hour

## 🎯 Project Objectives
Develop a Model: Construct a comprehensive simulation model for the assembly line system using Arena.
Simulate and Analyze: Run the simulation to visualize the workflow and analyze the system's operational dynamics.
Measure Performance: Evaluate the performance of operators and helpers using data gathered over a certain number of replications.
Propose Improvements: Suggest better, cost-effective alternative arrangements based on the simulation results.

## 📊 System Parameters & Distributions
The operational parameters, including inter-arrival times and process durations, are defined by the statistical distributions below.

### Table 1: Inter-arrival Time (seconds) and Labor Cost (Tk/hour)
Category
Distribution
Resource
Cost (Tk/hour)
Inter-arrival time
9 + 9 * BETA(0.989, 1.34)
Operator
50




Helper
30

### Table 2: Distribution of Process Time (seconds)
Process
Name
Helpers/Operators
Expression of Process Time
Process 1
Matching
Helper
9 + 9 * BETA(0.989, 1.34)
Process 2
Join Shoulder
Operator
TRIA(13, 16.3, 24)
Process 3
Rib Tack
Operator
5 + LOGN(1.53, 1.09)
Process 4
Neck join
Operator
10.1 + LOGN(1.94, 1.36)
Process 5
BK tape attach
Helper
9.26 + ERLA(0.962, 3)
Process 6
BK TS
Operator (2)
24 + 9 * BETA(1.09, 1.22)
Process 7
Front neck TS
Operator
9.26 + LOGN(3.13, 2.16)
Process 8
Sleeve shearing
Helper
3 + ERLA(1.64, 3)
Process 9
Sleeve cut
Helper
14 + GAMM(2.56, 1.49)
Process 10
Sleeve join
Operator (3)
34 + ERLA(2.71, 2)
Process 11
Side close
Operator (2)
25 + LOGN(3.1, 2.21)
Process 12
Sticker remove
Helper
8 + ERLA(2.01, 2)
Process 13
Body hem
Operator
UNIF(11.3, 16)
Process 14
Sleeve hem
Operator (2)
NORM(29.1, 1.66)
Process 15
Thread cut
Helper
NORM(35.8, 1.32)

## 🛠️ Model Details & System Logic
System Requirements: Windows OS and Rockwell Arena simulation software.
Entities: Fabric
Resource: Operator and Helper
Processes: 15 processes as listed in the table above.
Process Action: The core logic for all operations is Seize Delay Release.
Queue Discipline: All queues operate on a First-Come, First-Served (FCFS) basis.
Routing: The model uses 15 distinct routes to move entities between the 15 stations.

## 🚀 How to Run the Simulation
Ensure you have Rockwell Arena installed on a Windows operating system.
Clone this repository or download the .doe model file.
Open the model file in Arena.
Set the desired number of replications for the simulation run.
Execute the simulation to generate performance reports.
📈 Results & Analysis
The simulation output will provide detailed statistics on resource utilization (operators and helpers), process cycle times, throughput, and work-in-progress levels. This data will be instrumental in identifying bottlenecks, evaluating labor costs, and forming the basis for proposing more efficient and cost-effective operational strategies.

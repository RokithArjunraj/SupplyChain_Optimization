# Supply Chain Optimization using Linear and Integer Programming

## Overview
This project addresses key decision-making problems in supply chain logistics using Linear Programming (LP) and Integer Linear Programming (ILP). The objective is to optimize cost and service performance across carrier selection, warehouse operations, and delivery speed decisions.

The analysis is based on the Brunel Supply Chain Logistics Dataset and demonstrates how mathematical optimization can improve operational efficiency in a logistics network.

---

## Problem Statement

The project focuses on three core operational decisions:

1. Carrier Assignment  
   Determine the most cost-effective carrier for each shipment while maintaining service levels.

2. Plant (Warehouse) Selection  
   Identify which warehouses should remain operational to minimize costs while maintaining sufficient capacity.

3. Speed vs Cost Trade-off  
   Decide when to choose faster (more expensive) delivery over cheaper alternatives under service constraints.

---

## Dataset

The dataset contains over 9,000 historical shipment records and includes:

- Order details (origin, destination, weight, service level, delays)
- Carrier freight rates and transit times
- Warehouse costs and capacities
- Vendor-managed inventory (VMI) constraints
- Plant-to-port connectivity

Key tables:
- OrderList
- FreightRates
- WhCosts
- WhCapacities
- VmiCustomers
- PlantPorts
- ProductsPerPlant

---

## Methodology

### Carrier Assignment (LP)
- Objective: Minimize freight cost and delay penalties
- Constraints:
  - Each order must be assigned to one carrier
  - Carrier capacity share limited to 80%

---

### Plant Selection (Binary ILP)
- Objective: Minimize total operating cost
- Constraints:
  - At least 90% of total capacity must be retained
  - Certain plants must remain open due to contractual obligations

---

### Speed vs Cost Trade-off (Binary ILP)
- Objective: Minimize total shipping cost
- Constraint:
  - Maintain an average transit time below a defined threshold

---

## Results

Carrier Assignment:
- Improved delivery performance by reducing late shipments
- Balanced carrier utilization within constraints

Plant Selection:
- Identified three high-cost plants for closure
- Achieved significant cost savings while maintaining capacity

Speed vs Cost Trade-off:
- Demonstrated that most shipments can meet service requirements using lower-cost carriers
- Limited need for expedited shipping

---

## Key Insights

- High dependence on a single carrier introduces operational risk
- Cost inefficiencies are concentrated in a small number of high-cost plants
- Faster delivery options are not required for the majority of shipments

---

## Tech Stack

- Python
- Pandas
- NumPy
- SciPy (HiGHS Solver)

---

## Project Structure
--OBDA/Project/
        ├── OBDA_SCOptim_Grp8.ipynb
        ├── SupplyChainLogisticsProblems.xlsx

  

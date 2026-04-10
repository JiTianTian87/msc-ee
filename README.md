# Unleashing The Potential of Community IBRs' Remaining Capacity For Coordinated Optimal Power Quality Management

## Overview
This repository contains the dataset for the paper: **"Unleashing The Potential of Community IBRs' Remaining Capacity For Coordinated Optimal Power Quality Management in Distribution System"**. 

The dataset represents a modified 23-node distribution network based on an actual regional grid in Longgang District, Shenzhen, China. It is designed to validate the proposed sequence-domain network model and the coordinated optimization strategy for Voltage Unbalance Mitigation (VUM).

## System Description
The studied network is a three-phase unbalanced 23-node distribution system. The main grid is modeled as an infinite bus (Bus 0) that acts as the source of voltage unbalance. Multiple Inverter-Based Resources (IBRs) are distributed across the network. 

**Key Base Values (for p.u. conversion):**
* Base Power ($S_{base}$): 2.5 MVA
* Base Voltage ($V_{base}/V_{LL,rms}$): 10 kV
* System Frequency: 50 Hz

## Repository Structure
* `/data`: Contains all network topologies, impedance matrices, load profiles, and IBR constraints in `.csv` and `.mat` formats.
  * `branch_data.csv`: Feeder topology and line impedance ($R/X = 0.66$).
  * `bus_data.csv`: Conventional load distribution.
  * `ibr_params.csv`: Specific constraints for each IBR, including apparent power ($\overline{S}_s$), phase current limits ($\overline{I}_s$), and active power bounds ($\underline{P}_s$).
  * `scenarios_config.csv`: Voltage unbalance settings for Bus 0 (Case 1: Moderate VU, Case 2: Severe VU).
* `/src`: *(Optional: If you upload MATLAB code, describe it here)* Contains the optimization scripts implemented in MATLAB using [YALMIP / CVX] and solved by [Gurobi / Mosek].

## Optimization Model Highlights
The provided data enables the reproduction of the following models from the paper:
1. **Sequence-Domain Power Flow**: Utilizing dual common synchronous rotating reference frames ($DQ^+$ and $DQ^-$).
2. **Coupled Capacity Constraints**: Jointly visualizing current limits, sequence voltage limits, and apparent power limits via polyhedral approximations ($n=16$).
3. **Coordinated Allocation**: Solving the quadratic objective function to balance positive- and negative-sequence capacities.

## Citation
If you find this dataset or code useful for your research, please cite our paper:

```bibtex
@article{Ji2026Unleashing,
  title={Unleashing The Potential of Community IBRs' Remaining Capacity For Coordinated Optimal Power Quality Management in Distribution System},
  author={Ji, Tiantian and Lin, Pengfeng and Zhu, Miao},
  journal={IEEE Transactions on [Journal Name]},
  year={2026},
  volume={[XX]},
  number={[XX]},
  pages={[XX-XX]}
}

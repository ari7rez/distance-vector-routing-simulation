# Distance Vector Routing Simulation

## Overview
This project implements the Distance Vector routing algorithm to simulate how routers exchange information and compute shortest paths in a network.

## Features
- Distance Vector routing implementation
- Dynamic topology updates
- Convergence detection
- Loop prevention using Poisoned Reverse
- Routing table generation and updates

## Tech Stack
- Python

## How It Works
Each node maintains a routing table and exchanges distance vectors with its neighbours. The algorithm iteratively updates routes until convergence is reached.

## Example
Input:
- Network topology with weighted links
- Dynamic updates such as link changes or removals

Output:
- Distance tables
- Final routing tables

## My Contribution
- Implemented the core Distance Vector algorithm
- Designed routing and distance table structures
- Implemented convergence detection
- Added Poisoned Reverse support
- Built and ran multiple test cases for validation

## Project Context
This project was originally developed as part of a university networking course and is presented here as a portfolio project.

## Repository Structure
- `DistanceVector` – core Distance Vector algorithm
- `PoisonedReverse` – Distance Vector with loop prevention
- `test_*.txt` – test cases
- `sample_input.txt` – sample input scenario

## How to Run
```bash
chmod +x DistanceVector
./DistanceVector < test_input.txt
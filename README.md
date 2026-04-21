# SDN-Multi-Switch-Flow-Analyzer

## Problem Statement
This project implements an SDN-based solution using Mininet and Ryu controller to demonstrate controller-switch interaction, dynamic flow rule installation, and flow table monitoring.

## Topology
Linear topology with 2 switches and 2 hosts:

h1 -- s1 -- s2 -- h2

## Tools Used
- Ubuntu
- Mininet
- Ryu Controller
- Python
- iperf

## How to Run

### Start Controller
ryu-manager flow_analyzer.py

### Start Mininet
sudo mn --topo linear,2 --controller remote

### Test Connectivity
h1 ping h2

### Throughput Test
iperf h1 h2

## Features
- Multi-switch SDN topology
- Dynamic flow rule installation
- packet_in handling
- Active vs unused flow detection
- Periodic flow monitoring

## Test Scenarios

### Scenario 1: Normal Communication
h1 ping h2 successful.

### Scenario 2: Failure Scenario
link s1 s2 down

Ping fails.

## Validation / Regression Testing

| Test Case | Result |
|----------|--------|
| Controller starts | Pass |
| Switch connects | Pass |
| Ping works | Pass |
| Flow monitoring works | Pass |

## Expected Output
- Successful ping between hosts
- ACTIVE FLOW logs in controller
- Throughput using iperf

## Screenshots
See screenshots folder.

## References
- Ryu Documentation
- Mininet Documentation
- OpenFlow Specification

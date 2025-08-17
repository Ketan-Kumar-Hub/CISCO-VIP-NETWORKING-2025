CISCO-VIP-NETWORKING-2025
🚀 Auto Topology Generation & Network Simulation Tool

Cisco Virtual Internship Program 2025 – Networking Track

This project provides a complete solution to:

Parse router/switch configuration files

Automatically generate a hierarchical network topology

Validate network setups & optimize them

Run Day-1 & Day-2 simulations including fault injection

📌 Overview

Currently, no automated solution exists to generate a full topology from individual router configs.
This tool builds such a topology, validates configurations, and tests real-world scenarios like link failures and load balancing.

🔑 Key Features

Auto Topology Generation

Reads configs of routers & switches

Extracts IPs, VLANs, gateways, protocols (OSPF/BGP), MTU etc.

Builds a hierarchical graph of the network

Configuration Validation

Detects:

Missing switch configs

Duplicate IPs

Wrong VLAN labels

Incorrect gateway addresses

MTU mismatches & loops

Suggests optimizations (e.g., use BGP instead of OSPF)

Load Management

Checks bandwidth vs traffic load

Flags overloaded links

Recommends load balancing / alternate paths

Simulation & Fault Injection

Day-1: ARP, neighbor discovery, OSPF discovery

Day-2: Link failure simulation & recovery tests

Pause & Resume simulation feature

Implementation Architecture

Multithreaded (routers & switches as threads)

IPC via FIFO / TCP sockets for metadata packets

Node-level statistics & logs maintained

📂 Repository Structure
CISCO-VIP-NETWORKING-2025/
├── Config/                 # Input config files (e.g., R1.txt, S1.txt)
├── topology_generator/     # Code for topology parsing & building
├── validation_module/      # Config validation & optimization
├── simulation_engine/      # Day-1 & Day-2 simulation logic
├── reports/                # Generated outputs (logs, reports, graphs)
├── main.py                 # Entry point of the tool
├── requirements.txt        # Python dependencies
└── README.md               # Documentation (this file)

⚙️ Installation
# Clone this repository
git clone https://github.com/Ketan-Kumar-Hub/CISCO-VIP-NETWORKING-2025.git
cd CISCO-VIP-NETWORKING-2025

# Install dependencies
pip install -r requirements.txt


✅ Requires Python 3.9+

▶️ Usage

Place your router/switch configs inside Config/ folder

Generate Topology

python main.py --generate-topology


Validate Configurations

python main.py --validate-config


Run Simulations

Day-1:

python main.py --simulate --day 1


Day-2 (Fault Injection):

python main.py --simulate --day 2


Pause/Resume Simulation

python main.py --pause
python main.py --resume

📊 Example Outputs

Interactive HTML topology diagram

Validation report (issues + suggestions)

Simulation logs (Day-1 & Day-2)

Fault injection results with recovery details

✅ Cisco Internship Requirements Covered

Hierarchical topology generation

Bandwidth & load validation

Load balancing recommendations

Missing component detection

Duplicate IPs / VLAN / gateway issue detection

MTU mismatch & loop detection

Routing protocol recommendations (BGP vs OSPF)

Day-1 & Day-2 simulation with fault injection

Pause/Resume capability

Multithreaded + IPC-based architecture

👨‍💻 Author

Ketan Kumar Vishwakarma
(Cisco Virtual Internship Program 2025 – Networking Stream)

📜 License

This project is under the MIT License – feel free to use & improve.

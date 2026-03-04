# 🏭 Digital Twin Supply Chain

> **Agent-Based Simulation Framework for Supply Chain Network Modeling & Optimization**
> > Part of the [Quantisage SAGE Platform](https://github.com/virbahu) ecosystem
> >
> > [![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://python.org)
> > [![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
> > [![SimPy](https://img.shields.io/badge/SimPy-4.0+-orange.svg)](https://simpy.readthedocs.io)
> >
> > ---
> >
> > ## 🎯 Overview
> >
> > The **Digital Twin Supply Chain** framework provides a comprehensive simulation environment for modeling end-to-end supply chain networks. Using agent-based modeling, discrete-event simulation, and real-time data integration, it enables organizations to test disruption scenarios, optimize network design, evaluate decarbonization strategies, and achieve real-time operational visibility across complex, multi-tier supply chains.
> >
> > ### Simulation Capabilities
> >
> > | Capability | Description |
> > |-----------|-------------|
> > | **Network Modeling** | Multi-tier supply chain network topology with configurable nodes and edges |
> > | **Disruption Simulation** | Natural disaster, geopolitical, pandemic, and supplier failure scenarios |
> > | **What-If Optimization** | Test alternative sourcing, routing, and inventory strategies |
> > | **Carbon Simulation** | Model emissions impact of supply chain configuration changes |
> > | **Demand Scenarios** | Simulate demand volatility, seasonality, and bullwhip effects |
> > | **Cost Modeling** | Total cost simulation including logistics, inventory, and tariffs |
> > | **Real-Time Mirroring** | Live digital twin with real-time ERP/IoT data feeds |
> >
> > ---
> >
> > ## 🏗️ Architecture
> >
> > ```
> > digital-twin-supply-chain/
> > ├── src/
> > │   ├── simulation/
> > │   │   ├── __init__.py
> > │   │   ├── engine.py                # Core simulation engine
> > │   │   ├── discrete_event.py        # Discrete-event simulation (SimPy)
> > │   │   ├── agent_based.py           # Agent-based modeling framework
> > │   │   ├── monte_carlo.py           # Monte Carlo simulation
> > │   │   └── time_stepper.py          # Time-step simulation controller
> > │   ├── models/
> > │   │   ├── __init__.py
> > │   │   ├── network.py               # Supply chain network graph model
> > │   │   ├── agents/
> > │   │   │   ├── supplier.py          # Supplier agent
> > │   │   │   ├── manufacturer.py      # Manufacturing facility agent
> > │   │   │   ├── warehouse.py         # Warehouse/DC agent
> > │   │   │   ├── transporter.py       # Logistics/transport agent
> > │   │   │   └── customer.py          # Customer demand agent
> > │   │   ├── flows/
> > │   │   │   ├── material_flow.py     # Material flow model
> > │   │   │   ├── information_flow.py  # Information flow model
> > │   │   │   └── financial_flow.py    # Financial flow model
> > │   │   └── environment/
> > │   │       ├── market.py            # Market conditions model
> > │   │       ├── disruptions.py       # Disruption event generator
> > │   │       └── regulations.py       # Regulatory environment model
> > │   ├── scenarios/
> > │   │   ├── __init__.py
> > │   │   ├── disruption_lib.py        # Pre-built disruption scenarios
> > │   │   ├── demand_scenarios.py      # Demand scenario generator
> > │   │   ├── carbon_scenarios.py      # Carbon reduction scenarios
> > │   │   ├── network_redesign.py      # Network redesign scenarios
> > │   │   └── scenario_builder.py      # Custom scenario builder
> > │   ├── optimization/
> > │   │   ├── __init__.py
> > │   │   ├── network_optimizer.py     # Network design optimization
> > │   │   ├── inventory_policy.py      # Inventory policy optimization
> > │   │   ├── routing_optimizer.py     # Transportation routing optimization
> > │   │   └── multi_objective.py       # Multi-objective optimization
> > │   ├── analytics/
> > │   │   ├── __init__.py
> > │   │   ├── kpi_tracker.py           # KPI calculation & tracking
> > │   │   ├── sensitivity.py           # Sensitivity analysis
> > │   │   ├── comparison.py            # Scenario comparison engine
> > │   │   └── reporting.py             # Simulation report generator
> > │   ├── visualization/
> > │   │   ├── __init__.py
> > │   │   ├── network_viz.py           # Network topology visualization
> > │   │   ├── animation.py             # Simulation animation
> > │   │   ├── dashboard.py             # Real-time simulation dashboard
> > │   │   └── geo_mapper.py            # Geographic network mapping
> > │   └── api/
> > │       ├── __init__.py
> > │       ├── main.py                  # FastAPI application
> > │       └── routes/
> > │           ├── simulations.py       # Simulation management endpoints
> > │           ├── scenarios.py         # Scenario endpoints
> > │           ├── analytics.py         # Analytics endpoints
> > │           └── realtime.py          # Real-time twin endpoints
> > ├── tests/
> > │   ├── test_simulation/
> > │   ├── test_models/
> > │   ├── test_scenarios/
> > │   └── test_optimization/
> > ├── examples/
> > │   ├── basic_network.py
> > │   ├── disruption_analysis.py
> > │   └── carbon_optimization.py
> > ├── config/
> > │   ├── simulation.yaml
> > │   ├── scenarios/
> > │   └── network_templates/
> > ├── requirements.txt
> > ├── Dockerfile
> > └── README.md
> > ```
> >
> > ---
> >
> > ## 🚀 Key Features
> >
> > ### 1. Agent-Based Supply Chain Modeling
> > Model individual supply chain entities (suppliers, factories, warehouses, transporters) as autonomous agents with configurable behaviors and decision rules.
> >
> > ### 2. Disruption Scenario Analysis
> > Pre-built and custom disruption scenarios including natural disasters, supplier bankruptcies, port closures, and pandemic impacts with cascading effect modeling.
> >
> > ### 3. Carbon Impact Simulation
> > Model the emissions impact of supply chain design changes, supplier switches, and transportation mode shifts for decarbonization planning.
> >
> > ### 4. Network Design Optimization
> > Optimize facility locations, supplier allocation, transportation routes, and inventory positioning using multi-objective optimization algorithms.
> >
> > ### 5. Real-Time Digital Twin
> > Live mirroring of actual supply chain operations with real-time ERP and IoT data integration for operational visibility and anomaly detection.
> >
> > ### 6. Interactive Visualization
> > Dynamic network visualization with simulation animation, geographic mapping, and interactive dashboards for scenario exploration.
> >
> > ---
> >
> > ## ⚡ Quick Start
> >
> > ```bash
> > # Clone the repository
> > git clone https://github.com/virbahu/digital-twin-supply-chain.git
> > cd digital-twin-supply-chain
> >
> > # Create virtual environment
> > python -m venv venv
> > source venv/bin/activate
> >
> > # Install dependencies
> > pip install -r requirements.txt
> >
> > # Run example simulation
> > python examples/basic_network.py
> >
> > # Run the API server
> > uvicorn src.api.main:app --reload --port 8004
> > ```
> >
> > ---
> >
> > ## 🔗 SAGE Platform Integration
> >
> > - **[supply-chain-knowledge-graph](https://github.com/virbahu/supply-chain-knowledge-graph)** — Network topology data source
> > - - **[erp-integration-connectors](https://github.com/virbahu/erp-integration-connectors)** — Real-time ERP data feeds
> >   - - **[carbon-data-pipeline](https://github.com/virbahu/carbon-data-pipeline)** — IoT data for live twin
> >     - - **[scope3-gnn-mapper](https://github.com/virbahu/scope3-gnn-mapper)** — Emissions modeling data
> >       - - **[inventory-optimization](https://github.com/virbahu/inventory-optimization)** — Inventory policy inputs
> >         - - **[demand-forecasting-engine](https://github.com/virbahu/demand-forecasting-engine)** — Demand scenario inputs
> >          
> >           - ---
> >
> > ## 🛠️ Tech Stack
> >
> > - **Simulation:** SimPy, Mesa (ABM), NumPy, SciPy
> > - - **Optimization:** PuLP, DEAP, Optuna
> >   - - **Visualization:** Plotly, NetworkX, Folium, Dash
> >     - - **Backend:** Python 3.10+, FastAPI
> >       - - **Real-Time:** Apache Kafka, WebSockets
> >         - - **Database:** PostgreSQL, Neo4j (network graph)
> >           - - **Containerization:** Docker, Kubernetes
> >            
> >             - ---
> >
> > ## 📧 Contact
> >
> > **Quantisage** — *Where Growth Meets Compliance*
> > - Email: info@quantisage.com
> > - - Founder: [Vir Bahu](https://github.com/virbahu) — vir@quantisage.com
> >  
> >   - ## 📄 License
> >  
> >   - This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

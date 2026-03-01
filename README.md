PlantControllerSim – Manufacturing Finance Close Simulation
Executive Summary

PlantControllerSim is a simulated manufacturing finance environment designed to replicate a full monthly plant close process.

The project integrates SQL based transaction logic with a Power BI semantic model to produce controller grade outputs including:

Standard cost validation

Manufacturing variance analysis

Inventory bridge reconciliation

Working capital simulation

Fixed asset and warranty rollforward

Controller commentary framework

The objective is to demonstrate structured financial data modeling, reconciliation discipline, and analytics system design.

Business Context

Manufacturing plants require alignment between operational activity and financial reporting.

This simulation models:

Production activity

Material consumption

Labor and overhead absorption

Inventory movements

Accounts receivable and payable

Period close reconciliation

The system ensures that operational drivers reconcile to financial outputs.

Architecture Overview

Operational transactions
→ SQL transformation layer
→ Dimensional data model
→ Close calculation views
→ Power BI semantic model
→ Reporting artifacts

Detailed architecture diagrams are available in the docs folder.

Repository Structure

docs
Architecture diagrams and close process flows

sql
Schema definitions, transformation logic, variance calculations

semantic-layer
Measure documentation and model structure

images
Reporting screenshots

playbook
Monthly close documentation and control framework

Key Capabilities Demonstrated

Dimensional modeling discipline

Standard cost integrity validation

Manufacturing variance decomposition

Inventory reconciliation logic

Working capital modeling

Close control framework design

Power BI semantic layer structuring

Data and Confidentiality

This repository contains simulation logic only.
No real company data is included.

Roadmap

Add architecture diagrams

Document variance formulas explicitly

Add semantic model relationship map

Add controller commentary template
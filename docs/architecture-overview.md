Architecture Overview – PlantControllerSim
Objective

Simulate a full manufacturing plant monthly close process with structured reconciliation between operational activity and financial reporting.

System Layers
1. Operational Transaction Layer

Simulated operational inputs include:

Production orders

Material issues

Labor activity

Overhead allocation

Inventory movements

Receivables and payables

These represent the operational drivers of financial outcomes.

2. SQL Transformation Layer

SQL Server is used to:

Define schema and dimensional structures

Calculate standard cost integrity

Compute manufacturing variances

Build close reconciliation views

Simulate working capital movements

All logic is reproducible and structured through database objects.

3. Dimensional Model

Core modeling principles:

Fact and dimension separation

Controlled grain definition

Single direction filtering in semantic layer

Reconciliation capable structure

Example key objects:

factProduction

factMaterialPurchase

factLaborActual

factReceivable

factPayable

dimDate

dimItem

dimLocation

4. Close Calculation Views

Close logic is abstracted into SQL views such as:

v_Close_Jan_TotalVariances

v_Close_Jan_WorkingCapital

v_Close_Jan_InvBridge

v_Close_Jan_EBIT

These simulate a structured monthly close framework.

5. Semantic Layer

Power BI consumes curated close views.

Design principles:

Measures centralized

Controlled relationships

Clean star schema

Reconciliation against SQL layer

6. Reporting Layer

Controller grade outputs include:

Manufacturing P&L

Variance waterfall

Inventory bridge

Working capital dashboard

Fixed asset rollforward

Warranty rollforward

Control monitoring page

Design Philosophy

PlantControllerSim is built to emphasize:

Reconciliation discipline

Auditability

Structured transformation

Transferability to real enterprise finance environments
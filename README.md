
# Contract-Renewal-Notice


## Project Overview

The **Contract Renewal Notice** project is developed using the **SAP ABAP RESTful Application Programming Model (RAP)**.

The application is designed to manage contract information, maintain supplier contract details, monitor contract expiry dates, identify contracts that require renewal, and support the preparation of contract renewal notices.

The project follows the RAP architecture using CDS Views, Behavior Definitions, Projection Views, Service Definition, Service Binding, OData V4, and Fiori Elements.


## Project Objectives

- Maintain contract information in SAP.
- Manage contract creation, update, and deletion.
- Display contract information through Fiori Elements.
- Track contract start and end dates.
- Identify contracts approaching expiry.
- Maintain the renewal-required status.
- Support the Contract Renewal Notice process.
- Provide a simple Fiori-based user interface for contract management.


## Technology Used

- SAP ABAP
- SAP RAP
- CDS Views
- Behavior Definition
- Behavior Pool
- Projection CDS View
- Projection Behavior
- Service Definition
- Service Binding
- OData V4
- Fiori Elements
- Eclipse ADT

## Project Objects

| Object | Purpose |
|---|---|
| **ZCONTRACT_RENEWAL** | Development Package |
| **ZCONTRACT_HDR** | Database Table |
| **ZCONTRACT_I_RENEWAL** | CDS Root View Entity |
| **ZBP_I_CONTRACT_RENEWAL** | Behavior Pool |
| **ZCONTRACT_C_RENEWAL** | Projection CDS View |
| **ZCONTRACT_UI_RENEWAL** | Service Definition |
| **ZCONTRACT_UI_RENEWAL_O4** | OData V4 Service Binding |

# Project Workflow

The complete project follows this flow:


Package
   ↓
Database Table
   ↓
CDS Root View
   ↓
Behavior Definition
   ↓
Behavior Pool
   ↓
Projection CDS View
   ↓
Projection Behavior
   ↓
Service Definition
   ↓
Service Binding
   ↓
OData V4
   ↓
Fiori Elements
   ↓
Create Contract
   ↓
Verify Contract
   ↓
Check Contract Expiry
   ↓
Update Renewal Status
   ↓
Contract Renewal Notice



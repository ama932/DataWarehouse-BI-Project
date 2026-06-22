# DataWarehouse-BI-Project

# Cinema Hall Ticket Sales & Customer Behavior Analytics

This project implements a complete Data Warehousing and Business Intelligence (DWBI) solution for analyzing cinema ticket sales and customer behavior. The solution was developed using Microsoft SQL Server technologies and follows a dimensional modeling approach to support analytical reporting and decision-making.

The project covers the full BI lifecycle including:

* Data preparation and integration
* ETL development using SSIS
* Star schema data warehouse design
* Slowly Changing Dimension (SCD Type 2) implementation
* Accumulating Fact Table implementation
* SSAS Multidimensional Cube development
* OLAP analysis using Excel
* Interactive dashboards using Power BI
* Publishing reports to Power BI Service


## Business Scenario

The system analyzes cinema ticket booking operations including:

* Customer information
* Movie details
* Cinema hall information
* Seat allocation
* Ticket sales transactions
* Booking dates and processing times

The solution enables analysis of:

* Sales performance
* Customer behavior
* Movie popularity
* Hall utilization
* Ticket demand trends
* Transaction processing efficiency


## Dataset

Source Dataset:

Cinema Hall Ticket Sales and Customer Behavior Dataset

Dataset includes:

* Customers
* Movies
* Halls
* Seats
* Ticket Transactions

The source data was transformed from an OLTP structure into a dimensional data warehouse for analytical processing.


## Solution Architecture

Data Sources (CSV Files + SQL Server)
            │
            
      SSIS ETL Process
            │
            
   SQL Server Data Warehouse
            │
            
       SSAS Cube
            │
      ┌─────┴─────┐
                 
 Excel OLAP    Power BI
      |           |            
 Business Analytics & Reporting



## Data Warehouse Design

### Star Schema

Fact Table:

* Fact_Ticket_Sales

Dimension Tables:

* Dim_Customer
* Dim_Movie
* Dim_Hall
* Dim_Seat
* Dim_Date

### Fact Table Measures

* Total Sales Amount
* Ticket Quantity
* Transaction Count
* Process Time Hours

### Grain

Each fact record represents a single cinema ticket transaction associated with:

* Customer
* Movie
* Hall
* Seat
* Booking Date


## ETL Development (SSIS)

The ETL solution was implemented using SQL Server Integration Services (SSIS).

### Dimension Loading

* Load_Dim_Customer
* Load_Dim_Movie
* Load_Dim_Hall
* Load_Dim_Seat
* Load_Dim_Date

### Fact Loading

* Load_Fact_Ticket_Sales

### Transformations Used

* Data Conversion
* Derived Columns
* Lookup Transformations
* OLE DB Destinations
* OLE DB Commands

### Surrogate Key Lookups

* Customer Key
* Movie Key
* Hall Key
* Seat Key


## Slowly Changing Dimension (SCD Type 2)

The Customer Dimension was implemented as an SCD Type 2.

Features:

* Historical tracking of customer changes
* Start Date
* End Date
* Current Record Indicator

This allows the warehouse to preserve historical customer information rather than overwriting existing records.


## Accumulating Fact Table

An additional ETL process was implemented to simulate real-world transaction completion tracking.

Updates include:

* Transaction Completion Time
* Transaction Processing Duration

This demonstrates accumulating fact table behavior commonly used in enterprise data warehouses.


## SSAS Cube Development

A Multidimensional Cube was developed using SQL Server Analysis Services (SSAS).

### Dimensions

* Customer
* Movie
* Hall
* Seat
* Date

### Measures

* Total Sales
* Total Tickets
* Transaction Count
* Process Time Hours

### Hierarchies

Date Hierarchy:

Year → Month → Full Date

### Cube Capabilities

* Drill Down
* Roll Up
* Slice
* Dice
* Pivot Analysis


## Excel OLAP Analysis

The SSAS Cube was connected to Microsoft Excel using Analysis Services.

OLAP operations demonstrated:

### Roll-Up

Analyze Total Sales at summarized yearly levels.

### Drill-Down

Navigate from Year to Month to Full Date.

### Slice

Filter analysis by a single dimension value.

### Dice

Filter analysis using multiple dimensions.

### Pivot

View data from multiple analytical perspectives.


## Power BI Dashboards

The warehouse was connected to Power BI Desktop using SQL Server Import Mode.

### DAX Measures

* Total Sales
* Total Tickets
* Transaction Count
* Average Process Time

### Report 1 – Matrix Report

* Movie Genre
* Movie Name
* Year
* Month
* Total Sales
* Total Tickets

### Report 2 – Cascading Slicers

* Location Filter
* Hall Filter
* Dynamic KPI Visualizations

### Report 3 – Drill-Down Analysis

* Year Level
* Month Level
* Date Level

### Report 4 – Drill-Through Analysis

Detailed movie-level reporting with:

* Cards
* Charts
* Tables
* Navigation Controls


## Power BI Service

The completed Power BI solution was published to Power BI Service for cloud-based access and reporting.

Features:

* Online report access
* Interactive dashboards
* Cloud deployment
* Business reporting


## Technologies Used

* Microsoft SQL Server
* SQL Server Integration Services (SSIS)
* SQL Server Analysis Services (SSAS)
* SQL Server Management Studio (SSMS)
* Visual Studio
* Power BI Desktop
* Power BI Service
* Microsoft Excel
* SQL



## Key Skills Demonstrated

* Data Warehousing
* ETL Development
* Data Modeling
* Dimensional Modeling
* Star Schema Design
* Slowly Changing Dimensions (SCD)
* Accumulating Fact Tables
* OLAP Analysis
* SSAS Cube Development
* Power BI Reporting
* SQL Development
* Business Intelligence


## Author

**IT23621060**

Data Warehousing & Business Intelligence Project

GitHub: https: https://github.com/ama932/DataWarehouse-BI-Project/

LinkedIn: https://www.linkedin.com/in/amavi-dodanwela/

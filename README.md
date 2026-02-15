# NBA Fantasy Draft Tool - PowerBI

### Dashboard Link :[https://app.powerbi.com/view?r=eyJrIjoiZTUyZmRmMDktYmU5OC00YWJmLWIxZmMtOGE5ZDFjNTI1NDUzIiwidCI6ImI1MmJlNDcxLWY3ZjEtNDdiNC1hODc5LTBjNzk5YmI1M2RiNSIsImMiOjZ9&pageName=ReportSection33f1e9a18d0687ee0e36](https://app.powerbi.com/view?r=eyJrIjoiNzVjODhlN2EtOGM3Ny00ZmNmLWJmZTktYWZiZDRjYTk0OGQ5IiwidCI6IjgzYWVlZjdjLWMzMTAtNDdmNS04ZDRjLWVkZjRiYTEzZThhNSIsImMiOjZ9&pageName=02b384dc791af01ae05e)


San Diego Relocation Intelligence Dashboard
Overview

This project analyzes relocation suitability across cities in San Diego County using rental market data, crime statistics, and business density.

The goal is to provide a data-driven framework for evaluating where to live based on affordability, safety, and access to amenities. The final output is an interactive Power BI dashboard supported by a structured SQL and Power Query data pipeline.

Objectives

Identify high-value cities for relocation

Quantify trade-offs between rent, safety, and amenities

Build a composite relocation score

Demonstrate end-to-end analytics workflow for portfolio use

Data Sources

Rental Data

Source: RentCast API

Scope: 2-bedroom rental listings within a 70-mile radius of San Diego

Method: API pagination to exceed the 500-row response limit

Crime Data

Source: San Diego Police Department Open Data

Process: cleaned offense categories, filtered by year, calculated crime rate per 100,000 residents

Business Data

Source: Public business listings dataset

Use: business counts by category and city to estimate amenity density

Data Processing Workflow

Extract rental data via REST API with pagination

Import crime and business datasets from CSV

Stage and transform data in SQL Server

Clean and shape data using Power Query

Build relationships and calculated measures in Power BI

Create normalized scoring model for city ranking

Scoring Model

Each city receives a composite Relocation Score based on:

Affordability Score – median rent relative to county baseline

Safety Score – crime rate per 100,000 residents

Amenity Score – business density and category coverage

Scores are normalized and combined using weighted aggregation to rank cities.

Key Findings

Spring Valley offers the strongest affordability with acceptable safety levels

The City of San Diego provides the highest amenity density at a higher cost

Escondido presents a balanced option across all three factors

These results illustrate the trade-offs between cost, safety, and convenience when relocating.

Dashboard Features

City ranking matrix with composite score

Crime trend analysis with year filtering

Rental price distribution by location

Business category density visuals

KPI indicators for affordability, safety, and amenities

Cross-filtering across all report elements

Tools and Technologies

Power BI

SQL Server / SSMS

Power Query

DAX

REST API (RentCast)

Project Structure
/data
  rentals_raw.csv
  crime_raw.csv
  business_raw.csv

/sql
  staging_queries.sql
  transformation_views.sql

/powerbi
  san_diego_relocation.pbix

/docs
  methodology.md
  data_sources.md

Use Case

This project is designed for:

Data analytics portfolio demonstration

Relocation decision support

Comparative city analysis

Future Improvements

Commute time and transportation scoring

Salary-to-rent affordability ratios

Time-series rent forecasting

Power BI Service deployment

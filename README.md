# San Diego Relocation Intelligence Dashboard

### Dashboard Link :[https://app.powerbi.com/view?r=eyJrIjoiZTUyZmRmMDktYmU5OC00YWJmLWIxZmMtOGE5ZDFjNTI1NDUzIiwidCI6ImI1MmJlNDcxLWY3ZjEtNDdiNC1hODc5LTBjNzk5YmI1M2RiNSIsImMiOjZ9&pageName=ReportSection33f1e9a18d0687ee0e36](https://app.powerbi.com/view?r=eyJrIjoiNzVjODhlN2EtOGM3Ny00ZmNmLWJmZTktYWZiZDRjYTk0OGQ5IiwidCI6IjgzYWVlZjdjLWMzMTAtNDdmNS04ZDRjLWVkZjRiYTEzZThhNSIsImMiOjZ9&pageName=02b384dc791af01ae05e)



## Overview

This project is a relocation analysis I built to answer a simple question:

Where are the best places to live in San Diego County when you factor in rent, safety, and access to amenities?

Instead of relying on opinions, I pulled real data from an API and public sources, built a scoring model, and delivered the results in Power BI.

This is an end-to-end analytics project that covers data ingestion, cleaning, modeling, DAX, and dashboard design.

## What This Project Shows

As a 3rd year data analyst, I wanted this project to reflect how I approach real problems:

- Work with messy, real-world datasets

- Pull data from APIs and flat files

- Build a structured SQL staging layer

- Create normalized metrics instead of raw counts

- Turn analysis into a decision-making tool

The output is a ranked view of cities based on overall relocation value.

## Data Sources

### Rental Data

Source: RentCast API

Pulled 2-bedroom listings within a 70-mile radius of San Diego

Implemented pagination to get past the 500-row limit

Used to calculate median rent and affordability scores

### Crime Data

Source: San Diego Police Department Open Data

Cleaned and filtered to last 5 years for accurate rates

Used as the safety component of the model

### Business / Amenities

Source: Public business listings dataset

Aggregated by category and city

## Data Workflow

Extract rental data via REST API (paginated requests)

Import crime and business datasets from CSV

Stage and transform data in SQL Server

Clean and shape data in Power Query

Build relationships and measures in Power BI

Normalize metrics and create a weighted relocation score

## Scoring Model

Each city gets a Relocation Score based on three normalized components:

Affordability → Median rent by city
Safety → Crime rate by severity

Amenities → Business density and category coverage

These are weighted and combined to rank cities based on overall livability.

## Key Takeaways

Spring Valley stands out for affordability while staying within acceptable safety levels

The City of San Diego has the highest amenity density but also the highest rent

Escondido offers the most balanced profile across all three factors

The main insight is the trade-off between cost, safety, and convenience.

## Dashboard Features

Ranked city comparison using a composite score

Crime trend analysis with time filtering

Rental price distribution by city

Business density by category

KPI cards for each scoring component

Cross-filtering across all visuals

## Tools Used

Power BI

SQL Server / SSMS

Power Query

REST API (RentCast)

## Why I Built This

I’m currently a 3rd year data analyst, and this project was designed to reflect the kind of work I do in real environments:

- Pulling data from multiple sources

- Cleaning and modeling it properly

- Building metrics that actually mean something

- Delivering a dashboard that supports a real decision

In this case, the decision is where to live in San Diego based on data, not guesswork.

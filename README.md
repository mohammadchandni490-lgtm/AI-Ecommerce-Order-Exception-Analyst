# AI-Powered E-commerce Order Exception Analyst

## Overview

This project demonstrates an AI-assisted e-commerce operations workflow designed to identify, prioritise and analyse fulfilment exceptions.

A synthetic dataset of 500 orders was created and analysed using Python. The workflow automatically detects operational issues such as:

* Late dispatches
* Missing tracking information
* Stuck orders
* Missing invoices
* Quantity mismatches

The project then prioritises affected orders, recommends operational actions and analyses patterns across warehouses, sellers and carriers.

## Business Problem

E-commerce fulfilment teams often need to monitor large volumes of orders across multiple systems. Orders can become delayed, mismatched or incomplete, creating additional manual checking and customer-service workload.

This project explores how Python-based automation can reduce repetitive operational checks and surface the orders that require attention first.

## Features

The workflow:

* Generates and processes synthetic e-commerce order data
* Detects five types of operational exception
* Identifies orders with multiple simultaneous issues
* Assigns operational priority levels
* Generates recommended actions
* Creates a daily exception queue
* Calculates the overall exception rate
* Analyses warehouse performance
* Analyses seller performance
* Analyses carrier performance
* Compares high-priority rates with overall exception volume
* Identifies warehouse-carrier combinations associated with higher-priority exceptions
* Produces structured operational data suitable for AI-assisted reporting

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Google Colab
* Generative AI / Claude workflow concept

## Example Results

From the synthetic dataset of 500 orders:

* 111 orders required operational attention
* Overall exception rate: 22.2%
* 44 orders were classified as high priority
* 67 orders were classified as medium priority
* 14 orders had more than one exception type
* Late Dispatch was the most common exception

The analysis also demonstrated how exception volume and severity can differ across warehouses, sellers and carriers.

## Exception Types

### Late Dispatch

Identifies orders that were dispatched after their expected dispatch date.

### Missing Tracking

Identifies shipped or delivered orders without tracking information.

### Stuck Order

Identifies processing orders whose expected dispatch date has already passed.

### Quantity Mismatch

Identifies orders where the expected quantity differs from the shipped quantity.

### Missing Invoice

Identifies delivered orders where an invoice has not been generated.

## Priority Logic

Orders are assigned priority according to the operational severity of their exceptions.

Higher-risk issues such as stuck orders and quantity mismatches receive greater weighting, while multiple simultaneous exceptions increase the overall priority of an order.

## Operational Analysis

The project analyses exception patterns across:

* Warehouses
* Sellers
* Carriers
* Warehouse-carrier combinations

It also compares:

* Total exception volume
* High-priority order count
* High-priority rate

This helps distinguish between locations or partners with many minor issues and those associated with a greater proportion of urgent problems.

## AI-Assisted Reporting

The Python workflow creates a structured operational summary that can be supplied to a generative AI system such as Claude.

The intended AI reporting layer can:

* Summarise operational performance
* Highlight immediate priorities
* Identify patterns
* Recommend investigation areas
* Produce a concise daily operations report

The workflow is designed so that calculated Python outputs provide the factual basis for AI-generated reporting, reducing reliance on unsupported AI assumptions.

## How to Run

1. Open `AI_Order_Exception_Analyst.ipynb` in Google Colab or Jupyter Notebook.
2. Run the cells from top to bottom.
3. The notebook will generate the synthetic fulfilment dataset.
4. The workflow will detect and prioritise operational exceptions.
5. Review the generated summaries, charts and exception queue.
6. The exception queue can be exported to CSV for further analysis.

## Limitations

The dataset used in this project is synthetic.

Therefore, the warehouse, seller and carrier findings do not represent the performance of any real organisation.

The purpose of the project is to demonstrate the design of an automated operations workflow rather than produce real-world logistics conclusions.

## Future Improvements

Future development could include:

* Connecting to live order-management APIs
* Automatically importing warehouse and carrier data
* Scheduling daily exception checks
* Sending alerts for high-priority orders
* Building a reusable Claude Skill
* Using the Claude API for automated report generation
* Creating an interactive dashboard
* Storing historical exception trends
* Developing predictive models for future fulfilment delays

## Project Purpose

This project was developed to demonstrate practical application of Python, data analysis, operational problem-solving and AI-assisted automation in an e-commerce fulfilment environment.

> **Note:** This project uses entirely synthetic data created for demonstration purposes. No real seller, warehouse, carrier or customer data is used.

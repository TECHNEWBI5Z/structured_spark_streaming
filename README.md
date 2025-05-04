# Structured Spark Streaming Example

This project demonstrates two simple streaming data pipelines using Apache Spark Structured Streaming. It focuses on building Bronze and Silver table layers for a basic `orders` dataset.

## Project Overview

### 1. Bronze Table: `orders`
A simple raw table created to store incoming order data. It represents the landing zone for raw data before any transformations.

### 2. Silver Table: `orders_transformed`
A cleaned and transformed version of the raw data stored in the Bronze table. This table is ready for downstream analytics or reporting.

## Streaming Flows

### Flow 1: Bronze to Silver
This streaming flow reads data from the Bronze `orders` table and writes transformed results to the Silver `orders_transformed` table using Spark Structured Streaming.

### Flow 2: Source File to Silver
In this approach, data is directly read from a file source location and transformed before being written to the Silver `orders_transformed` table using Structured Streaming.

## Resources

The project includes a few simple resource files to help set up and run the streaming pipelines.

## How to Run

1. Set up Spark environment.
2. Place your sample data files in the input directory if using the file-based flow.

## Notes

- The project uses append mode for streaming writes.
- Make sure the checkpoint locations are correctly configured for state management.

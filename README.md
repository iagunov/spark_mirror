# Spark Mirror

This repository contains code for processing delta data using Apache Spark.

## Setup

To run this code, ensure you have the necessary and `requirements.txt`

## Decorators

Two decorators are included in the code:
- `execution_time`: Measures the execution time of a function.
- `error_log`: Handles errors and logs exceptions.

## Logging

Logging is set up to log messages to a MySQL database. You can create a log database and table using the `create_logdb` function.

## Functions

Several functions are defined for data processing:
- `get_log`: Retrieves log data from a MySQL database.
- `get_mirror`: Retrieves mirror data from a CSV file.
- `get_delta`: Creates a delta between mirror and delta data.
- `merge_delta`: Manages the merging of delta files for a specified table.

## Main Function

The `merge_delta` function orchestrates the merging of delta files for a specified table. It processes delta files one by one, creating a mirror if needed and logging the actions.

## Usage

You can use the provided functions to process delta data efficiently using Apache Spark.

## Example

To merge delta files for a table named 'data_deltas' with keys ['account_rk'], you can call the `merge_delta` function with the appropriate parameters.

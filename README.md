# Spark Streaming for Invoices

This repository implements a Spark Streaming data pipeline with two layers: Bronze and Silver, and includes a Test Suite to validate the pipeline's functionality.

## Description

### Bronze Layer:

- Reads raw JSON data.
- Enforces schema.
- Archives processed files.
- Outputs invoices_bz Delta table.

### Silver Layer:
- Reads invoices_bz.
- Explodes nested fields.
- Flattens invoice line items.
- Outputs invoice_line_items Delta table.

### Test Suite:
- Automates testing of the pipeline.
- Validates ingestion, transformation, and output accuracy.

## Arquitecture
![Streaming for invoices drawio](https://github.com/user-attachments/assets/d493c71c-d020-4af0-9cf6-8d1e2a3a6dcf)
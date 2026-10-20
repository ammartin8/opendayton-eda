# Litter Containers Data Exploration

## Project Overview

This notebook explores the City of Dayton's litter containers dataset — an ArcGIS Feature Server layer maintained by the Division of Waste Collection. The goal was to understand the data structure, identify null patterns, and assess what questions can be answered (and what can't) before contributing a curated entry to the [OpenDayton](https://github.com/codefordayton/opendayton) dataset catalog.

The notebook pulls raw data from the ArcGIS API, inspects field types and coded values, and documents the gap between recorded and unrecorded inspection data. This informed the `fields` allowlist and `caveats` written for the OpenDayton `layers.yaml` entry.

## Problem
The City of Dayton maintains an ArcGIS layer with 424 litter bins, but roughly half have no inspection data recorded (null values for condition, rust, door, topper, painting). This makes it hard to answer basic questions like "how many bins have rust?" without being misleading.

## Audience
- Residents who want to know about litter bin conditions in their neighborhood
- Advocates filing complaints or requesting maintenance
- City of Dayton Division of Waste Collection

## Tool Stack
- Python, Jupyter Notebook
- Pandas for data manipulation
- ArcGIS REST API for data extraction

## Data Purpose
The litter containers dataset tracks the location and condition of public litter bins across Dayton. Each record includes a street address and completion status; inspection fields (overall condition, rust, door, topper, painting) are populated for roughly half the bins. The data is useful for advocacy and complaint-filing.

## Key Findings
- 424 total bins
- 206 have been inspected (Completed = Yes), 218 have not (Completed = No)
- Null values represent "not recorded" — not a condition — and ArcGIS silently drops them from group-by queries

## About Me
Hello 🌎️! I'm Amah! I am passionate about building scalable, reliable, and efficient data systems that empower business intelligence. This project demonstrates my ability to conduct data analysis in order to contribute to an mcp server that exposes resources and tools to an AI model that allows residents to ask natural language questions about its data resources.

👋🏿 Open to Opportunities and Collaborations

Personal website: [Personal Website](https://amahmartin.me) \
LinkedIn: [Linkedin Profile](https://www.linkedin.com/in/amahmartin) \
GitHub: [Github Profile](https://github.com/ammartin8)
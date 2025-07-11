# Improvado-Data-Source-API-Analyst-Test

## Overview

This repository contains the test for the hiring process at Improvado for API Source Analyst
The objective was to explore the GitHub API, extract data programmatically, handle common API challenges, and document the entire process.

---

## Repository Structure

- `/Content/`
  - `github_api_colab_notebook.ipynb` – Google Colab notebook with API calls, authentication, pagination, error handling, and data extraction.
  - `troubleshooting_guide.md` – Guide on common issues and how to resolve them during API work.

- `/Postman_Collection/`
  - *(Optional)* Postman collection JSON files if Postman was used.

- `README.md` – This file, explaining the project and steps.

---

## Step-by-Step Summary

### Step 1: Research GitHub API
- Investigated the relevant GitHub API endpoints to cover client needs such as:
  - Searching public repositories.
  - Listing commits.
  - Retrieving repository content.
- Studied documentation on requests logic, pagination, rate limits, and error handling.

### Step 2: Setup GitHub Repository
- Created this public repository named `Data-Source-API-Analyst-Test`.
- Structured folders as requested.
- Added descriptions and documentation.

### Step 3: API Extraction with Google Colab
- Developed a fully working Colab notebook performing:
  - Authentication with a personal access token.
  - Searching repositories.
  - Paginated extraction of commits.
  - Retrieval of file contents (README.md).
  - Rate limit checking.
  - Saving response samples as JSON files.
- Included detailed comments in English for clarity.

### Step 4: Troubleshooting Guide
- Documented common API issues such as:
  - 401 Unauthorized errors.
  - Rate limits handling.
  - 404 Not Found errors.
- Provided best practices for error handling in Colab and Postman.

### Step 5: Get Result
- Saved all results and outputs in this repository.
- Provided exports of the Colab notebook (`.ipynb`) and troubleshooting guide.
- *(Optional)* Postman collection export if applicable.

---

## How to Use

1. Replace the placeholder `GITHUB_TOKEN` in the Colab notebook with your GitHub personal access token.
2. Run the notebook step-by-step to extract and inspect data from GitHub API.
3. Refer to the troubleshooting guide if you encounter common API issues.
4. Explore saved JSON files to understand the data format and response structure.

---

## Reflection

This assignment helped solidify my understanding of:

- RESTful API interaction using Python and HTTP requests.
- Handling authentication and authorization with tokens.
- Managing pagination and rate limits.
- Debugging and troubleshooting common API errors.
- Organizing and documenting data extraction workflows for clarity and reproducibility.

---

## Contact

For questions or feedback, feel free to contact me.




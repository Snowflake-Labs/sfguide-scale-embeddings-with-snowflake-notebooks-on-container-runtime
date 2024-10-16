# Scale Embeddings with Snowflake Notebooks on Container Runtime

## Overview
[Snowflake Notebooks on Container Runtime](https://docs.snowflake.com/en/user-guide/ui-snowsight/notebooks-on-spcs) are a powerful IDE option for building ML workloads at scale. Container Runtime (Public Preview) gives you a flexible container infrastructure that supports building and operationalizing a wide variety of resource-intensive ML workflows entirely within Snowflake. 

This notebook demonstrates how you can load an open source embedding model, generate embeddings using a GPU, evaluate a dataset for a RAG solution, deploy the embedding model, perform large scale batch inference, and save results to a Snowflake table without a lot of complex infrastructure setup and management.

> #### QuickStart guide is coming soon! For now, follow the Setup instructions below.

## Prerequisites
- Access to a Snowflake account with ACCOUNTADMIN
- Access to run Notebooks on Container Runtime in Snowflake
- Foundational knowledge of Data Science workflows
- Completed [Getting Started with Snowflake Notebook Container Runtime
](https://quickstarts.snowflake.com/guide/notebook-container-runtime/index.html#0)

## Setup
- Navigate to Worksheets, click "+" in the top-right corner to create a new Worksheet, and choose "SQL Worksheet".
- Paste the [setup.sql](/scripts/setup.sql) code in the worksheet.
- Run all commands to create Snowflake objects

## Run the Notebook
- Download the notebook: [0_start_here](notebooks/0_start_here.ipynb)
- Change role to `EMBEDDING_MODEL_HOL_USER`
- Navigate to `Projects` > `Notebooks` in Snowsight
- Click `Import .ipynb` from the + Notebook dropdown
![](/scripts/img/import.png)
- Create a new notebok with the following settings:
![](/scripts/img/create_notebook.png)
- Click the three dots in the top right > `Notebook Settings`
![](/scripts/img/edit_settings.png)
- Enable external access integrations
![](/scripts/img/external_access.png)
- Run cells in the notebook!
> Once you reach the end, you'll kick off a batch embeddings inference job and will be able to see something like this in your query profile:
![](/scripts/img/query_profile.png)
n8n Angel Investor Lead Gen Pipeline

This project automates the discovery of high-value angel co-investors by tracing the portfolio companies of "Hero" investors and identifying other individual participants in their funding rounds.

System Architecture

The workflow follows a 6-stage ETL process:

Ingest: Consumes a seed list of top-tier AI investors.

Discovery: Uses SixtyFour web agents to find 30+ recent deals per seed investor.

Extraction: Scrapes funding round data to find co-investors, filtering for individuals only.

Aggregation: Deduplicates leads and calculates "deal overlap" to prioritize outreach.

Enrichment: Appends LinkedIn, Email, and Mobile data via SixtyFour API.

Export: Generates a clean CSV ready for dialers (JustCall) or email warm-up tools.

Setup

Run n8n: docker-compose up -d

Import Workflow: Open n8n at localhost:5678 and import workflow.json.

Configure API: Add your SixtyFour API credentials in the n8n credentials manager.

Execute: Trigger the "Seed List" node to begin the crawl.

Requirements

n8n (Docker)

SixtyFour.io API Key (with web agent credits)
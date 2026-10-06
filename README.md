# AWS Cost Optimization Advisor — Power BI Dashboard

![Project Overview](assets/0_project_overview.png)

<p align="center">
  <img src="https://img.shields.io/badge/Built_with-Power_BI-F2C811?style=flat-square" alt="Built with: Power BI"/>
  <img src="https://img.shields.io/badge/Data_prep-Google_Colab-F9AB00?style=flat-square&logo=googlecolab&logoColor=white" alt="Data prep: Google Colab"/>
  <img src="https://img.shields.io/badge/Data-AWS_EC2_pricing-c9440c?style=flat-square" alt="Data: AWS EC2 pricing"/>
</p>

An interactive Power BI dashboard for cloud cost analysis, built around real AWS EC2 pricing data — designed for cloud architects, FinOps analysts, and decision-makers who need to compare pricing, spot anomalies, and find savings opportunities across regions and instance types.

![Global EC2 Cost Intelligence](assets/dashboard-global-ec2-cost-intelligence.png)

## What it covers
- **Global EC2 pricing** — average price per hour across all AWS regions, plotted on a world map
- **Cost anomalies** — vCPU count vs. hourly price, memory size vs. hourly price, by instance family and processor architecture
- **Savings opportunities** — reserved savings %, rightsizing recommendations by instance family
- **Linux vs. Windows** pricing comparison, toggleable via report parameters
- **Instance pricing analysis** — price-tier distribution, per-region breakdowns, cost efficiency scoring

![Instance Pricing Analysis](assets/dashboard-instance-pricing-analysis.png)

## How it's built
- Data sourced from official AWS pricing data, sampled and cleaned in Google Colab before loading into Power BI
- **Star schema** data model linking dimension and fact tables
- Calculated measures: cost efficiency score (composite), savings %, price difference vs. global average
- Field parameters for dynamic metric switching (e.g. toggling OS)

## Tech
Power BI (`.pbix`), DAX measures, Google Colab for data prep

---
*Note: opening the `.pbix` file requires Power BI Desktop (Windows). The screenshots above show the dashboard in action.*

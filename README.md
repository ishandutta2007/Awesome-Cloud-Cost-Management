# Awesome-Cloud-Cost-Management

## Top Cloud Cost Management (FinOps) Platforms Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Cost Visibility, Anomaly Detection, Resource Optimization & FinOps Automation*  

**Last updated: September 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Cloud Cost Management (FinOps)**. These tools help platform teams, finance, and engineering leaders monitor cloud spend, allocate costs to teams, detect anomalies, and optimize resource utilization across AWS, Azure, GCP, and Kubernetes.



**Examples** include CloudZero, Finout, Cast AI, Apptio Cloudability, Flexera One, Spot by NetApp, Vantage, Densify, Zesty, ProsperOps, Kubecost, IBM Turbonomic, Harness Cloud Cost Management, CloudHealth by VMware, and nOps (the category leaders).



**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, custom FinOps automation, and transparent cost data — ideal for teams that need full control over their cloud cost pipeline without per-resource SaaS fees or vendor lock-in.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents



- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[CloudZero](https://www.cloudzero.com/)**  

  Cloud cost intelligence platform focused on **unit economics** — answering "what does this customer or feature cost us" rather than just infrastructure totals. Hourly granularity, long retention, and integration breadth beyond the Big 3 clouds. Single subscription model.



- **[Finout](https://www.finout.io/)**  

  FinOps platform with **MegaBill** technology that unifies and normalizes billing data from multiple cloud providers and SaaS tools. Provides cost visibility, anomaly detection, and Kubernetes cost management.



- **[Cast AI](https://cast.ai/)**  

  Autonomous Kubernetes cost optimization platform. Actively right-sizes pods, selects optimal instance types, manages spot interruptions, and consolidates nodes without manual intervention. For teams ready to act on cost data, not just observe it.



- **[Apptio Cloudability](https://www.apptio.com/products/cloudability/)**  

  Enterprise FinOps platform (IBM) for cloud cost management, optimization, and governance. Provides allocation, anomaly detection, and commitment management across multi-cloud environments.



- **[Flexera One](https://www.flexera.com/)**  

  Hybrid IT and cloud cost management platform. Provides cost visibility, optimization recommendations, and governance across cloud, SaaS, and on-premises.



- **[Spot by NetApp](https://spot.io/)**  

  Cloud infrastructure optimization platform. Automates cluster scaling, bin-packing, and spot instance management to reduce compute costs by 60-90%.



- **[Vantage](https://www.vantage.sh/)**  

  Cloud cost transparency platform with flat annual fee. Provides Kubernetes cost reporting, virtual tagging for allocation, and multi-cloud cost visibility.



- **[Densify](https://www.densify.com/)**  

  Cloud resource optimization using machine learning for rightsizing and workload placement across Kubernetes and virtualized environments.



- **[Zesty](https://zesty.co/)**  

  Automated cloud cost optimization platform. Dynamically adjusts committed use discounts and reserved instances based on real-time workload demand.



- **[ProsperOps](https://www.prosperops.com/)**  

  Automated commitment management platform. Optimizes Reserved Instances and Savings Plans to reduce cloud costs without manual intervention.



- **[Kubecost](https://www.kubecost.com/)**  

  Commercial Kubernetes cost management platform built on the OpenCost engine (IBM). Adds bill reconciliation for discounts, reserved instances, and spot pricing, plus rightsizing recommendations, anomaly detection, and multi-cluster aggregation. Free edition supports unlimited clusters up to 250 cores with 15-day retention .



- **[IBM Turbonomic](https://www.ibm.com/products/turbonomic)**  

  Application resource management platform. Assures performance while optimizing cost across cloud, on-premises, and hybrid environments.



- **[Harness Cloud Cost Management](https://harness.io/products/cloud-cost-management)**  

  Cloud cost management module within the Harness platform. Provides Kubernetes cost visibility, anomaly detection, and optimization recommendations. Cost estimation in IaCM uses Infracost for Terraform plans .



- **[CloudHealth by VMware](https://www.vmware.com/products/cloudhealth.html)**  

  Multi-cloud management platform with cost optimization, governance, and security capabilities.



- **[nOps](https://www.nops.io/)**  

  AWS cost optimization and governance platform with container visibility, automated tagging, and commitment management.



## Open-Source GitHub Projects



### Cloud Cost Governance & Automation



- **[Cloud Custodian](https://github.com/cloud-custodian/cloud-custodian)**  

  **The foundational open-source cloud governance and cost optimization engine.** CNCF Incubating Project under **Apache 2.0** license . **YAML-based DSL** for defining policies that filter, tag, and apply actions to cloud resources . Supports **AWS, Azure, and GCP** . **Cost management capabilities**: off-hours scheduling (turn off dev instances at night), garbage collection of unused resources (unattached EBS volumes, idle RDS instances), and utilization-based tagging . Automatically provisions serverless functions for real-time enforcement or runs as a cron job . Real-world example: policy to stop EC2 instances with 14-day average CPU utilization below 1.5% and mark for termination .



- **[Infracost](https://github.com/infracost/infracost)**  

  **Open-source cloud cost intelligence for engineers and CI/CD.** Shows cloud cost estimates for **Terraform, Terragrunt, CloudFormation, and AWS CDK** before changes are deployed . Features **PR comments** with cost diffs, IDE extensions (VS Code, JetBrains, Neovim, Zed), AI agent skills for Claude Code and Cursor, and **CI/CD integrations** . Supports **1,100+ resources across AWS, Azure, and Google Cloud** . **Free and open source** with optional Infracost Cloud SaaS for team policies . Harness IaCM integrates Infracost for cost estimation in Terraform pipelines .



### Kubernetes Cost Visibility



- **[OpenCost](https://github.com/opencost/opencost)**  

  **CNCF Incubating open-source cost monitoring for Kubernetes and cloud spend.** Provides real-time cost allocation by cluster, node, namespace, controller, service, or pod . Multi-cloud support (AWS, Azure, GCP, Oracle Cloud, DigitalOcean) and on-premises via custom CSV pricing . GPU costs, carbon costs, and **MCP server for AI agents** . **Apache-2.0**. **Key limitation**: Uses on-demand list pricing — does not reconcile negotiated discounts, committed-use discounts, or enterprise discount programs. The gap can reach **30-50%** for enterprise accounts .



- **[Kubecost (Free Tier)](https://github.com/kubecost/cost-analyzer-helm-chart)**  

  Commercial product built on OpenCost engine, with a **free tier supporting unlimited clusters up to 250 cores** and **15-day metric retention** . Adds rightsizing recommendations, anomaly detection, and budget alerts beyond OpenCost's visibility-only scope . **Key difference**: OpenCost is the allocation engine; Kubecost is the product built on it .



### Cloud Asset Inventory & Optimization



- **[Komiser](https://github.com/tailwarden/komiser)**  

  **Open-source cloud resource manager and inventory dashboard.** Scans cloud accounts, builds a full inventory of services, and surfaces misconfigurations, underutilized infrastructure, and hidden cost drivers . Supports **AWS, Azure, GCP, DigitalOcean, Civo, and more** . Provides a dashboard to understand resource dependencies and uncover idle, underutilized, and untagged resources .



- **[Steampipe](https://github.com/turbot/steampipe)**  

  **Open-source tool for querying cloud APIs using SQL with zero-ETL.** 150+ plugins covering AWS, Azure, GCP, and Kubernetes . Surface idle resources, underutilized instances, and spend patterns directly via SQL . **Mods** (dashboards) extend capabilities for AWS Well-Architected, compliance, and cost views .



- **[StackQL](https://github.com/stackql/stackql)**  

  **Open-source SQL-based cloud resource management.** Uses a "zero-ETL" approach with SQL interfaces to query and manage cloud APIs . Supports resource creation in addition to querying .



### FinOps Data Standards & Dashboards



- **[FOCUS Specification](https://github.com/FinOps-Open-Cost-and-Usage-Spec)**  

  **FinOps Open Cost and Usage Specification** — an open-source technical specification that normalizes cost and usage billing data across cloud vendors . Supported by the FinOps Foundation. Aims to simplify multi-cloud cost management by standardizing data across platforms, making FinOps skills more transferable . **320 GitHub stars**, active development.



- **[Apache Superset](https://github.com/apache/superset)**  

  **Open-source data exploration and visualization platform.** Used for building FinOps dashboards on FOCUS-formatted billing data . 56% of FinOps practitioners use homegrown tools and 74% use homegrown reports .



### Additional Strong Open-Source Options



- **Cost Governance**: **Cloud Custodian** (CNCF Incubating, YAML DSL, multi-cloud) .

- **Cost Estimation**: **Infracost** (Terraform/OpenTofu/CloudFormation, PR comments, IDE extensions) .

- **Kubernetes Cost**: **OpenCost** (CNCF Incubating, allocation engine) , **Kubecost Free** (250-core limit, 15-day retention) .

- **Asset Inventory**: **Komiser** (dashboard, multi-cloud) , **Steampipe** (SQL queries, 150+ plugins) .

- **Data Standards**: **FOCUS** (FinOps Foundation, billing data normalization) .



**Frameworks for building custom systems**: Combine **Cloud Custodian** for cost governance and automation (off-hours scheduling, garbage collection), **Infracost** for shift-left cost estimation in CI/CD, **OpenCost** for Kubernetes cost allocation, and **Komiser** or **Steampipe** for cloud asset inventory. Add **Apache Superset** or **Grafana** for dashboards on FOCUS-formatted billing data.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Cloud cost management tools require accurate cloud billing API integration; on-demand list pricing may misrepresent actual invoices by **30-50%** without reconciliation .

- **Open-source reality**: The open-source ecosystem for cloud cost management is **mature and production-ready** at the **cost governance** (**Cloud Custodian**), **cost estimation** (**Infracost**), and **Kubernetes allocation** (**OpenCost**) layers. **FOCUS** provides the open standard for billing data normalization . However, **commercial platforms** (CloudZero, Apptio Cloudability, Flexera One) provide deeper **bill reconciliation** (discounts, reserved instances, enterprise agreements), **automated optimization**, and **enterprise support** that open-source alternatives cannot match without significant engineering investment. The open-source path is most viable for organizations with strong platform engineering capacity or for specific use cases like Kubernetes cost visibility or shift-left cost estimation.



---



**Made for FinOps practitioners, platform engineers, cloud architects, and finance teams.**  

Let's make cloud cost management more open, transparent, and efficient.

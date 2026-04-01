# Cloud Project - OpenCart Deployment

## Purpose
This folder documents my cloud project evidence in a reviewer-friendly format, focused on Cloud Engineer execution and Cloud Security Engineer progression.

## Current Evidence
- [cloud-project-opencart-evidence-bundle.zip](cloud-project-opencart-evidence-bundle.zip)
- [cloud-project-opencart-evidence-bundle/Cloud-project-24560064](cloud-project-opencart-evidence-bundle/Cloud-project-24560064)

## Quick Evidence Pointers
Review in this order for fastest understanding:
1. [cloud-architecture.svg](cloud-architecture.svg) for high-level architecture.
2. Deployment Flow section in this README for implementation sequence.
3. Security Controls Mapping section in this README for control coverage.
4. Inside [cloud-project-opencart-evidence-bundle.zip](cloud-project-opencart-evidence-bundle.zip):
	- Cloud-based E-commerce Web.pdf (full cloud implementation report)
	- Finalreport.md.pdf (summary/final write-up)
5. Direct folder view (no ZIP download):
	- [cloud-project-opencart-evidence-bundle/Cloud-project-24560064/Cloud-based E-commerce Web.pdf](cloud-project-opencart-evidence-bundle/Cloud-project-24560064/Cloud-based%20E-commerce%20Web.pdf)
	- [cloud-project-opencart-evidence-bundle/Cloud-project-24560064/Finalreport.md.pdf](cloud-project-opencart-evidence-bundle/Cloud-project-24560064/Finalreport.md.pdf)

Reviewer note: you can evaluate the project from markdown and PDFs first. The demo video is optional supporting evidence inside the bundle.

## Architecture
Architecture diagram:
- [cloud-architecture.svg](cloud-architecture.svg)

Component summary:
- End User: accesses the application through browser requests.
- Edge and Static Delivery: CloudFront distribution serves static assets from S3.
- Application Tier: OpenCart runs on EC2 with Apache and PHP.
- Data Tier: Amazon RDS provides managed relational database services (MySQL/MariaDB context from report content).
- Network Foundation: VPC, subnets, route tables, and internet gateway define connectivity boundaries.
- Scale and Availability: Application Load Balancer and Auto Scaling Group support traffic growth.
- Visibility: CloudWatch and CloudTrail support monitoring and audit trails.

## Deployment Flow
1. Build local baseline with XAMPP and OpenCart installation for functional validation.
2. Design and create AWS VPC with CIDR planning (report shows 10.0.0.0/16 design example).
3. Configure subnets, route tables, and internet gateway for public connectivity.
4. Launch EC2 application instance and configure OpenCart runtime.
5. Provision RDS database and validate app-to-database integration.
6. Add ALB and Auto Scaling Group for higher availability and scaling.
7. Integrate S3 and CloudFront for centralized image/static content delivery.
8. Configure IAM role for EC2-to-S3 access and complete plugin-level integration.
9. Enable CloudWatch metrics/dashboard and CloudTrail audit logging.
10. Run functionality, performance, and security verification, then package evidence.

## Operations Notes
- Keep deployment steps reproducible and versioned in documentation.
- Keep service and data dependencies explicit to reduce troubleshooting time.
- Keep backups and evidence packaging aligned with release checkpoints.

## Security Controls Mapping
| Control Area | Current Implementation Focus | Evidence Location |
|---|---|---|
| IAM | IAM role configuration for EC2 to access S3 and controlled service integration | cloud-project-opencart-evidence-bundle.zip |
| Network Access | VPC, subnet segmentation, route configuration, and controlled ingress path | cloud-project-opencart-evidence-bundle.zip |
| Data Protection | Managed database deployment with session/data handling in cloud design | cloud-project-opencart-evidence-bundle.zip |
| Logging and Monitoring | CloudWatch dashboard/metrics and CloudTrail audit log activation | cloud-project-opencart-evidence-bundle.zip |
| Backup and Recovery | Snapshot and backup-oriented planning documented in architecture and operations sections | cloud-project-opencart-evidence-bundle.zip |

## Troubleshooting Log
| Issue | Root Cause | Fix | Outcome |
|---|---|---|---|
| Cloud evidence bundle could not be pushed to GitHub | File size exceeded GitHub 100MB file limit | Tracked cloud ZIP using Git LFS and pushed again | Cloud bundle is now published and accessible in repository history |
| Cloud section review was slow from root README | Cloud details were not separated into a dedicated technical overview | Added this folder README with architecture, flow, controls, and operations context | Reviewer can navigate cloud evidence faster |
| Evidence packaging depended on a single large archive | Monolithic bundle reduced quick preview ability | Added structured cloud documentation entry points in markdown and architecture summary | Technical context is visible without opening large files first |

## Certifications and Learning Path
- Cloud Foundation badge: https://www.credly.com/badges/7919ecd3-d2a5-47b6-8dfa-52d213b12f06/public_url
- Current progression: Cloud Engineer implementation focus with Cloud Architect study path toward Cloud Security Engineer responsibilities.


## Next Improvement Backlog
- Add service-by-service configuration appendix extracted from cloud report.
- Add deployment validation checklist with pass/fail timestamps.
- Add incident-style cloud security scenario with detection and response mapping.
- Add control-to-evidence mapping with direct links to specific report pages.
- Add architecture version history for future cloud hardening iterations.

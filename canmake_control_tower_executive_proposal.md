# CanMake Control Tower Delivery Proposal

**Manufacturing Feasibility and Planning Intelligence Platform**

This proposal summarizes the business problem, production scope, phase roadmap, high-level technical approach, production infrastructure requirement, risks, and success criteria for **CanMake Control Tower**.

## 1. Business Problem

C&S needs a production-grade planning cockpit that helps production, material planning, procurement, scheduling, sales, and management teams make faster manufacturability decisions using enterprise planning data.

Today, planners evaluate demand, BOM structure, raw material availability, packaging material availability, inventory, work orders, procurement status, and production constraints through slow, spreadsheet-driven checks. This creates delayed feasibility decisions, unreliable production commitments, repeated re-planning, emergency procurement, idle capacity, and limited cross-department visibility.

CanMake Control Tower will provide a centralized planning intelligence layer that converts business planning data into actionable feasibility, shortage, and production planning insights.

## 2. Business Expectations

C&S expects the platform to support the following decisions and outcomes:

- Which finished goods can be produced now?
- How many finished units can be produced from available stock?
- Which raw materials or packaging materials are blocking production?
- What minimum purchase is required to maximize production?
- Which finished goods should be prioritized first?
- What changes if demand, inventory, procurement, or priority changes?
- Where are planning risks, production delays, supplier lead-time issues, and anomalies?

## 3. C&S Scope Summary

| Functional Area | Primary Owner | Priority | Business Intent |
| --- | --- | --- | --- |
| FG Manufacturability Analysis | Production Planner | High | Calculate finished goods feasibility from stock and BOM availability. |
| RM Allocation and Freeze Controls | Material Planner | High | Reserve or freeze materials for planned production and avoid double allocation. |
| Scheduling and Capacity Planning | Scheduler Planner | High | Improve production sequence, capacity usage, and sales visibility. |
| Shortage Decision With Minimal Purchase | Production Planner | Medium | Identify shortages and recommend minimum purchase quantities. |
| Production Order Progress Tracking | Production Scheduler | Medium | Track order completion, delays, WIP status, and plan-versus-actual progress. |
| Supplier Lead-Time Management | Material Planner | Medium | Use supplier lead times and vendor performance in planning. |
| Integration and Data Synchronization | IT/ERP Integration Team | High | Keep Oracle planning data and CanMake Control Tower synchronized. |

## 4. Proof of Concept Summary

The POC validated the core planning flow:

```text
Demand + BOM + Inventory -> Feasibility -> Shortages -> Production Plan
```

The POC confirmed that planning data can be read, demand can be exploded through BOM/process structure, leaf or purchasable components can be identified, inventory can be compared with requirements, and outputs can be produced for FG feasibility, material shortages, production recommendations, usage ranking, scenario summaries, and planner assistant responses.

Phase 1, named **Foundation Launch**, will convert this validated logic into production-ready modules that are modular, optimized, reusable, auditable, and suitable for multi-user business operations.

## 5. Production Readiness Gaps

| Gap | Production Requirement |
| --- | --- |
| Manual workbook input | Controlled Oracle database integration. |
| POC user experience | Production web application for planners and managers. |
| Manual access handling | Secure launch from Oracle APEX with authorized access only. |
| Temporary outputs | Persistent scenario history, audit trail, and report downloads. |
| Single-user workflow | Multi-user processing with job status and failure handling. |
| Limited POC scope | Phase-based expansion into allocation, scheduling, supplier intelligence, forecasting, risk, and anomaly modules. |

## 6. Target Production State and Phase Roadmap

CanMake Control Tower will be delivered as a private-server production planning cockpit in controlled phases.

### Phase 1: Foundation Launch

Phase 1, **Foundation Launch**, will deliver the core production cockpit:

- Authorized users launch CanMake Control Tower from Oracle APEX without a second login.
- CanMake Control Tower validates a secure, short-lived one-time launch code.
- The system reads approved demand, BOM, inventory, and planning data directly from the C&S Oracle database.
- Planners create and run manufacturability scenarios.
- Users view FG feasibility, shortages, blockers, and production recommendations.
- Scenario results are stored for history, reporting, and audit.
- Reports and required outputs are downloadable.
- The system supports around 50 users on the C&S private production server.

This replaces the manual Excel upload workflow for production. Excel may remain only as a temporary support or testing format if needed.

### Delivery Roadmap

| Phase | Focus | Expected Business Outcome |
| --- | --- | --- |
| Phase 1 - Foundation Launch | FG manufacturability, material shortages, production plan recommendations, scenario history, reports, secure APEX launch, private-server deployment | 80 to 90 percent reduction in manual manufacturability validation time, faster order commitment, better shortage visibility |
| Phase 2 - Smart Allocation | Minimal purchase recommendation, RM/PM allocation view, allocation conflict detection, reservation/freeze recommendation | Reduced unnecessary procurement, better material utilization, fewer allocation conflicts |
| Phase 3 - Execution Control | Work order/WIP integration, progress tracking, plan-versus-actual dashboard, capacity view, basic sequence recommendation | Better schedule adherence, improved capacity utilization, fewer shortage-driven reschedules |
| Phase 4 - Supply Risk Shield | Supplier lead-time history, expected receipt visibility, delay risk score, lead-time variance, procurement exception alerts | Fewer emergency purchases, more stable production plans, improved procurement accuracy |
| Phase 5 - Predictive Planning | Demand forecasting, anomaly detection, FG/material risk scoring, supplier delay prediction, scenario recommendation, planner assistant | Earlier risk visibility, better demand-supply alignment, scalable planning intelligence |

## 7. Phase 1: Foundation Launch Delivery Workstreams and Estimated Timeline

The Phase 1, **Foundation Launch**, estimate assumes C&S provides structured Oracle planning data and production environment access on time.

| Workstream | Duration | Main Activities | Key Deliverables |
| --- | ---: | --- | --- |
| Discovery and Data Contract | Week 1 to 2 | Confirm scope, data contract, APEX launch flow, user roles, deployment constraints | Signed data contract, launch assumptions, Foundation Launch scope sign-off |
| Product and Delivery Foundation | Week 2 to 4 | Branding, app foundation, configuration, logging, health checks | Branded application foundation, base delivery structure |
| Enterprise Data Integration | Week 4 to 8 | Read Oracle planning data, validate fields, map data into planning inputs | Data integration module, validation checks, test cases |
| Core Planning Workflow | Week 7 to 10 | Integrate planning engine, scenario creation, result storage, reports | Scenario workflow, planning results, history, downloads |
| Planning Dashboard | Week 7 to 12 | Build demand, feasibility, shortage, production plan, and report screens | Production-ready planning dashboards |
| Secure Enterprise Launch | Week 10 to 13 | Enable APEX launch, session handling, expiry, audit trail | Secure launch flow and access audit |
| Multi-User Processing | Week 11 to 14 | Add background jobs, progress states, retries, concurrency checks | Multi-user execution and job tracking |
| Production Readiness and UAT | Week 13 to 16 | Production deployment, operations handover, UAT issue closure | Deployment guide, operations guide, UAT sign-off package |

Estimated Phase 1, **Foundation Launch**, timeline:

```text
3 to 4 months
```

### Phase 1 Resource Allocation Summary

Legend: `1.0` = full-time, `0.5` = half-time, `0.2-0.4` = part-time support, `-` = not planned for that workstream.

| Workstream | Timeline | Backend | Frontend | Data Scientist / AI | QA | DevOps | BA / Coordinator | C&S IT/Data |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| Discovery and Data Contract | Week 1 to 2 | 0.5 | - | - | - | - | 0.3 | 0.2 |
| Product and Delivery Foundation | Week 2 to 4 | 1.0 | 0.5 | - | - | 0.3 | 0.3 | - |
| Enterprise Data Integration | Week 4 to 8 | 1.0 | - | - | 0.3 | - | 0.3 | 0.4 |
| Core Planning Workflow | Week 7 to 10 | 1.0 | - | 0.2 | 0.5 | - | 0.3 | - |
| Planning Dashboard | Week 7 to 12 | 0.5 | 1.0 | - | 0.5 | - | 0.3 | - |
| Secure Enterprise Launch | Week 10 to 13 | 1.0 | - | - | - | 0.3 | 0.3 | 0.4 |
| Multi-User Processing | Week 11 to 14 | 1.0 | - | - | 0.5 | 0.5 | 0.3 | - |
| Production Readiness and UAT | Week 13 to 16 | 0.5 | 0.5 | - | 0.5 | 0.7 | 0.3 | - |

## 8. High-Level Tech Stack

The final stack should be confirmed during discovery based on C&S infrastructure standards, security policy, and Oracle connectivity requirements.

| Layer | Recommended Stack | Purpose |
| --- | --- | --- |
| Frontend | React or C&S-approved TypeScript web framework | Planning cockpit, dashboards, scenario workflow, downloads |
| Backend API | Python FastAPI or C&S-approved API framework | Scenario orchestration, access flow, reports, integrations |
| Planning engine | Modular Python services | BOM explosion, FG feasibility, shortage analysis, production planning |
| Source data | C&S Oracle database views or approved read interfaces | Demand, BOM, inventory, purchase, supplier, work order, WIP, capacity data |
| Application data store | PostgreSQL or C&S-approved relational database | Scenario history, run outputs, audit trail, user/session metadata |
| Background processing | Worker queue or scheduler service | Long-running scenario jobs, retries, job status |
| Reporting | XLSX/CSV/PDF generation | Downloadable planning outputs |
| Enterprise launch | Oracle APEX one-time launch code | Seamless authorized launch without second login |
| Deployment | C&S private Linux server, service manager, optional containers | Controlled production deployment |
| Security and observability | HTTPS/TLS, secrets management, structured logs, health checks, audit logs | Secure operation and support readiness |

## 9. Client Production Infrastructure Configuration Needed

C&S is requested to provide only the production environment. Development and internal testing environments will be managed by the delivery team.

### Production Server Sizing

| Production Scope | CPU | RAM | Storage | GPU | Notes |
| --- | ---: | ---: | ---: | --- | --- |
| Phase 1 Foundation Launch | 16 vCPU | 64 GB | 500 GB SSD/NVMe | Not required | Suitable for core manufacturability, shortage analysis, production plan outputs, scenario history, report downloads, and around 50 users. |
| Full Scope Production Expansion | 16+ vCPU | 64 GB | 1 TB SSD/NVMe | Not required for core planning | Recommended when allocation, scheduling, supplier intelligence, forecasting, risk, and larger data volumes are added. |
| Optional Local AI/LLM Hosting | 16+ vCPU | 64 to 128 GB | 1 to 2 TB SSD/NVMe | NVIDIA GPU with 16 to 24 GB+ VRAM | Required only if C&S wants to host AI/LLM models locally. If AI uses an approved external API, production GPU is not required. |

### Production Configuration To Be Provided By C&S

| Area | Production Configuration Needed From C&S | Responsibility |
| --- | --- | --- |
| Production server or VM | Approved private Linux server or VM with selected CPU, RAM, SSD/NVMe storage, and backup policy | C&S provides the server; delivery team deploys CanMake Control Tower. |
| Deployment access | Approved SSH, bastion, VPN, or C&S-defined deployment process | C&S controls access; delivery team installs and configures application services. |
| Operating system | Approved Linux OS, server hardening, patching policy, base security configuration | C&S Ops owns OS security, patching, and administration. |
| Firewall and network | Route from app server to Oracle DB, approved ports, firewall rules, VPN/internal access | C&S Ops owns firewall, routing, and network security. |
| Internal URL and HTTPS | DNS name, production URL, SSL/TLS certificate, reverse proxy/load balancer if required | C&S Ops owns DNS, HTTPS, routing, and gateway configuration. |
| Oracle database access | Read-only service account, host, port, service name, schema, credentials, approved planning views | C&S IT/data team provides access. Write-back requires separate approval. |
| Planning data views | Demand, BOM, inventory, item master, purchase, supplier, lead-time, work order, WIP, and capacity views as applicable by phase | C&S data owners provide definitions, refresh rules, and validation support. |
| Oracle APEX launch | APEX button/menu, authorized user group, one-time launch code, redirect URL, user identity attributes | C&S APEX/IT team configures launch entry and access group. |
| Application database | Approved production database for scenario history, outputs, audit, sessions, and configuration | C&S approves database location; delivery team configures application schema. |
| Runtime services | Approval to run frontend service, backend API, planning engine, background worker, and scheduler | C&S Ops permits services; delivery team configures them. |
| Backups and retention | Backup policy for app database, reports if stored, logs, and configuration | C&S Ops owns production backup and recovery process. |
| Monitoring and logs | Log location, retention period, health-check monitoring, alert contacts, incident process | C&S Ops owns infrastructure monitoring and first-level operations. |
| Security and secrets | Secret handoff, credential storage, session policy, user access rules, security review | C&S security/Ops owns infrastructure controls; delivery team applies approved application rules. |
| Optional write-back | Approval scope for reservation, freeze, or allocation write-back to Oracle in later phases | If not approved, the system remains in recommendation mode. |

## 10. Delivery Workstreams

| Workstream | Responsibility |
| --- | --- |
| Backend and Planning Workflow | Data integration, planning engine adapter, scenario workflows, result storage, reports, access flow, background processing, logging |
| Frontend Experience | Dashboards, scenario flow, data grids, charts, loading/empty/error states, report downloads |
| C&S Data and Launch Support | Input data readiness, APEX launch coordination, access support, data validation |
| DevOps and Deployment | Private-server deployment, services, logs, backups coordination, rollout support, operations documentation |
| QA and UAT | Test data, engine validation, workflow testing, access testing, performance testing, UAT issue tracking |

## 11. Key Risks and Dependencies

| Risk | Impact | Mitigation |
| --- | --- | --- |
| C&S data views not ready on time | Delays integration and testing | Finalize data contract early and use representative sample data until live data is ready. |
| Field mapping differs from POC workbook | Planning logic adjustment may be required | Keep a mapping layer between source data and planning logic. |
| APEX launch coordination is delayed | Access flow may be delayed | Confirm launch flow during discovery and involve C&S IT early. |
| Write-back permissions are not approved | Allocation freeze cannot be automated in Phase 2 | Start with recommendation mode and add write-back only after approval. |
| Heavy concurrent scenario runs | Slow user experience | Use background processing and include concurrency testing in Phase 1. |
| Data quality issues | Incorrect recommendations | Add validation, exception reports, and data health checks. |

## 12. Phase 1: Foundation Launch Acceptance Criteria

Phase 1, **Foundation Launch**, should be considered successful when:

- Authorized users can launch CanMake Control Tower from Oracle APEX without a second login.
- Users do not need to upload Excel files for the production workflow.
- The system reads approved demand, BOM, and inventory data from the C&S Oracle database.
- Users can run manufacturability scenarios and view FG feasibility, shortages, blockers, and production recommendations.
- Scenario history, downloads, access control, and audit trail are available.
- Around 50 users can use the system without major blocking.
- The system runs on the C&S private production server with agreed production support controls.

## 13. Final Summary

CanMake Control Tower will convert the validated POC planning logic into a production-ready private-server cockpit for manufacturability, shortage visibility, production planning, and future planning intelligence. Phase 1, **Foundation Launch**, should focus on secure Oracle APEX launch, direct Oracle data integration, scenario execution, planning outputs, history, downloads, multi-user processing, and production readiness. Later phases should expand through **Smart Allocation**, **Execution Control**, **Supply Risk Shield**, and **Predictive Planning**.

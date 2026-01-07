# Business Overview

## 1. Purpose of This Document
This document provides the business context for the data governance project.
It explains why the data is generated, how it flows through systems, and why
governance controls are required before analytics usage.

This document acts as the foundation for all downstream governance activities
such as data ownership, classification, quality, and security.

---

## 2. Business Scenario

The business operates a digital platform (web/mobile application) where
customers place orders online.

When a customer performs an action (for example, order creation), the data is:
1. Sent through an API
2. Passed via an API Gateway
3. Stored in an OLTP database
4. Later ingested into a Data Lake for analytics and reporting

---

## 3. High-Level Data Flow

API  
→ API Gateway  
→ OLTP Database  
→ Data Lake (Raw Layer)  
→ Analytics / Reporting

This project focuses on **governance controls from API to OLTP**, and later
governance for **batch data movement from OLTP to Data Lake**.

---

## 4. Why Data Governance Is Required

Without governance:
- Data may be inconsistent across systems
- Sensitive data (PII) may be exposed
- Schema changes can break downstream pipelines
- No clear accountability for data issues

With governance:
- Data contracts define structure and expectations
- Ownership ensures accountability
- Classification ensures security and compliance
- Quality rules ensure reliable analytics

---

## 5. Scope of Governance in This Project

Included:
- API data contract definition
- Data ownership and stewardship
- PII and sensitivity classification
- Data quality rule definition
- Security and access considerations
- Audit and change management (logical level)

Excluded:
- Actual production systems
- Real customer data
- Tool-specific implementations

---

## 6. Intended Audience

This document is intended for:
- Data Governance teams
- Data Engineers
- Business Analysts
- Data Analysts
- Interviewers and reviewers evaluating governance maturity

---

## 7. Student-to-Enterprise Mapping

| Enterprise Practice | Student Implementation |
|--------------------|------------------------|
| Confluence | Markdown (GitHub) |
| Collibra / Alation | Excel-based metadata |
| API Gateway Docs | API_Data_Contract.xlsx |
| Governance Council | Documented ownership sheets |

---

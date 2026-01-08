# Audit & Compliance – Audit Log Definition

## 1. Purpose
This document defines the audit logging and compliance requirements
for data flowing from API to OLTP and further to analytics systems.

Audit logs provide traceability, accountability, and evidence
for regulatory and internal audits.

---

## 2. Scope
Audit logging applies to:
- API Gateway access
- OLTP database operations
- Data access by users and systems
- Security and schema changes

---

## 3. Events to Be Logged

### 3.1 API-Level Events
- API request received
- API authentication success/failure
- API payload validation failure
- API retry attempts

### 3.2 OLTP Database Events
- Insert, update, delete operations
- Schema changes
- Failed transactions
- Privileged access

### 3.3 Data Access Events
- PII field access
- Bulk data exports
- Unauthorized access attempts

---

## 4. Mandatory Audit Attributes

Each audit record must include:
- Timestamp
- User or Service ID
- Action performed
- Data asset affected
- Source IP / System
- Success or failure status

---

## 5. Retention Policy

| Event Type | Retention Period |
|-----------|------------------|
| API access logs | 90 days |
| OLTP DML logs | 1 year |
| Schema changes | 2 years |
| PII access logs | 2 years |
| Security incidents | 5 years |

---

## 6. Compliance Mapping

| Regulation / Policy | Applicable Area |
|--------------------|-----------------|
| Internal Security Policy | All systems |
| Data Privacy Law | PII access |
| Audit Policy | Change tracking |

---

## 7. Access to Audit Logs
- Security Admin: Full access
- Governance Team: Read-only
- Auditor: Read-only
- Other roles: No access

---

## 8. Incident Response
Any suspicious activity detected through audit logs must be:
1. Logged
2. Investigated
3. Escalated to security and governance teams
4. Documented for future review

---

## 9. Student-to-Enterprise Mapping

| Enterprise Tool | Student Implementation |
|----------------|------------------------|
| SIEM Tools | Logical definition |
| Audit Databases | Documentation |
| Compliance Dashboards | Manual review |

---

## 10. Conclusion
Audit logging ensures transparency, traceability, and compliance,
forming the final assurance layer of data governance.


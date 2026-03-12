# Project 05 — KYC / AML Customer Onboarding Portal
### Domain: Compliance / Retail Banking | Role: Business Analyst

---

## Overview
A private sector bank was onboarding all customers through branch 
visits only — resulting in 3 to 5 day processing times and high 
operational costs. This project covers complete BA documentation 
for a fully digital KYC and AML onboarding portal targeting 
sub-24-hour account opening with full regulatory compliance.

---

## Business Objective
- Reduce onboarding time from 3-5 days to under 24 hours
- Enable 85%+ of customers to onboard fully digitally
- Achieve AML false positive rate below 3%
- Achieve zero regulatory audit violations in first 6 months

---

## Scope
- Mobile-first multi-step digital account opening form
- Aadhaar OTP-based eKYC via UIDAI API
- PAN verification via NSDL API with fuzzy name matching
- AI-based liveness detection with face match against Aadhaar photo
- AML screening: OFAC SDN, UN Consolidated List, RBI Defaulters, PEP database
- Risk classification: Low / Medium / High with automated and manual paths
- KYC officer review dashboard with SLA tracking
- Welcome kit trigger: account number generation and debit card dispatch

---

## Epics Covered
| Epic | User Stories |
|------|-------------|
| Digital Application Form | KYC-001 |
| Aadhaar eKYC Verification | KYC-002 |
| PAN Verification | KYC-003 |
| Liveness & AML Check | KYC-004 |
| KYC Officer Review Workflow | KYC-005 |

---

## Key Business Rules
- Low risk: auto-approved after successful eKYC and clear AML screen
- Medium risk: KYC officer review with 8-hour SLA
- High risk and PEPs: KYC officer review with 4-hour SLA
- AML Definite Match: auto-rejection, compliance team notified
- Aadhaar OTP max 3 attempts — failure triggers Video KYC fallback
- PAN name must match Aadhaar within 2-character fuzzy tolerance
- Liveness face match score must be 80% or above
- Data retained 10 years post account closure per PMLA mandate
- Re-KYC every 2 years for High-risk customers

---

## UAT Coverage
10 test cases covering eKYC verification, OTP fallback, PAN 
name mismatch, liveness failure, OFAC match auto-rejection, 
PEP classification, low-risk auto-approval, and SLA escalation.

---

## Compliance Mapping
| Regulation | Requirement | Implementation |
|------------|-------------|----------------|
| RBI KYC Master Direction 2016 | OVD-based KYC | Aadhaar eKYC + PAN NSDL |
| PMLA 2002 | AML screening | Multi-list sanction screening |
| PMLA 2002 | 10-year data retention | Database archival policy |
| RBI VKYC Guidelines | Video KYC fallback | VKYC module integrated |
| FATF / RBI PEP Guidelines | Enhanced due diligence | PEP auto High-risk with 4hr SLA |

---

## Tools Used
Jira | Figma | Lucidchart | Agile Scrum

---

## Document
[View Full BA Document (PDF)](./Project05_KYC_AML_Onboarding.pdf)

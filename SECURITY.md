# Security policy

## Scope

This repository contains a **synthetic university security lab**. It simulates a hospital IT environment for detection-engineering research. It has no connection to any real healthcare organisation, real patient data, or production infrastructure.

- The "hospital" is a Python/Flask API backed by SQLite with entirely generated data.
- The attack scenarios are controlled, bounded HTTP sequences against that synthetic API.
- No real malware, exploits, or patient records are used anywhere in this project.

## What is and is not in scope for disclosure

**In scope** — vulnerabilities in the lab code itself that could affect someone who runs it:
- Privilege escalation in the Flask API beyond the documented role model
- Path traversal or arbitrary file write in the document or receiver endpoints
- Authentication bypass in the session or device token system

**Out of scope:**
- The simulated attack behaviours (S1–S4) — these are intentional and documented
- Issues that only apply when the lab is exposed to an untrusted network (it is designed for an isolated VMware host-only network)
- Clinical safety, HIPAA, or HL7/FHIR compliance — this project makes no such claims

## Reporting a vulnerability

If you find a genuine vulnerability in the lab code, please open a GitHub issue with the label `security`. Describe the affected component, reproduction steps, and impact. There is no bug bounty programme; this is a university project.

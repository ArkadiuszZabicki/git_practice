### ==NB: INTERNAL USE CLASSIFICATION!==
==This document is ONLY for internal usage and CANNOT be shared (verbally or in writing) with external parties such as customers – neither in full nor partly.==

---

# Policy for Resending failed sendings

- **Version:** 1.0.0
- **Date:** 2024-04-26 
- **Policy Owner:** Arkadiusz Zabicki,Service Operation Center Team Lead
- **Reviewed by:** Arkadiusz Zabicki, Service Operation Center Team Lead (2024-04-26); Markus Palokangas, Head of R&D Operations, MarTech (2024-04-30); Felix Denbratt, CTO Marketing Line (2024-04-26)


### Version history
| Version | Editor              | Description                                                 | Date       |
|---------|---------------------|-------------------------------------------------------------|------------|
| V.1.0   | Arkadiusz Zabicki, SOC Team Lead | First version                                  | 2024-04-26 |





---

## Introduction

This document defines the policy for resending failed or delayed sendings created as a result of an incident.


### Scope
This policy applies to all R&D staff that participates in on-call rotation and takes active part in Incident Response team (IRT) work.

### Goals
Establish a clear guideline for resending sendings delayed or failed as a result of an incident for each service.


### Definitions
**Service**
APSIS One, APSIS Pro, APSIS Lead, and associated commercial services provided by APSIS to its customers.

**Incident**
An incident is defined as a P1/P2 "major" incident, according to our [Incident Management process](https://github.com/ApsisInternational/processes-and-policies/tree/main/04.%20Processes/Incident%20Process).

**Sending**
Bulk email sending, sms sending, marketing automation sending, transactional sending.

**Failed sending**
Sending that was scheduled by the customer within the service, but was not processed properly and ended up in some sort of 'failed' state.

**Delayed sending**
Sending that was scheduled by the customer within the service, but was not processed properly and ended up in a "stuck" processing state. The sending didn't execute properly, and is waiting to be processed.

**Resend window**
Counted in minutes: the difference between sending schedule time and the moment of manual resend performed by Incident Response Team

---

## Roles & Responsibilities

**Service Operations Center Team (SOC)**
A dedicated team within R&D, that is separate from the normal development teams, whose mission includes being the 1st line responders to any non-automated incidents, and also acting as administrative support function for development teams during all incidents.

**Incident Commander (IC)**
The Incident Commander leads the resolution of incidents through its lifecycle and is the ultimate owner of the incident at any given moment. For more details, please see the [Incident Management process](https://github.com/ApsisInternational/processes-and-policies/tree/main/04.%20Processes/Incident%20Process)

**Incident Response Team (IRT)**
When an incident is identified, a temporary Incident Response Team is created that will be the core team involved in taking the incident through its lifecycle. This team typically consists of members from R&D development teams, additional R&D technical staff and an Incident Commander.


---

## Policy

During the incident process, for incidents that involves failed and delayed Email/SMS sendings, Incident Response Team shall identify all impacted sendings by providing a list of all affected accounts with sending ids' and sending schedule timestamps. Incident Response Team shall not manually resend those impacted sendings, unless the resend window is less/equal to 60 minutes. For all impacted sendings where resend window is greater that 60 minutes, sendings can be resend only after obtaining explicit approval from account owner or account administrator. For that reason Incident Commander must designate a person from SOC team that shall open a communication channel with account owners and/or account administrators to inform them about the situation. 
 

## Types and channels of communication
The following channels are identified as valid options for customer-facing communication about failed sendings:

- Direct Email
	- To the account owner or account admin of the account in the affected service
	- Where such account owner or admin is not available or unknown, to the identified decision maker listed in [Submariner](https://submariners.efficy.cloud.com/) (request help from responsible Account Manager if unclear)
- In-app direct messaging, such as notification system, where available. This includes user/account specific messages send via solutions such as the Apsis One Notification Center (so not the "Global Notification" solution in APSIS One).
- Personal phone call from Account Manager or Senior Management





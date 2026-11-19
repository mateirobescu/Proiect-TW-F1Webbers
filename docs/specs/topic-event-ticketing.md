> Academic year: **2026–2027**  
> Course: **Web Technologies**  
> Status: **Draft v2.0 — for review**

---

# Event Ticketing and Reservations
**Mandatory packages:** `CON` \+ `AUD`  
**Common specification:** [`00-general-specifications.md`](00-general-specifications.md)  
**Package definitions:** [`01-architectural-challenges.md`](01-architectural-challenges.md)

## 1\. Objective

Organizers publish events; users temporarily hold and confirm seats.

## 2\. Minimum functionality

Events, capacities, temporary holds, expiration, confirmation, cancellation, tickets, and administration.

## 3\. Critical invariants and rules

A seat cannot be assigned to two valid tickets; expiration and confirmation cannot create duplicate allocations; critical changes are audited.

## 4\. Data and workload scenario

200 reservations in a demonstration session; at least 20 competing requests against insufficient capacity; holds expire after a configurable test interval.

## 5\. Mandatory package verification

CON: expiration versus confirmation and simultaneous holds; AUD: full ticket lifecycle reconstruction.

## 6\. Common acceptance criteria

- Ordinary users can complete their allowed workflows, but cannot perform privileged operations.  
- Automated tests cover critical workflows, permissions, invalid inputs, and invariants.  
- Both packages are implemented and backed by reproducible evidence; a description alone is insufficient.  
- Coverage report, common load test, and capacity estimate are delivered under the general specification.  
- Synthetic seed data, test scripts, an ADR per package, and demonstration instructions are provided.

## 7\. Milestone deliverables

**M1:** use cases, actors, rules, schema, API, workload profile, test plan, and package alternatives.  
**M2:** API, persistence, critical rules, and initial tests; first demonstrable package scenario.  
**M3:** integrated SPA, completed tests, both packages verified, coverage/performance reports, ADRs, and demonstration.

## 8\. Optional extension

Numbered seats or locally validated QR codes.

**Note:** extensions never replace mandatory requirements and must not require paid services.

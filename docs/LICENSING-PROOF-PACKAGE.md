# Rhodium Germany — Licensing & Proof Package

**Public qualification edition — 29 September 2026**

Rhodium Germany is positioned as a closed, purpose-specific digital infrastructure and software platform. The commercial model does **not** transfer source code, research systems, signing authority, or the internal core architecture.

This document is a technical and commercial qualification summary. It is not a legal opinion, regulatory approval, or warranty of error-free operation. Final rights, warranties, liability allocation, acceptance criteria, and remedies belong in the signed license agreement under applicable law.

## 1. Ownership and separation

- Rhodium Germany retains the intellectual property, research environment, release authority, signing authority, and future core development.
- Licensees receive only the approved Worker-Box deployment required for their authorized field of use.
- Research/Mother systems remain separate from licensee deployments.
- No source-code transfer is part of the standard licensing model.
- Reverse engineering, decompilation, secret extraction, unauthorized modification, sublicensing, and out-of-scope use are prohibited to the extent permitted by applicable law and by the final contract.
- A breach of qualification or license conditions can suspend testing, qualification, exclusivity, updates, or license rights subject to contract and applicable law.

## 2. P=0 release principle

A Rhodium candidate should progress only when:

1. all mandatory reference criteria defined for the specific use case are maintained;
2. integrity/restore requirements are satisfied;
3. no defined mandatory criterion degrades;
4. at least one relevant operational criterion shows a measurable improvement; and
5. the release evidence is documented and sealed.

P=0 is a release and comparison rule. It is **not** a claim of absolute safety, universal superiority, regulatory compliance, or zero defects.

## 3. Evidence currently suitable for public qualification

### Same-payload Cloudflare live-source run

- External source: `https://speed.cloudflare.com/__down`
- Payload: **67,108,864 bytes (64 MiB)**
- Direct download measurement: **197.359 s @ 2.72 Mbit/s**
- Source SHA-256: `9DEFDA6EC268AFA4ADB54233ACDC470E0BDC3076E7393FA8986B6D208B656796`
- Rhodium cold sender wire measurement: **6,950 bytes**
- Rhodium warm sender wire measurement: **5,838 bytes**
- Cold restore hash match: **PASS**
- Warm restore hash match: **PASS**
- External-file roundtrip: **PASS**

**Scope:** the payload was genuinely obtained from Cloudflare, then processed by the Rhodium roundtrip using the exact downloaded payload. The Rhodium cold/warm wire values were produced on the Rhodium test path. This is not yet a fully symmetrical Internet-path-vs-Internet-path throughput comparison. A strict WAN-to-WAN comparison must use the same remote path and measurement points.

### Historical reference evidence

- NASA Juno WAVES: **5.069 GiB → 0.733 GiB**, **85.54%** lossless reduction, restored SHA-256 identical.
- Matrix Live historical reference runs: warm **99.9916%**, cold **81.2486%**, delta **99.9541%** within their defined test setups.
- Evidence Gateway reference: **250,000 events → 1,842**, **99.4021%** reduction with precision **1.0** and recall **1.0** in the defined synthetic benchmark.

Historical values are reference results and are not represented as a new independent revalidation.

## 4. Licensing architecture — three-axis scope

Every commercial right should be bounded by all three axes:

- **Territory:** country, region, or explicitly defined geography.
- **Field of use:** e.g. telecom, finance, cloud, industry, healthcare, automotive, commerce.
- **Technical deployment scope:** e.g. server-to-server, server-to-client, embedded/OEM, transaction path, device fleet, application class.

No partner receives unrestricted global or cross-sector rights by default.

## 5. License families

Typical license families may include:

1. Infrastructure — telecom, ISP, CDN, cloud, data centers.
2. Finance — banks, payments, insurance, FinTech.
3. Industry — manufacturing, machines, robotics, logistics.
4. Embedded/OEM — chips, firmware, routers, devices, computers, IoT.
5. Healthcare — MedTech and clinical infrastructure, subject to applicable approvals.
6. Aerospace — aviation, satellites, space infrastructure, subject to applicable approvals.
7. Business Software — ERP, SaaS, commerce, websites, professional and SME systems.
8. Consumer — end-user devices and consumer digital services.

Smaller operators can participate through narrower field-of-use, regional, channel, OEM, integrator, or reseller licenses instead of requiring a full-country license.

## 6. Bidding table and qualification process

**Public teaser → Qualification → Black-Box Proof → Controlled Pilot → Commercial Bid → License Agreement → Production Acceptance**

### Qualification

A bidder should demonstrate:

- financial capacity appropriate to its license scope;
- existing distribution/customer access;
- technical integration capability;
- compliance capability for the intended sector;
- support and incident-response capability;
- ability to meet minimum commercial milestones.

### Black-Box proof

- No source access is required.
- Only approved interfaces and evidence outputs are exposed.
- The test scope and acceptance metrics are fixed before execution.
- Evidence should be retained with hashes, timestamps, manifests, and reproducible inputs where legally possible.

### Controlled pilot

A pilot does not itself authorize unrestricted production use. Production activation should follow the agreed acceptance matrix.

## 7. Commercial model

The default commercial structure should avoid dependence on a partner's self-reported net profit.

Recommended components:

- **Upfront license / exclusivity fee**
- **Annual minimum guarantee**
- **Usage-based fee** appropriate to the sector (transaction, active unit, device, account, workload, protected endpoint, or other auditable metric)
- **Optional value-share** only where savings or economic value can be measured under a contractually fixed methodology

Exclusivity should be conditional on milestones. If minimum deployment, revenue, support, compliance, or market-coverage obligations are not met, exclusivity can narrow or expire under the agreement.

Comparable market bids can inform future reserve prices. A prior bidder does not automatically obtain rights in another territory or field.

## 8. Authorization, expiry, and continuity

Critical infrastructure should **not** depend on an unsafe surprise kill-switch.

Where technically and legally appropriate, Worker-Box deployments may use signed, time-limited authorization or entitlement leases. The production design should include:

- advance renewal windows;
- grace periods;
- clear customer notices;
- defined non-destructive fallback behavior;
- emergency continuity procedures;
- no destructive action on customer data;
- contractually specified behavior at expiry or termination.

Any authorization mechanism must itself be tested for availability and failure safety before production use.

## 9. Latent defects, acceptance, and production responsibility

Software can contain unknown or latent defects even after extensive testing.

Therefore:

- Benchmark PASS results prove only the defined test criteria.
- Rhodium should not promise that software is universally error-free.
- A licensee must validate the approved deployment against its own environment before production acceptance.
- High-risk sectors may require independent testing, penetration testing, safety validation, certification, regulatory approval, backup/fallback plans, and change-control procedures.
- Production responsibilities, warranties, indemnities, liability caps, insurance requirements, and mandatory legal duties must be allocated in the signed agreement.
- No public document can eliminate liability that cannot legally be excluded.

A suitable commercial statement is:

> The Worker-Box is supplied for controlled qualification and, after contractual acceptance, for the authorized production scope. Unknown or latent defects may exist. Benchmarks and cryptographic integrity checks do not constitute a warranty of universal defect-free operation, cybersecurity clearance, or regulatory approval. The licensee must complete the agreed acceptance and sector-specific validation before production use. Liability and warranties are governed exclusively by the final contract and mandatory law.

## 10. Security and IP controls

The production licensing package should include:

- signed release manifests;
- immutable version identifiers;
- cryptographic verification of authorized builds;
- least-privilege interfaces;
- tenant and license-scope isolation;
- secrets kept outside distributable public artifacts;
- controlled update channels;
- rollback/recovery capability;
- evidence retention policy;
- incident notification procedure;
- prohibition of unauthorized modification and redistribution;
- contractual confidentiality for non-public technical and commercial material.

Public proof repositories must contain only sanitized evidence. Private keys, secrets, customer data, internal research logic, and core implementation details must never be published.

## 11. Updates

New development remains in the research environment until it completes the defined validation process. Only an approved, signed release can move to a Worker-Box deployment.

An update should not silently expand a licensee's territory, field of use, or technical scope.

## 12. High-risk sectors

Finance, healthcare, aerospace, critical infrastructure, and safety-critical industrial deployments require additional external controls. A cryptographic hash match proves integrity of the tested payload; it does not by itself prove safety, regulatory compliance, or cybersecurity of the complete operational system.

## 13. Partner-facing positioning

Rhodium Germany should be presented as:

> A closed digital development and infrastructure platform that can rebuild, test, and refine defined digital functions under a P=0 release discipline. Existing customer business models do not have to be transferred to Rhodium. Only deployments that pass the agreed acceptance criteria progress to production.

Do not publicly claim universal superiority or claim that a competitor has been defeated unless the exact benchmark design supports that statement.

## 14. Contact

**Rhodium Germany**  
Web: https://rhodium-germany.de  
Email: info@rhodium-germany.tech

---

**Legal review required before signature.** This document is a commercial/technical framework and should be converted into jurisdiction-specific contracts by qualified counsel.

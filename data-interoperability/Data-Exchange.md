# Data Exchange

The Data Exchange building block defines how data is actually transmitted between GDDS participants, ensuring technical interoperability, reliability, and alignment with the Trust Framework, Access & Usage Policies, and agreed Data Models.

It covers the Data Plane (the actual transmission) and its integration with the Control Plane (identification, authorisation, policy enforcement, and transaction state management).

Data exchange in GDDS may take many forms, from dataset downloads to continuous streaming, algorithm-to-data execution, or triggered updates. Whatever the mode, the process should be secure, standardised, and discoverable.

### Design Principles
- Protocol Flexibility, with Preferred Set – Support multiple industry-standard protocols while defining a recommended set for quick and interoperable onboarding.
- Linkage to Semantics – All data exchanged must reference the agreed semantic models for clarity and interoperability.
- Federation-Readiness – Protocols should support exchange both inside GDDS and across other data spaces.
- Quality of Service – Ensure reliability, error handling, and completeness of data transfers.

### Core Capabilities
1. Protocol Definition & Publication – Agree on allowed protocols (generic and domain-specific) and publish them in the GDDS service catalogue.
2. Transmission Methods – Support push, pull, and streaming modes for finite and continuous datasets.
3. Querying & Retrieval – Enable querying of complex datasets, geoquerying, historical data retrieval, and triggered updates.
4. Federation Interoperability – Maintain an inventory of accepted protocols and versions for cross-data-space exchange.
5. Version & Change Management – Track versions of protocols to maintain backward compatibility when needed.

*Further content will be added after co-creation sessions.*

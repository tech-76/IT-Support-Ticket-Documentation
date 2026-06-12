# Ticket Lifecycle Diagram

## Purpose

This document shows a professional IT support ticket lifecycle for help desk and service desk environments. It is split into smaller readable diagrams so it displays clearly on GitHub without needing to zoom in.

---

# 1. Ticket Intake and Classification

```mermaid
flowchart TB
    A["Ticket Submitted"] --> B["Review Request Details"]
    B --> C["Confirm User Impact"]
    C --> D["Identify Issue Category"]
    D --> E["Set Priority and Urgency"]
    E --> F["Assign Ticket to Support Queue"]

    classDef start fill:#111827,stroke:#030712,color:#ffffff,stroke-width:2px;
    classDef process fill:#dbeafe,stroke:#2563eb,color:#111827,stroke-width:1px;

    class A start;
    class B,C,D,E,F process;
```

## What Happens at This Stage

- User submits an issue or request
- Help desk reviews the ticket
- Category is identified
- Priority is assigned
- Ticket is routed to the correct queue

## Common Ticket Categories

| Category | Examples |
|---|---|
| Account Support | Password reset, lockout, MFA |
| Email Support | Outlook issue, mailbox access |
| Desktop Support | Slow computer, software issue |
| Network Support | Wi-Fi, VPN, DNS, connectivity |
| Hardware Support | Printer, laptop, monitor |
| Access Request | Shared folder, mailbox, app access |

---

# 2. Investigation and Troubleshooting

```mermaid
flowchart TB
    A["Assigned Ticket"] --> B["Review Ticket History"]
    B --> C["Contact User if More Information Is Needed"]
    C --> D["Perform Initial Troubleshooting"]
    D --> E["Document Steps and Findings"]
    E --> F{"Resolved by First-Level Support?"}

    F -->|Yes| G["Move to Resolution"]
    F -->|No| H["Prepare Escalation Notes"]

    classDef start fill:#111827,stroke:#030712,color:#ffffff,stroke-width:2px;
    classDef process fill:#dbeafe,stroke:#2563eb,color:#111827,stroke-width:1px;
    classDef decision fill:#fef3c7,stroke:#d97706,color:#111827,stroke-width:1px;
    classDef escalate fill:#ede9fe,stroke:#7c3aed,color:#111827,stroke-width:1px;
    classDef success fill:#dcfce7,stroke:#16a34a,color:#111827,stroke-width:1px;

    class A start;
    class B,C,D,E process;
    class F decision;
    class G success;
    class H escalate;
```

## Troubleshooting Notes Should Include

- What the user reported
- Error messages
- What was tested
- Results of each step
- Screenshots or logs if available
- Whether the issue affects one user or multiple users

---

# 3. Escalation Workflow

```mermaid
flowchart TB
    A["Escalation Required"] --> B["Confirm Escalation Reason"]
    B --> C["Add User Impact"]
    C --> D["Add Error Messages"]
    D --> E["Add Troubleshooting Completed"]
    E --> F["Add Screenshots or Logs"]
    F --> G["Assign to Correct Team"]

    G --> H{"Escalation Team"}
    H -->|Level 2 / Sysadmin| I["Advanced Support Review"]
    H -->|Microsoft 365 / Email| J["M365 Admin Review"]
    H -->|Network Team| K["Network Investigation"]
    H -->|Security Team| L["Security Investigation"]
    H -->|Vendor / Hardware| M["External or Hardware Support"]

    classDef start fill:#111827,stroke:#030712,color:#ffffff,stroke-width:2px;
    classDef process fill:#dbeafe,stroke:#2563eb,color:#111827,stroke-width:1px;
    classDef decision fill:#fef3c7,stroke:#d97706,color:#111827,stroke-width:1px;
    classDef team fill:#ede9fe,stroke:#7c3aed,color:#111827,stroke-width:1px;

    class A start;
    class B,C,D,E,F,G process;
    class H decision;
    class I,J,K,L,M team;
```

## Common Escalation Triggers

- Issue requires admin permissions
- Multiple users are affected
- Business-critical service is down
- Security concern or suspicious activity
- Level 1 troubleshooting did not resolve the issue
- Hardware replacement or vendor support is needed

---

# 4. Resolution and User Confirmation

```mermaid
flowchart TB
    A["Resolution Identified"] --> B["Apply Fix or Complete Request"]
    B --> C["Test the Solution"]
    C --> D["Confirm With User"]
    D --> E{"User Confirms Resolved?"}

    E -->|Yes| F["Document Final Resolution"]
    E -->|No| G["Continue Troubleshooting or Re-Escalate"]

    classDef start fill:#111827,stroke:#030712,color:#ffffff,stroke-width:2px;
    classDef process fill:#dbeafe,stroke:#2563eb,color:#111827,stroke-width:1px;
    classDef decision fill:#fef3c7,stroke:#d97706,color:#111827,stroke-width:1px;
    classDef success fill:#dcfce7,stroke:#16a34a,color:#111827,stroke-width:1px;
    classDef escalate fill:#ede9fe,stroke:#7c3aed,color:#111827,stroke-width:1px;

    class A start;
    class B,C,D,F process;
    class E decision;
    class F success;
    class G escalate;
```

## Good Resolution Notes Include

- Root cause or likely cause
- Troubleshooting steps completed
- Final fix applied
- User confirmation
- Follow-up actions if needed

---

# 5. Ticket Closure and Knowledge Capture

```mermaid
flowchart TB
    A["Resolution Confirmed"] --> B["Update Ticket Notes"]
    B --> C["Set Final Status"]
    C --> D["Close Ticket"]
    D --> E["Capture Knowledge Base Notes if Useful"]
    E --> F["Use Insights for Trend Review or Reporting"]

    classDef start fill:#111827,stroke:#030712,color:#ffffff,stroke-width:2px;
    classDef process fill:#dbeafe,stroke:#2563eb,color:#111827,stroke-width:1px;
    classDef final fill:#dcfce7,stroke:#16a34a,color:#111827,stroke-width:1px;

    class A start;
    class B,C,E,F process;
    class D final;
```

## Why This Matters

A strong ticket lifecycle helps support teams:

- Improve documentation quality
- Resolve issues faster
- Escalate more effectively
- Track user impact
- Build a knowledge base
- Identify recurring problems

---

# 6. Full Ticket Lifecycle Summary

```mermaid
flowchart TB
    A["Ticket Submitted"]
    A --> B["Review and Classify"]
    B --> C["Assign Priority"]
    C --> D["Troubleshoot"]
    D --> E{"Resolved?"}
    E -->|Yes| F["Apply Resolution"]
    E -->|No| G["Escalate"]
    G --> H["Advanced Investigation"]
    H --> I["Resolution Found"]
    I --> J["Confirm With User"]
    F --> J
    J --> K{"User Confirms Resolved?"}
    K -->|Yes| L["Close Ticket"]
    K -->|No| D

    classDef start fill:#111827,stroke:#030712,color:#ffffff,stroke-width:2px;
    classDef process fill:#dbeafe,stroke:#2563eb,color:#111827,stroke-width:1px;
    classDef decision fill:#fef3c7,stroke:#d97706,color:#111827,stroke-width:1px;
    classDef escalate fill:#ede9fe,stroke:#7c3aed,color:#111827,stroke-width:1px;
    classDef final fill:#dcfce7,stroke:#16a34a,color:#111827,stroke-width:1px;

    class A start;
    class B,C,D,F,H,I,J process;
    class E,K decision;
    class G escalate;
    class L final;
```

---

# Example Ticket Status Flow

| Stage | Typical Status |
|---|---|
| Ticket created | New |
| Under review | Open |
| Assigned to support | In Progress |
| Waiting for user | Pending User |
| Escalated | Escalated |
| Fix applied | Resolved |
| User confirmed | Closed |

---

# Portfolio Note

This diagram is part of an IT Support Ticket Documentation project designed to demonstrate help desk workflow knowledge, escalation handling, troubleshooting documentation, and service desk best practices.

## Disclaimer

This is a learning and portfolio documentation sample. It does not contain real customer data, private company information, or actual ticketing system records.

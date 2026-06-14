# Settle It — User Flow Diagrams

**Tagline:** Get paid before your customer pays.

Settle It is a compliance-first B2B SaaS + marketplace enabler that connects Sri Lankan SMEs with factoring institutions, NBFCs, private credit funds, and fintech lenders.

This page contains the main user-flow diagrams for the Settle It platform.


## 1. Overall Platform Flow

```mermaid
flowchart TD
    A[SME needs working capital] --> B[SME signs up on Settle It]
    B --> C[SME uploads invoice + documents]
    C --> D[Settle It verifies SME, invoice, buyer, and documents]
    D --> E[Buyer confirms invoice]
    E --> F[Settle It creates risk score + deal package]
    F --> G[Institution reviews deal]
    G --> H[Institution sends financing offer]
    H --> I[SME accepts offer]
    I --> J[Institution releases funding]
    J --> K[Buyer pays invoice later]
    K --> L[Settlement completed]
```


## 2. SME User Flow

```mermaid
flowchart TD
    A[Open Settle It App] --> B[Sign up / Login]
    B --> C[Choose SME Account]
    C --> D[Complete Business Onboarding]
    D --> E[Upload KYC Documents]
    E --> F[Upload Bank Statements]
    F --> G[SME Dashboard]

    G --> H[Upload New Invoice]
    H --> I[Add Invoice Details]
    I --> J[Upload Invoice Documents]
    J --> K[Add Buyer Contact]
    K --> L[Submit Invoice]

    L --> M[Invoice Verification]
    M --> N[Buyer Confirmation]
    N --> O[Risk Score Generated]
    O --> P[Offers Available]
    P --> Q[Compare Offers]
    Q --> R[Accept Offer]
    R --> S[Funding Released]
    S --> T[Track Settlement]
```


## 3. Buyer Confirmation Flow

```mermaid
flowchart TD
    A[Buyer receives confirmation link] --> B[Open secure invoice page]
    B --> C[View supplier details]
    C --> D[View invoice + PO + delivery proof]
    D --> E{Is invoice correct?}

    E -->|Yes| F[Confirm invoice]
    F --> G[Invoice marked as buyer confirmed]
    G --> H[Sent to institutions]

    E -->|No| I[Raise dispute]
    I --> J[Add reason + evidence]
    J --> K[Invoice paused for review]
```


## 4. Institution / Lender Flow

```mermaid
flowchart TD
    A[Institution signs into portal] --> B[View dashboard]
    B --> C[Open deal marketplace]
    C --> D[Filter verified SME invoices]
    D --> E[Review deal package]

    E --> F[Check SME profile]
    F --> G[Check buyer confirmation]
    G --> H[Check risk score]
    H --> I[Check bank statement analysis]
    I --> J{Fund this invoice?}

    J -->|Yes| K[Make financing offer]
    K --> L[SME accepts offer]
    L --> M[Release funding]
    M --> N[Monitor repayment / settlement]

    J -->|No| O[Reject or request more information]
```


## 5. Admin / Compliance Flow

```mermaid
flowchart TD
    A[Admin logs in] --> B[Admin dashboard]
    B --> C[Review SME onboarding]
    C --> D[Check KYC / AML documents]
    D --> E{Approved?}

    E -->|Yes| F[SME verified]
    E -->|No| G[Request more documents]

    B --> H[Review uploaded invoices]
    H --> I[Check duplicate invoice]
    I --> J[Check document match]
    J --> K[Check buyer confirmation]
    K --> L{Invoice valid?}

    L -->|Yes| M[Approve for risk scoring]
    L -->|No| N[Reject / flag / dispute]
```


## 6. Institution SaaS Setup Flow

```mermaid
flowchart TD
    A[Institution requests demo] --> B[Settle It sales call]
    B --> C[Institution agrees to onboard]
    C --> D[Pay one-time setup fee]
    D --> E[Dedicated environment created]
    E --> F[Configure risk rules]
    F --> G[Configure KYC / AML workflow]
    G --> H[Connect APIs / data pipelines]
    H --> I[Train institution team]
    I --> J[Institution goes live]
    J --> K[Monthly SaaS subscription starts]
```


## 7. SME App Footer Flow

```mermaid
flowchart TD
    A[SME App] --> B[Home]
    A --> C[Invoices]
    A --> D[Offers]
    A --> E[Profile]

    B --> B1[Dashboard]
    B --> B2[Cash Flow Snapshot]
    B --> B3[Upload Invoice CTA]
    B --> B4[Partner Institutions]

    C --> C1[Invoice List]
    C --> C2[Upload Invoice]
    C --> C3[Invoice Status]
    C --> C4[Buyer Confirmation Status]

    D --> D1[Available Offers]
    D --> D2[Compare Offers]
    D --> D3[Accept Offer]
    D --> D4[Track Funding]

    E --> E1[Business Details]
    E --> E2[KYC Documents]
    E --> E3[Bank Details]
    E --> E4[Consent Settings]
    E --> E5[Free SME Access Plan]
```


## 8. Simple Pitch Slide Flow

```mermaid
flowchart LR
    A[SME Uploads Invoice] --> B[Settle It Verifies]
    B --> C[Buyer Confirms]
    C --> D[Institution Reviews & Offers]
    D --> E[SME Gets Funded]
```

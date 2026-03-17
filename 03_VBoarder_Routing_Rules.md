# 🛣️ VBoarder Inc. — Intake Routing & Processing Rules
## Version 3.0 | Updated January 2026

---

## Quick Routing Guide

When files are dropped into the system, route according to these rules.

---

## ROUTING BY DOCUMENT TYPE

### 1️⃣ CLIENT COMMUNICATIONS & PARTNERSHIPS

**Examples:** Emails from clients, partnership inquiries, meeting notes, proposals

**Routing:**
- **Primary:** Tara (CTO) — Technical validation
- **Secondary:** Money Penny — Scheduling
- **Tertiary:** Maya (CMO) — Brand check
- **Final:** Lori (CEO) — Partnership approval if >$50K

**Priority:** 🟠 HIGH (24-48 hours)

**Archive:** `D:\02_SOFTWARE\PRODUCTION\projects\ClientPartnerships\`

---

### 2️⃣ TECHNICAL DOCUMENTS & ARCHITECTURE

**Examples:** System diagrams, specs, code docs, API documentation

**Routing:**
- **Primary:** Tara (CTO) — Technical review
- **Secondary:** Omar (COO) — Operations impact
- **Tertiary:** Eric — Strategic tech decisions

**Priority:** 🟡 MEDIUM (48-72 hours)

**Archive:** `D:\02_SOFTWARE\PRODUCTION\projects\TechnicalDocs\`

---

### 3️⃣ EXECUTIVE & STRATEGIC ITEMS

**Examples:** CEO reports, strategic plans, board materials, major decisions

**Routing:**
- **Primary:** Lori (CEO) — Executive authority
- **Secondary:** Money Penny — Documentation
- **Tertiary:** All agents — Awareness

**Priority:** 🔴 URGENT (same-day review)

**Archive:** `D:\02_SOFTWARE\PRODUCTION\projects\Executive\`

---

### 4️⃣ BUDGET & FINANCIAL DOCUMENTS

**Examples:** Budget requests, expense reports, financial proposals

**Routing:**
- **Primary:** Finn (CFO) — Financial authority
- **Escalate:** Lori (CEO) if >$50K

**Spending Thresholds:**
| Amount | Approver | Timeline |
|--------|----------|----------|
| <$1K | Department Agent | Same day |
| $1K-$50K | Finn (CFO) | 24 hours |
| >$50K | Lori (CEO) + Finn | 48 hours |
| >$100K | Board | 1 week |

**Priority:** 🟠 HIGH (24 hours)

**Archive:** `D:\02_SOFTWARE\PRODUCTION\projects\Finance\`

---

### 5️⃣ LEGAL & CONTRACT DOCUMENTS

**Examples:** Contracts, agreements, legal notices, NDAs

**Routing:**
- **Primary:** Luca (CLO) — Legal review
- **Secondary:** Finn (CFO) — Financial terms
- **Final:** Lori (CEO) — Approval if >$50K

**Priority:** 🟠 HIGH (48-72 hours)

**Archive:** `D:\02_SOFTWARE\PRODUCTION\projects\Legal\`

**⚠️ CURRENT URGENT:** Legal report due Monday Jan 5, 2026 @ 12:00 PM

---

### 6️⃣ HUMAN RESOURCES & PERSONNEL

**Examples:** Employee docs, hiring requests, leave requests

**Routing:**
- **Primary:** Money Penny — Admin processing
- **Secondary:** Department head — Manager review
- **Final:** Lori (CEO) — Major changes

**Priority:** 🟡 MEDIUM (24-48 hours)

**Archive:** `D:\02_SOFTWARE\PRODUCTION\projects\Personnel\`

---

### 7️⃣ OPERATIONS & PROCESS DOCUMENTS

**Examples:** Process improvements, SOPs, workflow docs

**Routing:**
- **Primary:** Omar (COO) — Operations authority
- **Secondary:** Finn (CFO) — Budget impact

**Priority:** 🟡 MEDIUM (48 hours)

**Archive:** `D:\02_SOFTWARE\PRODUCTION\projects\Operations\`

---

### 8️⃣ MARKETING & COMMUNICATIONS

**Examples:** Campaign proposals, brand materials, PR content

**Routing:**
- **Primary:** Maya (CMO) — Marketing authority
- **Secondary:** Money Penny — Scheduling
- **Final:** Lori (CEO) — Strategic alignment

**Priority:** 🟡 MEDIUM (24-48 hours)

**Archive:** `D:\02_SOFTWARE\PRODUCTION\projects\Marketing\`

---

### 9️⃣ SPAM & REJECTED

**Examples:** Junk mail, duplicates, obsolete files

**Routing:** Auto-reject

**Archive:** `D:\_ARCHIVE\Rejected\`

---

## ROUTING DECISION TREE

```
📥 File received
    ↓
🔍 Spam check
    ├─ YES → Reject & archive
    └─ NO → Continue
    ↓
📂 Classify by type:
    ├─ Client/Partnership → Tara + Money Penny
    ├─ Technical → Tara + Omar
    ├─ Executive → Lori + Money Penny
    ├─ Financial → Finn
    ├─ Legal → Luca + Finn
    ├─ HR → Money Penny + Manager
    ├─ Operations → Omar
    ├─ Marketing → Maya
    └─ Unknown → Money Penny for routing
    ↓
⚡ Set priority:
    ├─ Executive → URGENT (4 hours)
    ├─ Financial >$50K → HIGH (24 hours)
    ├─ Client → HIGH (24-48 hours)
    ├─ Technical/Legal → MEDIUM (48-72 hours)
    └─ Other → STANDARD (72 hours)
    ↓
📋 Generate action items
    ↓
📤 Route to agent inbox
    ↓
💾 Archive with metadata
    ↓
✅ Log for compliance
```

---

## RESPONSE TIME SLA

| Priority | Target | Max | Escalation |
|----------|--------|-----|------------|
| 🔴 URGENT | 2 hrs | 4 hrs | After 2 hrs |
| 🟠 HIGH | 4 hrs | 24 hrs | After 24 hrs |
| 🟡 MEDIUM | 8 hrs | 48 hrs | After 48 hrs |
| ⚪ STANDARD | 24 hrs | 72 hrs | After 72 hrs |

---

## FILE LOCATIONS

### Active Agent Folders
```
D:\02_SOFTWARE\PRODUCTION\AGENTS\
├── ADMIN_EXEC_MONEYPENNY_v1.0\inbox\  ← Money Penny
├── offices\CFO\inbox\                  ← Finn
├── offices\CLO\inbox\                  ← Luca
├── offices\COO\inbox\                  ← Omar
├── offices\CMO\inbox\                  ← Maya
├── offices\CSO\inbox\                  ← Sage
├── offices\CTO\inbox\                  ← Tara
└── offices\AIR\inbox\                  ← AIR
```

### Pending Migration (Legacy)
```
D:\_ARCHIVE\2026-01_NAVIMIGRATE\VBoarder_NAVIMIGRATE\offices\
├── CFO\inbox\   (3,938 files)
├── CLO\inbox\   (1,892 files) ⚠️ URGENT
├── COO\inbox\   (5,341 files)
├── CMO\inbox\   (312 files)
├── CSO\inbox\   (9 files)
├── CTO\inbox\   (1,147 files)
├── EXEC\inbox\  (2,659 files)
└── AIR\inbox\   (empty)
```

---

## ESCALATION CHAIN

### Technical Issues
Eric → Tara → Omar

### Financial Issues
Finn → Lori → Board

### Legal Issues
Luca → Lori → Outside Counsel

### Administrative
Money Penny → Eric → Lori

---

## BLOCKING ITEMS

If item blocked >24 hours:
1. Auto-escalate to next level
2. Log in compliance system
3. Notify Eric via Money Penny
4. Document reason for delay

---

**Routing Rules Version:** VBoarder v3.0
**Effective Date:** January 3, 2026
**Maintained By:** NAVI + Money Penny

---

*All incoming files routed per these rules. Exceptions require Eric approval.*

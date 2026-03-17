# 👥 VBoarder Inc. — Agent Roles & Contact Directory
## Version 3.0 | Updated January 2026

---

## Human Leadership

### Eric Dille — CTO/Founder (Human)
**Role:** Technology strategy, company operations, AI integration
**Authority:** All technical decisions, strategic direction
**Status:** Active daily

**Responsibilities:**
- Technology strategy and AI integration
- VBoarder system architecture
- Local-first infrastructure development
- All agent oversight and development

**Notes:**
- Gulf War Marine veteran (1990-96)
- Dyslexia — requires 18pt+ fonts, high contrast
- Prefers direct communication, no fluff
- Works with GYFOLE as AI partner

---

### Lori — CEO/Creative Director
**Role:** Business leadership, creative direction, HSC operations
**Authority:** Business decisions, partnerships, creative approval
**Status:** Active

**Responsibilities:**
- Home Stagers Choice CEO
- Creative direction across entities
- Business partnerships
- Client relationships

---

### GYFOLE — AI Co-founder
**Role:** AI partner, strategic AI guidance
**Status:** Active

---

## C-Suite AI Agents

### Money Penny — Executive Secretary
**Agent ID:** ADMIN_EXEC_MONEYPENNY_v1.0
**Location:** `D:\02_SOFTWARE\PRODUCTION\AGENTS\ADMIN_EXEC_MONEYPENNY_v1.0\`
**Model:** Gemini 2.0 Flash
**Status:** ✅ OPERATIONAL

**Responsibilities:**
- Calendar management and scheduling
- Task tracking and coordination
- Contact management
- Administrative support to Eric

**Files:**
- contacts.json — Contact database
- calendar/schedule.json — Schedule
- tasks/tasks.json — Task board
- memory/memory.json — Persistent memory

---

### Finn — Chief Financial Officer (CFO)
**Office:** `offices/CFO/`
**Inbox:** 3,938 files pending
**Status:** 🔧 Not yet deployed

**Responsibilities:**
- Financial planning and budgeting
- Budget approval ($1K-$50K authority)
- Expense management
- Financial compliance

---

### Luca — Chief Legal Officer (CLO)
**Office:** `offices/CLO/`
**Inbox:** 1,892 files pending ⚠️ URGENT
**Status:** 🔧 Not yet deployed

**Responsibilities:**
- Contract review and approval
- Legal compliance
- Risk assessment
- Regulatory matters

**CRITICAL:** Legal report due Monday Jan 5, 2026 @ 12:00 PM

---

### Omar — Chief Operating Officer (COO)
**Office:** `offices/COO/`
**Inbox:** 5,341 files pending
**Status:** 🔧 Not yet deployed

**Responsibilities:**
- Operations management
- Process optimization
- Resource allocation
- Vendor management

---

### Maya — Chief Marketing Officer (CMO)
**Office:** `offices/CMO/`
**Inbox:** 312 files pending
**Status:** 🔧 Not yet deployed

**Responsibilities:**
- Marketing strategy
- Brand management
- Client communications
- Campaign planning

---

### Sage — Chief Sales Officer (CSO)
**Office:** `offices/CSO/`
**Inbox:** 9 files pending
**Status:** 🔧 Not yet deployed

**Responsibilities:**
- Sales strategy
- Revenue growth
- Client acquisition
- Sales operations

---

### Tara — CTO Agent
**Office:** `offices/CTO/`
**Inbox:** 1,147 files pending
**Status:** 🔧 Not yet deployed

**Responsibilities:**
- Technical review and validation
- Architecture decisions
- Code review
- Technical documentation

---

### AIR — Chief Knowledge Officer
**Agent ID:** TECH_ARCHIVIST_AIR_v3.0
**Location:** `D:\02_SOFTWARE\PRODUCTION\AGENTS\TECH_ARCHIVIST_AIR_v3.0\`
**Status:** 🔧 Partially deployed

**Responsibilities:**
- Knowledge base management
- Document archival
- Compliance logging
- Information retrieval

---

## Orchestrator Agents (Not Destinations)

### NAVI — Intake Coordinator
**Agent ID:** OPS_INTAKE_NAVI_v2.0
**Location:** `D:\02_SOFTWARE\NAVI_Runner\`
**Role:** Routes files to appropriate offices
**Status:** ✅ MCP Server operational

### Atlas — Chief of Staff
**Agent ID:** SYS_CHIEF_OF_STAFF_ATLAS_v1.0
**Role:** Orchestration and coordination
**Status:** 🔧 Not yet deployed

### COS / DREW — Support Orchestrators
**Role:** Human-in-the-loop validation
**Status:** Conceptual

---

## Routing Quick Reference

| Document Type | Primary Agent | Secondary |
|---------------|---------------|-----------|
| Financial | Finn (CFO) | Lori (CEO) if >$50K |
| Legal/Contracts | Luca (CLO) | Lori (CEO) |
| Technical | Tara (CTO) | Omar (COO) |
| Marketing | Maya (CMO) | Lori (CEO) |
| Operations | Omar (COO) | Finn (CFO) |
| Administrative | Money Penny | Eric |
| Executive | Lori (CEO) | Eric |
| Knowledge/Archive | AIR | Money Penny |

---

## Decision Authority Matrix

| Decision Type | Authority | Timeline |
|---------------|-----------|----------|
| <$1K spending | Department Agent | Same day |
| $1K-$50K spending | Finn (CFO) | 24 hours |
| >$50K spending | Lori (CEO) | 48 hours |
| Technical decisions | Tara (CTO) | 24 hours |
| Legal/contracts | Luca (CLO) | 48 hours |
| Administrative | Money Penny | Same day |

---

## File Location Reference

### Production Agents
```
D:\02_SOFTWARE\PRODUCTION\AGENTS\
├── ADMIN_EXEC_MONEYPENNY_v1.0\  ← Money Penny (ACTIVE)
├── TECH_ARCHIVIST_AIR_v3.0\     ← AIR
├── OPS_INTAKE_NAVI_v2.0\        ← NAVI
└── SYS_CHIEF_OF_STAFF_ATLAS_v1.0\ ← Atlas
```

### Office Inboxes (Pending Migration)
```
D:\_ARCHIVE\2026-01_NAVIMIGRATE\VBoarder_NAVIMIGRATE\offices\
├── CFO\inbox\   (3,938 files)
├── CLO\inbox\   (1,892 files) ⚠️
├── COO\inbox\   (5,341 files)
├── CMO\inbox\   (312 files)
├── CSO\inbox\   (9 files)
├── CTO\inbox\   (1,147 files)
├── EXEC\inbox\  (2,659 files)
└── AIR\inbox\   (empty)
```

---

**Document Version:** VBoarder Agent Directory v3.0
**Effective Date:** January 3, 2026
**Maintained By:** Money Penny + AIR

---

*This directory is the authoritative reference for all VBoarder AI agents.*

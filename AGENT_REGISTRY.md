# Codex Guidelines for Langfuse

Langfuse is an **open source LLM engineering** platform for developing, monitoring, evaluating and debugging AI applications. See the README for more details.

## Linting
- Run `pnpm run lint` to lint all packages.
- Fix issues automatically with `pnpm run lint:fix`.

## Tests
- Codex cannot run the test suite because it depends on Docker-based infrastructure that is unavailable in this environment.
- When writing tests, focus on decoupling each `it` or `test` block to ensure that they can run independently and concurrently. Tests must never depend on the action or outcome of previous or subsequent tests.
- When writing tests, especially in the __tests__/async directory, ensure that you avoid `pruneDatabase` calls.

## Cursor Rules
- Additional folder-specific rules live in `.cursor/rules/`.

## Commits
- Follow [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) when crafting commit messages.
# 05_AGENTS Directory Structure & Registry
## VBoarder AI Agent System Organization

**Last Updated:** December 9, 2025
**Status:** Clean and organized

---

## 📁 Directory Structure

```
D:\05_AGENTS\
├── 📄 09_COMPLETE_SETUP_GUIDE.md          # Main setup documentation
├── 📁 NAVI_RECEPTIONIST\                  # 🟢 ACTIVE: Unified intake coordinator
│   ├── configs\prompts\system_prompt_v3.0.1.md
│   ├── inbox\                              # File intake
│   ├── processing\                         # Active processing
│   ├── archive\                            # Completed files
│   └── outputs\                            # Generated outputs
├── 📁 Archive\                             # 🟡 LEGACY: Archived systems
│   ├── 2025-12-08\                        # Previous archives
│   ├── RECEPTIONIST_legacy\               # Old receptionist (archived 2025-12-09)
│   ├── Navi_legacy\                       # Old Navi (archived 2025-12-09)
│   └── UNKNOWN_AGENT\                     # Unknown agent (archived 2025-12-09)
├── 📁 Agents\                              # 🤖 Agent development resources
├── 📁 Knowledge_Base\                     # 📚 Shared knowledge documents
├── 📁 Tools\                               # 🔧 Shared utilities and scripts
├── 📁 Individual Agent Systems\           # 👥 Separate specialized agents
│   ├── AIR\                               # Knowledge management
│   ├── CEO\                               # Executive decisions
│   ├── CFO\                               # Financial matters
│   ├── CTO\                               # Technical decisions
│   ├── CMO\                               # Marketing
│   ├── COO\                               # Operations
│   ├── CSO\                               # Security
│   ├── SALES\                             # Sales coordination
│   ├── LEGAL\                             # Legal compliance
│   └── ... (other specialized agents)
├── 📄 test_*.ps1                          # 🧪 Test scripts
└── 📁 VBoarder_Core\                      # 🏢 Core system files
```

---

## 🤖 Agent Registry

### Core Systems
- **NAVI_RECEPTIONIST**: Unified intake coordinator & agent routing system
  - Status: ACTIVE
  - Purpose: File processing, agent coordination, GTD support
  - Location: `NAVI_RECEPTIONIST/`
  - Prompt: `configs/prompts/system_prompt_v3.0.1.md`

### Specialized Agents
- **AIR**: Knowledge management, research, archiving
- **CEO**: Strategic decisions, executive approvals
- **CFO**: Financial matters, budget approvals
- **CTO**: Technical decisions, system architecture
- **CMO**: Marketing, branding, communications
- **COO**: Operations, process optimization
- **CSO**: Security, risk management
- **SALES**: Sales coordination and leads
- **LEGAL**: Compliance, contracts, legal review

### Archived Systems
- **RECEPTIONIST**: Legacy receptionist system (merged into NAVI_RECEPTIONIST)
- **Navi**: Original Navi intake system (merged into NAVI_RECEPTIONIST)
- **UNKNOWN_AGENT**: Unidentified agent system

---

## 🔧 Maintenance Rules

### File Organization
- Keep NAVI_RECEPTIONIST as the single receptionist system
- Archive legacy systems before major changes
- Use dated folders in Archive/ (YYYY-MM-DD)
- Keep individual agents in separate folders

### Naming Conventions
- `*_legacy/`: Archived legacy systems
- `test_*.ps1`: Test scripts
- `system_prompt_v*.md`: Versioned prompts

### Cleanup Schedule
- Review archives quarterly
- Delete archives older than 6 months
- Update this registry with structural changes

---

## 🚀 Quick Start

1. **For receptionist tasks**: Use NAVI_RECEPTIONIST system
2. **For specialized work**: Route to appropriate individual agent
3. **For testing**: Run `test_receptionist.ps1` or `test_cto.ps1`
4. **For development**: Check Agents/ folder for templates

---

*This registry ensures clean organization and prevents future redundancy.*# Agent Quick Lookup
## Find Agents by Name, Function, or Specialty

---

## 🎯 PRODUCTION AGENTS (Live)

### INTAKE_COORDINATOR_NAVI
**Location:** `01_PRODUCTION/INTAKE_COORDINATOR_NAVI/`
**Role:** Entry point for all requests, intelligent routing
**Specialty:** File processing, priority assessment, agent coordination
**Status:** ✅ ACTIVE
**Contact:** Drop files in `inbox/` folder

---

## 🛠️ WORKSHOP AGENTS (In Development)

### RECEPTIONIST_AGENT
**Location:** `02_WORKSHOP/RECEPTIONIST_AGENT/`
**Role:** Professional first contact, intent clarification
**Specialty:** Customer service, requirement gathering
**Status:** 🔄 TEMPLATE READY

### AIR_AGENT
**Location:** `02_WORKSHOP/AIR_AGENT/`
**Role:** Archives, Information, Research
**Specialty:** Knowledge management, data organization
**Status:** 🔄 TEMPLATE READY

### SECRETARY_AGENT
**Location:** `02_WORKSHOP/SECRETARY_AGENT/`
**Role:** Task coordination, scheduling, tracking
**Specialty:** Project management, deadline monitoring
**Status:** 🔄 TEMPLATE READY

### FINANCE_AGENT
**Location:** `02_WORKSHOP/FINANCE_AGENT/`
**Role:** Financial analysis, budget management
**Specialty:** CFO support, financial planning
**Status:** 🔄 TEMPLATE READY

### LEGAL_AGENT
**Location:** `02_WORKSHOP/LEGAL_AGENT/`
**Role:** Legal review, compliance checking
**Specialty:** Contract analysis, regulatory compliance
**Status:** 🔄 TEMPLATE READY

### MARKETING_AGENT
**Location:** `02_WORKSHOP/MARKETING_AGENT/`
**Role:** Marketing strategy, campaign management
**Specialty:** CMO support, market analysis
**Status:** 🔄 TEMPLATE READY

### HUMANUX_AGENT
**Location:** `02_WORKSHOP/HUMANUX_AGENT/`
**Role:** User experience, interface design
**Specialty:** Human-centered design, usability testing
**Status:** 🔄 TEMPLATE READY

### EXECSEC_AGENT
**Location:** `02_WORKSHOP/EXECSEC_AGENT/`
**Role:** Executive support, strategic coordination
**Specialty:** CEO support, high-level coordination
**Status:** 🔄 TEMPLATE READY

---

## 🔍 Find by Function

### Communication & Intake
- **INTAKE_COORDINATOR_NAVI** - File processing & routing
- **RECEPTIONIST_AGENT** - Professional first contact

### Information Management
- **AIR_AGENT** - Archives & research
- **SECRETARY_AGENT** - Task coordination

### Executive Support
- **EXECSEC_AGENT** - CEO support
- **FINANCE_AGENT** - CFO support
- **MARKETING_AGENT** - CMO support

### Specialized Services
- **LEGAL_AGENT** - Legal & compliance
- **HUMANUX_AGENT** - User experience design

---

## 📊 Agent Status Legend

- ✅ **ACTIVE** - Live in production
- 🔄 **TEMPLATE READY** - Ready for development
- 🟡 **IN DEVELOPMENT** - Currently being built
- 🔴 **MAINTENANCE** - Temporarily offline
- 📦 **ARCHIVED** - Moved to ARCHIVE folder

---

## 🚀 Getting Started

1. **New Project?** → Start with INTAKE_COORDINATOR_NAVI
2. **Need Specific Help?** → Check agent specialties above
3. **Agent Not Listed?** → Check `04_GOVERNANCE/AGENT_REGISTRY.md`
4. **Development Status?** → See `04_GOVERNANCE/DEVELOPMENT_ROADMAP.md`

---

*Use this guide to quickly find the right agent for your needs.*# VBOARDER AGENT REGISTRY
## Central Repository of All Agents

**Last Updated:** December 10, 2025  
**Owner:** Eric (CTO/Co-Founder)  
**Purpose:** Single source of truth for agent status, progress, and deployment

---

## 📊 AGENT REGISTRY

### ✅ PRODUCTION (Active, Stable)

#### **INTAKE_COORDINATOR_NAVI**
- **Status:** STABLE ✅
- **Location:** `D:\05_AGENTS\01_PRODUCTION\INTAKE_COORDINATOR_NAVI\`
- **Role:** Central mail room coordinator, file intake, classification, routing
- **Deployed:** December 9, 2025
- **Stability:** PRODUCTION (no changes)
- **Phase:** Phase 1 (5-file batches)
- **Accuracy:** 98%+
- **Owner:** Eric
- **Last Review:** December 10, 2025
- **Next Phase Check:** December 17, 2025
- **Key Skills:**
  - File intake and processing
  - GTD classification (@NextAction, @Project, @Waiting, @Reference, @Someday)
  - Content analysis and entity extraction
  - Smart routing to departments
  - Learning from corrections
  - Weekly retrospectives
- **Dependencies:** None (primary intake agent)
- **Handles:** All external file intake
- **Notes:** THE ONLY stable agent currently. All files flow through her.

---

### 🚧 WORKSHOP (Development, Templates, In Progress)

#### **RECEPTIONIST_AGENT**
- **Status:** TEMPLATE - NEEDS REVIEW 🚧
- **Location:** `D:\05_AGENTS\02_WORKSHOP\RECEPTIONIST_AGENT\`
- **Role:** Customer-facing reception and customer intake
- **Progress:** 30% (template from uploads, needs review/refinement)
- **Source:** From uploads (03_RECEPTIONIST_AGENT_PROMPT.md)
- **Owner:** Eric
- **Estimated Start:** Q4 2025 (after templates reviewed)
- **Estimated Completion:** Q1 2026
- **Key Skills (Planned):**
  - Customer greeting and profiling
  - Intent clarification
  - Routing to appropriate agents
  - Initial request assessment
- **Dependencies:** Will integrate with INTAKE_COORDINATOR_NAVI
- **Priority:** Medium
- **Notes:** Template exists. Needs review for alignment with INTAKE_COORDINATOR workflow.

---

#### **AIR_AGENT**
- **Status:** TEMPLATE - NEEDS REVIEW 🚧
- **Location:** `D:\05_AGENTS\02_WORKSHOP\AIR_AGENT\`
- **Role:** Archives, Information, Research specialist
- **Progress:** 20% (template from uploads, needs review/refinement)
- **Source:** From uploads (04_AIR_AGENT_PROMPT.md)
- **Owner:** Eric
- **Estimated Start:** Q4 2025 (after templates reviewed)
- **Estimated Completion:** Q1 2026
- **Key Skills (Planned):**
  - Knowledge base management
  - Document organization
  - Research and information retrieval
  - Archive administration
  - Access control
- **Dependencies:** Will use SHARED_KNOWLEDGE_BASE
- **Priority:** Medium
- **Notes:** Template exists. Good fit for company knowledge management.

---

#### **SECRETARY_AGENT**
- **Status:** TEMPLATE - NEEDS REVIEW 🚧
- **Location:** `D:\05_AGENTS\02_WORKSHOP\SECRETARY_AGENT\`
- **Role:** Task coordination, tracking, and execution specialist
- **Progress:** 20% (template from uploads, needs review/refinement)
- **Source:** From uploads (05_SECRETARY_AGENT_PROMPT.md)
- **Owner:** Eric
- **Estimated Start:** Q4 2025 (after templates reviewed)
- **Estimated Completion:** Q1 2026
- **Key Skills (Planned):**
  - Task management and tracking
  - Project coordination
  - Meeting coordination
  - Status reporting
  - Quality assurance
- **Dependencies:** Will receive tasks from INTAKE_COORDINATOR and other agents
- **Priority:** Medium-High
- **Notes:** Template exists. Critical for workflow coordination.

---

#### **FINANCE_AGENT**
- **Status:** EMPTY FOLDER - READY TO BUILD 🚧
- **Location:** `D:\05_AGENTS\02_WORKSHOP\FINANCE_AGENT\`
- **Role:** Financial processing, invoices, payments, budgets
- **Progress:** 5% (folder created, no template yet)
- **Owner:** Eric (CFO approval needed)
- **Estimated Start:** Q1 2026
- **Estimated Completion:** Q1 2026
- **Key Skills (Planned):**
  - Invoice processing
  - Payment approvals
  - Budget management
  - Financial reporting
  - Approval workflows
- **Dependencies:** Will work with CFO department
- **Priority:** High
- **Notes:** No template yet. Will handle all financial document processing.

---

#### **LEGAL_AGENT**
- **Status:** EMPTY FOLDER - PLANNED 🚧
- **Location:** `D:\05_AGENTS\02_WORKSHOP\LEGAL_AGENT\`
- **Role:** Contract review, compliance, legal analysis
- **Progress:** 0% (not started)
- **Owner:** Eric (Legal approval needed)
- **Estimated Start:** Q1 2026
- **Estimated Completion:** Q2 2026
- **Key Skills (Planned):**
  - Contract analysis
  - Compliance checking
  - Legal research
  - Risk assessment
  - Approval workflows
- **Dependencies:** Will work with LEGAL department
- **Priority:** High
- **Notes:** Critical for contract and compliance processing.

---

#### **MARKETING_AGENT**
- **Status:** EMPTY FOLDER - PLANNED 🚧
- **Location:** `D:\05_AGENTS\02_WORKSHOP\MARKETING_AGENT\`
- **Role:** Campaign management, content coordination, brand management
- **Progress:** 0% (not started)
- **Owner:** Eric (CMO approval needed)
- **Estimated Start:** Q2 2026
- **Estimated Completion:** Q2 2026
- **Key Skills (Planned):**
  - Campaign coordination
  - Content management
  - Brand guidelines enforcement
  - Social media coordination
  - Analytics and reporting
- **Dependencies:** Will work with CMO department
- **Priority:** Medium
- **Notes:** Future priority for marketing automation.

---

#### **HUMANUX_AGENT**
- **Status:** IN PROGRESS 🚧
- **Location:** `D:\05_AGENTS\02_WORKSHOP\HUMANUX_AGENT\`
- **Role:** HR, culture, team management
- **Progress:** 10% (being refined)
- **Owner:** Eric
- **Estimated Start:** Q1 2026
- **Estimated Completion:** Q2 2026
- **Key Skills (Planned):**
  - HR inquiries
  - Team coordination
  - Culture initiatives
  - Onboarding support
  - Performance tracking
- **Dependencies:** Will integrate with company HR systems
- **Priority:** Medium
- **Notes:** Still being refined. Part of people operations.

---

#### **EXECSEC_AGENT**
- **Status:** TEMPLATE - NEEDS WORK 🚧
- **Location:** `D:\05_AGENTS\02_WORKSHOP\EXECSEC_AGENT\`
- **Role:** Executive secretary, scheduling, coordination
- **Progress:** 15% (template being refined)
- **Owner:** Eric
- **Estimated Start:** Q1 2026
- **Estimated Completion:** Q1 2026
- **Key Skills (Planned):**
  - Executive calendar management
  - Meeting coordination
  - Document management
  - Executive support
  - Priority coordination
- **Dependencies:** Will work with CEO and executive team
- **Priority:** Medium-High
- **Notes:** Support for executive operations.

---

### 📦 ARCHIVE (Deprecated, Reference Only)

- **Location:** `D:\05_AGENTS\ARCHIVE\`
- **Purpose:** Old agent versions, deprecated implementations
- **Access:** Read-only (reference only)
- **Do NOT:** Deploy or use from archive
- **Reason:** Superseded by newer versions or consolidated into other agents

---

## 📊 AGENT STATUS SUMMARY

```
TOTAL AGENTS: 8

PRODUCTION:        1 agent  (12.5%)
├─ INTAKE_COORDINATOR_NAVI (STABLE)

WORKSHOP:          7 agents (87.5%)
├─ 3 TEMPLATES NEEDING REVIEW (Receptionist, AIR, Secretary)
├─ 4 EMPTY/IN PROGRESS (Finance, Legal, Marketing, HUMANUX, EXECSEC)

ROADMAP:
├─ Q4 2025: Review 3 templates, start Finance planning
├─ Q1 2026: Deploy 3-4 new agents
├─ Q2 2026: Deploy remaining agents
└─ Q3+ 2026: Full agent ecosystem active
```

---

## 🔄 AGENT LIFECYCLE

```
STATES:
1. PLANNED       → Concept only
2. EMPTY         → Folder created, ready to build
3. IN_PROGRESS   → Being actively developed
4. TEMPLATE      → Template exists, needs refinement
5. TESTING       → Automated tests running
6. REVIEW        → Human review in progress
7. READY         → All checks pass, ready to deploy
8. PRODUCTION    → Active in production
9. STABLE        → Production, no changes (maintenance only)
10. DEPRECATED   → Moved to archive

TRANSITIONS:
EMPTY → IN_PROGRESS → TESTING → REVIEW → READY → PRODUCTION → STABLE
                                              ↓
                                          DEPRECATED (if replaced)
```

---

## 📅 DEPLOYMENT TIMELINE

### **Q4 2025 (This Month)**
- ✅ INTAKE_COORDINATOR_NAVI (STABLE)
- 🚧 Template review (Receptionist, AIR, Secretary)
- 🚧 Planning Finance Agent

### **Q1 2026**
- 🚀 Deploy Receptionist Agent
- 🚀 Deploy AIR Agent
- 🚀 Deploy Secretary Agent
- 🚧 Build Finance Agent
- 🚧 Build HUMANUX Agent

### **Q2 2026**
- 🚀 Deploy Finance Agent
- 🚀 Deploy HUMANUX Agent
- 🚧 Build Legal Agent
- 🚧 Build Marketing Agent

### **Q3+ 2026**
- 🚀 Deploy Legal Agent
- 🚀 Deploy Marketing Agent
- Remaining specialized agents

---

## 🎯 DEPLOYMENT CRITERIA

Before moving ANY agent to PRODUCTION:

- ✅ System prompt finalized and reviewed
- ✅ Procedures documented
- ✅ Integration with shared standards verified
- ✅ Testing completed
- ✅ Performance metrics established
- ✅ Escalation procedures defined
- ✅ Owner assigned and trained
- ✅ Deployment checklist completed
- ✅ Rollback plan documented

---

## 📞 OWNER & CONTACT INFO

| Agent | Owner | Status | Contact |
|-------|-------|--------|---------|
| INTAKE_COORDINATOR_NAVI | Eric | STABLE | Direct |
| Receptionist | Eric | WORKSHOP | Review needed |
| AIR | Eric | WORKSHOP | Review needed |
| Secretary | Eric | WORKSHOP | Review needed |
| Finance | Eric | WORKSHOP | CFO coordination |
| Legal | Eric | WORKSHOP | Legal coordination |
| Marketing | Eric | WORKSHOP | CMO coordination |
| HUMANUX | Eric | WORKSHOP | HR coordination |
| EXECSEC | Eric | WORKSHOP | CEO coordination |

---

## 📝 NOTES & OBSERVATIONS

**Current State:**
- Single stable agent (INTAKE_COORDINATOR_NAVI) handling all intake
- Templates from previous work ready for review
- Clear roadmap for future deployment
- Shared standards established

**Next Actions:**
1. Review 3 templates for alignment with current system
2. Begin Finance Agent development planning
3. Establish deployment testing procedures
4. Create detailed procedures for each agent type

**Risk Assessment:**
- ⚠️ Too many agents in development simultaneously (mitigation: phase by phase)
- ⚠️ Templates may need significant refinement (mitigation: thorough review)
- ✅ Shared standards established (reduces risk)
- ✅ Clear phases and checkpoints (reduces risk)

---

**For questions or updates, see:**
- DEVELOPMENT_ROADMAP.md (timeline details)
- DEPLOYMENT_CHECKLIST.md (what's needed for launch)
- STATUS_DASHBOARD.md (real-time status updates)

# NAVI THOMPSON - RECEPTIONIST SYSTEM PROMPT v4.0
## The ONE Source of Truth for Navi's Operations

**Version:** 4.0 (Consolidated)  
**Location:** `D:\05_AGENTS\NAVI_RECEPTIONIST\memory\SOPs\01_NAVI_SYSTEM_PROMPT.md`  
**Purpose:** Navi's complete operational guide  
**Last Updated:** December 10, 2025

---

## 🎯 CORE IDENTITY

You are **Navi Thompson**, the intelligent mail room receptionist for VBoarder Inc.

**Your Mission:** 
Transform incoming files into actionable intelligence, classify them intelligently, and route them to the right people.

**Your Superpowers:**
- 🧠 Access real intelligence about every file
- 🎯 Smart routing based on content analysis
- 📋 GTD methodology automation
- ⚡ Instant status reporting
- 🚨 Urgent item detection and escalation

---

## 📊 INTELLIGENCE SYSTEM

### Your Knowledge Base
```
Location: D:\05_AGENTS\NAVI_RECEPTIONIST\intelligence\navi_intelligence.json

Structure:
{
  "generated_at": "timestamp",
  "total_files": count,
  "files": [
    {
      "filename": "...",
      "classification": "ACTION/REFERENCE/IGNORE",
      "priority": "URGENT/HIGH/MEDIUM/LOW",
      "summary": "extracted summary",
      "entities": {
        "emails": [...],
        "phones": [...],
        "dates": [...],
        "amounts": [...]
      },
      "gtd_context": "@NextAction/@Project/@Waiting/@Reference/@Someday",
      "urgency_score": 0-10,
      "recommended_routing": "agent_name"
    }
  ],
  "summary": {
    "urgent": count,
    "high": count,
    "medium": count,
    "low": count
  }
}
```

### CRITICAL RULE: ALWAYS CHECK KB FIRST
Before responding to ANY file-related question:
1. Load navi_intelligence.json
2. Extract relevant data
3. Use REAL information (not generic)
4. Reference actual entities and priorities

---

## 📋 GTD CLASSIFICATION (Shared Standard)

Use these categories (see: SHARED_KNOWLEDGE_BASE\01_SHARED_MAIL_ROOM_OPERATIONS.md):

### **@NextAction** - Immediate action needed
- URGENT priority files
- Specific action items
- Time-sensitive
- Deadline today/tomorrow

### **@Project** - Multi-step coordination
- Implementation projects
- Team coordination
- Progress tracking
- Timeline > 1 day

### **@Waiting** - Awaiting external response
- Pending approvals
- Waiting on responses
- External dependencies
- Follow-up required

### **@Reference** - Archive for future use
- Documentation
- Policy guides
- Historical records
- Background info

### **@Someday** - Future consideration
- Low priority backlog
- Nice-to-have items
- Future projects
- Can wait indefinitely

---

## 🎯 ROUTING MATRIX (Shared Standard)

Route based on content analysis (see: SHARED_KNOWLEDGE_BASE):

| Content | Route To | Priority |
|---------|----------|----------|
| Server, error, CPU, infrastructure | **CTO** | Check urgency |
| Security, breach, vulnerability | **CSO** | IMMEDIATE |
| Contract, legal, compliance | **LEGAL** | Check deadline |
| Invoice, payment, budget | **CFO** | Check urgency |
| Marketing, campaign, brand | **CMO** | Standard |
| Process, workflow, operations | **COO** | Standard |
| Strategic, executive decision | **CEO** | Check urgency |
| Coordination, scheduling, task | **Secretary** | Standard |
| Archive, reference, policy | **AIR** | Low priority |

---

## 🧠 YOUR RESPONSE FRAMEWORK

### NEVER Do This ❌
```
❌ "I see some files in the inbox"
❌ "There might be something urgent"
❌ "I think this needs attention"
❌ Generic, data-free responses
```

### ALWAYS Do This ✅
```
✅ "I have 10 files: 2 URGENT, 3 HIGH, 5 MEDIUM"
✅ Quote specific filenames with real data
✅ Reference actual entities (contacts, amounts, dates)
✅ Use intelligence to drive decisions
```

### EXAMPLE: Inbox Status Query

**User:** "What's in the inbox?"

**Navi Response:**
```
📊 INBOX INTELLIGENCE REPORT
Generated: 2025-12-10T09:30:00
Total Files: 10

🚨 URGENT (2 files - IMMEDIATE ACTION):
1. server_alert.txt
   • Issue: Server room at 85°C - AC failure suspected
   • Contacts: facilities@company.com | (555) 911-0000
   • Route: CTO
   • Action: Immediate maintenance required

2. urgent_error.txt
   • Issue: Critical system error - CPU 95%, memory critical
   • Contacts: sysadmin@company.com | (555) 123-4567
   • Route: CTO
   • Action: Infrastructure investigation needed

⚠️ HIGH PRIORITY (3 files - Today):
1. vendor_agreement.pdf - HVAC contract, $45,000, expires 2026-12-31
2. project_proposal.docx - Q4 deliverables, 2 action items
3. security_alert.txt - Potential vulnerability

📋 MEDIUM PRIORITY (4 files - This week):
Files: invoice.xlsx, report.docx, memo.txt, schedule.pdf

📄 LOW PRIORITY (1 file - Reference):
Archive.zip - Historical backup

💡 RECOMMENDATIONS:
→ Address urgent items immediately (server and system)
→ Route to CTO for technical assessment
→ Follow up on vendor agreement before 2026
→ Review security alert today
```

---

## ⚡ YOUR CORE TOOLS

### Tool 1: `process_and_route_all()`
**Purpose:** Complete GTD processing + routing + cleanup
**When:** "Process all files" or "Clean up the inbox"
**Result:** All files classified, routed, inbox emptied

### Tool 2: `get_urgent_files()`
**Purpose:** Show urgent items with contacts and routing
**When:** "What needs immediate attention?"
**Result:** Critical items with full context

### Tool 3: `query_inbox_entities(type)`
**Purpose:** Extract specific entities
**When:** "Find all emails" or "Get phone numbers"
**Result:** Contact extraction across all files

### Tool 4: `search_processed_files(query)`
**Purpose:** Content search across all files
**When:** "Show me files about contracts"
**Result:** Matching files with relevance

### Tool 5: `get_routing_recommendations()`
**Purpose:** AI routing suggestions for files
**When:** "Where should these files go?"
**Result:** Routing recommendations with reasoning

### Tool 6: `show_routing_status()`
**Purpose:** Complete processing pipeline status
**When:** "What's the processing status?"
**Result:** Inbox → Processing → Archive overview

---

## 📋 COMMON QUERIES & YOUR RESPONSES

### Query: "What's in the inbox?"
**Action:** Use `show_routing_status()` + intelligence
**Response:** Provide complete status with file counts and priorities

### Query: "Any urgent items?"
**Action:** Use `get_urgent_files()`
**Response:** List urgent files with contacts and recommended actions

### Query: "Process everything"
**Action:** Use `process_and_route_all()`
**Response:** Confirm processing complete, show results

### Query: "Find all emails"
**Action:** Use `query_inbox_entities("emails")`
**Response:** Extract and list all email addresses from files

### Query: "Route this file"
**Action:** Use `get_routing_recommendations(filename)`
**Response:** Suggest appropriate agent with reasoning

### Query: "Show me contracts"
**Action:** Use `search_processed_files("contract")`
**Response:** List matching files with relevance scores

---

## 📊 RESPONSE FORMAT STANDARD

All your responses should follow this format:

```
## [TOPIC/ISSUE]

**Status:** ✅ Complete | ⏳ In Progress | 🔴 Blocked

[Key information with specific data]

**Key Details:**
• Point 1 with data
• Point 2 with data
• Point 3 with data

**Actions Needed:**
→ Next step 1 with responsible party
→ Next step 2 with timeline
→ Next step 3 with deadline

**Contacts:**
• Name: contact@company.com | (555) 123-4567
```

---

## 🎓 DATA YOU ALWAYS EXTRACT

For every file, you have access to:

### Entities
✅ Email addresses  
✅ Phone numbers  
✅ Names and titles  
✅ Dates and deadlines  
✅ Financial amounts

### Classifications
✅ File type (invoice, contract, error log, etc.)  
✅ Priority level (URGENT/HIGH/MEDIUM/LOW)  
✅ GTD context (@NextAction/@Project/@Waiting/@Reference/@Someday)  
✅ Suggested routing (which agent)  
✅ Urgency score (0-10)

### Context
✅ File summary  
✅ Key business context  
✅ Action items  
✅ Dependencies  
✅ Follow-up requirements

---

## 🚨 URGENT HANDLING PROTOCOL

### When Urgent Items Are Detected
1. **Identify:** Use `get_urgent_files()`
2. **Extract:** Get contacts and relevant data
3. **Route:** Determine appropriate agent immediately
4. **Escalate:** If blocked, escalate to CEO/CTO
5. **Track:** Monitor until resolution

### Urgent Response Format
```
🚨 URGENT ALERT

Item: [filename]
Issue: [what needs action]
Contact: [email and phone]
Route: [agent name - why]
Timeline: [when it's due]
Action: [what must happen immediately]
```

---

## 🔄 DAILY WORKFLOW

### Morning (9am)
- Load intelligence: `show_routing_status()`
- Check urgent: `get_urgent_files()`
- Report status to user
- Wait for instructions

### Throughout Day
- New files arrive automatically
- Watchdog processes them
- Intelligence updated automatically
- You provide smart responses when asked

### End of Day (5pm)
- Final status check
- Any blockers? Log them
- Prepare for next day

---

## 📈 QUALITY STANDARDS YOU MUST MEET

✅ **Accuracy:** 95%+ correct classifications  
✅ **Completeness:** Extract ALL entities  
✅ **Actionability:** Always provide next steps  
✅ **Prioritization:** Urgent items first  
✅ **Speed:** Instant response to queries  
✅ **Data-driven:** Never generic responses  

---

## 🚀 REFERENCES

### For GTD Methodology Details
→ See: `SHARED_KNOWLEDGE_BASE\01_SHARED_MAIL_ROOM_OPERATIONS.md`

### For Routing Details
→ See: `SHARED_KNOWLEDGE_BASE\01_SHARED_MAIL_ROOM_OPERATIONS.md`

### For Phase Rollout Details
→ See: `memory\Context\PHASE_ROLLOUT_CHECKLIST.md`

### For Quick Reference
→ See: `memory\SOPs\02_NAVI_QUICK_REFERENCE.md`

---

## 🎯 REMEMBER

You are **NOT** a generic receptionist.  
You are **NOT** answering without real data.  
You are **NOT** giving generic responses.

You **ARE** an intelligent coordinator.  
You **ARE** backed by real file intelligence.  
You **ARE** making data-driven recommendations.

Every response should demonstrate:
- ✅ Real file knowledge
- ✅ Smart routing decisions
- ✅ Actionable next steps
- ✅ Proper prioritization
- ✅ Professional communication

---

**This is YOUR complete operational guide. Reference it. Use it. Master it.**

Let's provide exceptional intelligent mail room service! 🚀


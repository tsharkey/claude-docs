# Task History and Patterns

## Overview
This document captures common task patterns, typical time estimates, and proven approaches from grooming sessions to improve future task organization and suggestions.

## Task Categories & Patterns

### Assessment/Planning Tasks
**Pattern:** Break down large, vague projects into specific actionable tasks
**Typical Time:** `@30m` for assessment, `@2hr` for comprehensive planning

**Examples:**
- "Assess [Project] state and create follow-up tasks" 
  - Time: `@30m`
  - Output: Specific actionable sub-tasks
  - Description template: "Review current state of [project] to understand what has been completed, what's outstanding, and what needs to be done next. **Output:** Create specific follow-up tasks based on assessment findings"

- "Create structured plan for [Project] development"
  - Time: `@2hr` 
  - Include getting started hints in description
  - Break into phases/milestones approach

**Key Insight:** Replace vague parent tasks with assessment tasks that generate concrete next steps

### Development Workflow Tasks
**Pattern:** Backend → API → Frontend pipeline with clear dependencies
**Typical Time:** `@2hr` per layer, `@+1d` for complex integrations

**Examples from Advantage Ads:**
1. Service Classes (`@2hr`) → Database layer
2. GraphQL Resolvers (`@2hr`) → API layer  
3. Redux Store Updates (`@+1d`) → State management
4. UI Integration (`@+1d`) → Frontend layer

**Standard Description Elements:**
- Dependencies clearly stated
- Completion criteria: "Code reviewed and merged"
- Repository specification when relevant
- Learning curve acknowledgment for unfamiliar tech

### Security/Compliance Tasks  
**Pattern:** Comprehensive setup with multiple configuration areas
**Typical Time:** `@30m` for simple config, `@2hr` for complex setup

**SecureFrame Example Breakdown:**
- User access management (`@30m`)
- Asset inventory (`@2hr`)
- Policy documentation (`@2hr`) 
- Monitoring/alerting (`@30m`)
- Evidence collection (`@2hr`)
- Vendor assessment (`@30m`)
- Employee lifecycle (`@2hr`)

**Key Insight:** Security tools require systematic setup across multiple domains - break into discrete configuration tasks

### Infrastructure/DevOps Tasks
**Pattern:** Terraform deployment with environment-specific troubleshooting
**Typical Time:** `@2hr` for environment extensions

**Example:**
- "Deploy [Tool] to [Environment]"
- Standard description: "Run existing Terraform configurations and resolve any environment-specific gotchas or missing resources"
- Include scope, method, and goal

### Research Tasks
**Pattern:** Information gathering with specific output requirements
**Typical Time:** `@30m` for quick research, `@2hr` for comprehensive analysis

**Common Labels:** `@research`, combined with time estimates
**Description Elements:**
- Clear research scope
- Expected deliverable/output
- Context for why research is needed

### Habit/Recurring Tasks
**Pattern:** Regular activities supporting personal/professional development
**Typical Time:** `@30m` for focused activities, `@2hr` for substantial sessions

**Examples:**
- Reading sessions: `@30m` for focused learning
- Creative time: `@2hr` for photography, beach relaxation
- Review sessions: `@30m` for knowledge management

**Key Insight:** Users prefer consistent time blocks for similar habit types

### Administrative/Personal Tasks
**Pattern:** Multi-step bureaucratic processes requiring coordination
**Typical Time:** `@2hr` (accounts for hold times and multiple contacts)

**Example Pattern:**
- Issue identification
- Multiple agency/party coordination  
- Documentation requirements
- Follow-up steps

**Description Elements:**
- Background context of the issue
- Current status
- Next steps required
- Information to gather

## Time Estimation Guidelines

### Standard Time Labels
- `@30m`: Quick tasks, simple configuration, assessment, focused habits
- `@2hr`: Substantial work, complex setup, planning sessions, creative time  
- `@+1d`: Complex integrations, learning-heavy tasks, multi-component work
- `@+1w`: Major projects with multiple sub-tasks

### Time Estimation Factors
- **Learning curve:** Add time for unfamiliar technologies
- **Coordination required:** Add time for multiple parties/agencies
- **Environment differences:** Add time for deployment variations
- **Hold times:** Factor in for government/service calls

## Sub-task Creation Patterns

### When to Create Sub-tasks
- Parent task >4 hours of estimated work
- Clear sequential dependencies  
- Multiple skill areas required
- Distinct milestones for progress tracking

### Sub-task Naming Conventions
- Action-oriented verbs
- Specific scope indication
- Technology/tool specification when relevant

## Description Templates

### Assessment Task Template
```
Review the current state of [project] work to understand what has been completed, what's outstanding, and what needs to be done next.

**Output:** Create specific follow-up tasks based on assessment findings
**Goal:** Clear understanding of [project] status and actionable next steps
```

### Development Task Template  
```
[Specific technical work description]

**Dependencies:** [Required predecessor tasks]
**Repository:** [If applicable]
**Note:** [Learning curve or special considerations]
**Completion Criteria:** Code reviewed and merged into main branch
```

### Infrastructure Task Template
```
[Deploy/Configure] [tool] in [environment]. [Brief scope description and expected challenges]

**Scope:** [What's being accomplished]
**Method:** [Approach - Terraform, manual config, etc.]
**Goal:** [End state description]
```

## Common Anti-patterns to Avoid

### Vague Parent Tasks
- ❌ "Project X work" with no description
- ✅ "Assess Project X state and create follow-up tasks"

### Missing Dependencies
- ❌ Tasks that can't be started without prerequisites
- ✅ Clear dependency statements in descriptions

### Unrealistic Time Estimates
- ❌ Complex multi-step work estimated as `@30m`
- ✅ Account for coordination, learning, and troubleshooting time

### Duplicate Task Creation
- ❌ Similar work scattered across multiple vague tasks
- ✅ Consolidate related work, eliminate redundancy

## Successful Grooming Session Patterns

### Session Structure
1. **Bulk Updates First:** Time estimates for straightforward tasks
2. **Collaborative Grooming:** Complex tasks requiring user input
3. **Priority Focus:** High-impact work (Focus Areas, urgent deadlines)
4. **Systematic Processing:** One task at a time with full context

### Quality Indicators
- Clear, actionable descriptions
- Appropriate time estimates with reasoning
- Proper project placement
- Dependencies explicitly stated
- Completion criteria defined
- `@groomed` label applied

## Notes for Future Updates
This document should be updated when:
- New task patterns emerge
- Time estimation accuracy improves
- New project types are encountered
- Successful grooming techniques are discovered
- Anti-patterns are identified and resolved

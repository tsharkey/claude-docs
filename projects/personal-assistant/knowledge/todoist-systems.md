# Todoist AI Assistant Integration System

## System Overview

This document defines the rules and protocols for an AI assistant to effectively collaborate with a user's Todoist workflow. The system is designed around quick capture followed by structured daily review, with clear decision trees for task organization and AI assistance opportunities.

## Core Workflow Pattern

```
CAPTURE → INBOX → DAILY REVIEW → ORGANIZED TASKS → EXECUTION
```

**User Pattern**: Quick capture everything to inbox, then daily review session to organize all items.

**AI Role**: Assist during daily review with suggestions, identify assistance opportunities, help with planning and scheduling.

## Project Structure Hierarchy

## Project Structure Hierarchy

### Primary Categories
- `#Personal` (parent project)
  - `#Focus Area - [Current Interest]` (e.g., "Focus Area - Warhammer 40k", "Focus Area - Personal Website")
  - `#Personal Todo` (miscellaneous active tasks)
  - `#Personal Chores` (routine maintenance tasks)
  - `#Personal Habits` (recurring personal development)
  - `#Personal Mess` (backlog/future ideas)

- `#Work` (parent project)
  - `#Focus Area - [Current Project]` (e.g., "Focus Area - Financial Services", "Focus Area - Advantage Ads")
  - `#Work Todo` (general work tasks)
  - `#Work Chores` (routine work maintenance)
  - `#Work Mess` (work-related backlog)

- `#Family` (parent project - shared)
  - `#Family Todo` (family tasks)
  - `#House Projects` (home improvement/maintenance)
  - `#Family Chores` (household routine tasks)
  - `#Birthdays and Holidays` (special events)
  - `#Family Mess` (family-related backlog)

- `#Lists` (parent project - reference lists)
  - `#Buy List` (shopping/purchase tracking)
  - `#Watch` (movies/shows to watch)
  - `#Restaurants` (places to try)
  - `#Date Ideas` (activity suggestions)
  - `#Reading` (books/articles to read)
  - `#Gift Ideas` (present suggestions)

### Project Assignment Logic

**CRITICAL RULE**: Any task with a date NEVER goes to `#Mess` - it must be assigned to an active project.

**Active Projects** (Focus Areas, Todo, Chores, Habits):
- Tasks with dates (scheduled/deadline)
- Tasks within current focus areas
- Tasks requiring active attention/completion
- Routine and recurring tasks

**Mess Projects** (`#Personal Mess`, `#Work Mess`, `#Family Mess`):
- Undated tasks outside current focus areas
- Future ideas/exploration items
- Tasks that might be valuable "someday"
- Research ideas not immediately relevant

**Lists Projects** (`#Lists` hierarchy):
- Reference materials and future considerations
- No immediate action required
- Ideas and suggestions for later

## Label System

### Time Estimation Labels
- `@15m` - Quick tasks (under 15 minutes) [OPTIONAL - user may add later]
- `@30m` - Short tasks (15-30 minutes)
- `@1hr` - Medium tasks (30 minutes - 1 hour) [OPTIONAL - user may add later]  
- `@2hr` - Long tasks (1-2 hours)
- `@+1d` - Full day tasks (requires dedicated day)
- `@+1w` - Week-long tasks or projects (requires multiple days)

### Task Type Labels
- `@research` - Tasks requiring information gathering/analysis
- `@shopping` - Tasks involving purchasing decisions/price comparison
- `@waiting` - Tasks blocked by external dependencies
- `@blocked` - Tasks blocked by internal dependencies

### Label Assignment Rules
**Active Project Tasks Must Have:**
- Time estimation label (`@30m`, `@2hr`, `@+1d`, `@+1w`)
- Task type label if applicable (`@research`, `@shopping`, `@waiting`, `@blocked`)
- Appropriate scheduling/priority

**Mess Project Tasks:**
- No required labels (minimal organization)
- May have task type labels if obvious

**Lists Project Tasks:**
- Minimal labeling required
- Treated as reference material

## Daily Review Process

### AI Assistant Role During Review

For each inbox item, the AI should analyze and suggest:

1. **Project Assignment**
   - Check for dates → Must go to active project
   - Assess alignment with current focus areas
   - Suggest specific project placement with reasoning

2. **Label Recommendations**
   - Estimate time required based on task description
   - Identify task type from keywords/context
   - Explain reasoning for suggestions

3. **AI Assistance Opportunities**
   - Flag `@research` tasks the AI could complete
   - Identify `@shopping` tasks for price comparison/research
   - Suggest breaking down complex tasks into AI-assistable components

4. **Scheduling Suggestions**
   - Recommend dates based on priority/urgency indicators
   - Consider user's focus areas and capacity
   - Suggest batching similar tasks

### Decision Tree for Task Organization

```
Does task have a date?
├─ YES → Active Project (Focus area or Todo-General)
│   ├─ Add time estimate label
│   ├─ Add task type label if applicable
│   └─ Set appropriate priority
└─ NO → Is it within current focus areas?
    ├─ YES → Active Project
    │   ├─ Add time estimate label
    │   ├─ Add task type label if applicable
    │   └─ Consider scheduling
    └─ NO → Mess Project
        ├─ Minimal labeling
        └─ Note potential for future promotion
```

## Focus Area Management

### When Focus Areas Change

**Process:**
1. Review current focus project tasks with AI assistance
2. Categorize each task:
   - **Keep Active**: Still relevant or has date
   - **Move to Mess**: No longer aligned with interests
   - **Complete Quickly**: Small tasks worth finishing

3. **Project Evolution Options:**
   - Rename existing projects if topic evolved
   - Archive completed focus areas
   - Create new projects only when needed
   - Promote relevant tasks from Mess to new focus areas

**AI Role in Transitions:**
- Analyze current tasks for continued relevance
- Scan Mess backlog for items matching new interests
- Suggest transition strategies (clean break vs gradual shift)
- Help plan completion of orphaned tasks

## AI Assistance Identification

### Tasks AI Can Complete
- `@research` tasks: Information gathering, analysis, comparisons
- `@shopping` tasks: Price research, feature comparisons, recommendations
- Breaking down complex tasks into subtasks
- Creating templates or frameworks
- Data analysis and summarization

### Tasks AI Can Support
- Planning and scheduling optimization
- Task prioritization based on context
- Identifying dependencies and blockers
- Suggesting task modifications for efficiency

### Red Flags for Human-Only Tasks
- Personal relationship matters
- Financial transactions requiring approval
- Physical tasks requiring presence
- Creative work requiring personal style/voice
- Decision tasks requiring personal values/preferences

## Scheduling and Planning Principles

### Scheduling and Task Management Benefits

**Daily Planning:**
- "You have 2 hours free this afternoon - here are your `@2hr` tasks to choose from"
- "I can fit three `@30m` tasks between your meetings"
- Avoid suggesting `@+1d` tasks for short time slots

**Weekly Planning:**
- "Your `@+1w` project needs to start Monday to finish on time"
- Identify which focus areas need attention
- Plan dedicated time blocks for longer tasks

**Task Batching:**
- Group similar time estimates for efficiency
- Batch `@research` tasks for focused work sessions
- Schedule `@shopping` tasks when AI can assist with research

## Communication Protocols

### AI Suggestion Format
```
TASK: [Task name]
SUGGESTED PROJECT: [Project] 
REASONING: [Why this project fits]
LABELS: [Suggested labels with reasoning]
AI ASSISTANCE: [What AI could help with, if applicable]
SCHEDULING: [Recommended timing/priority]
```

### Focus Area Discussion
- AI should ask about current interests/motivations
- Track focus area changes over time
- Suggest connections between tasks and interests
- Recommend when to review/update focus areas

## Current System State

**Implemented Structure (as of June 2025):**
- ✅ Full project hierarchy with parent/child relationships
- ✅ Focus area projects for current interests (Warhammer 40k, Personal Website, Financial Services, Advantage Ads)
- ✅ Mess projects for backlog items in each major category
- ✅ Lists hierarchy for reference materials and future ideas
- ✅ Time estimation labels: `@30m`, `@2hr`, `@+1d`, `@+1w`
- ✅ Task type labels: `@research`, `@shopping`, `@waiting`, `@blocked`

**Ready for AI Integration:**
- MCP server can access all projects and labels
- System supports intelligent task categorization during daily review
- Time estimates enable realistic scheduling and planning
- Task type labels identify AI assistance opportunities

### System Health Indicators
- Inbox regularly cleared during daily reviews
- Active projects contain only relevant, actionable tasks
- Mess project prevents active project bloat
- AI assistance opportunities are regularly identified and acted upon
- Focus areas remain aligned with current interests and energy

### Warning Signs
- Inbox backlog growing consistently
- Active projects becoming cluttered with irrelevant tasks
- Focus areas unchanged for extended periods despite lost interest
- AI suggestions consistently rejected (indicates system misalignment)

## Success Metrics

### Context Awareness
- Track patterns in user's task creation and completion
- Learn from project assignment decisions over time
- Recognize seasonal/cyclical patterns in focus areas
- Adapt suggestions based on user feedback history

### Proactive Assistance
- Monitor for research tasks that could be automated
- Suggest task breakdowns before user gets overwhelmed
- Identify when focus areas may need refreshing
- Recommend system optimizations based on usage patterns

### Natural Language Processing
- Parse task descriptions for implicit timing/priority cues
- Identify task relationships and dependencies
- Extract actionable components from vague task descriptions
- Recognize context clues for project assignment

---

*This system prioritizes sustainability over perfection. The AI should help maintain the user's existing successful patterns while gradually optimizing for better outcomes.*

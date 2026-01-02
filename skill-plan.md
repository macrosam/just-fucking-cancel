# Subscription Audit Skill - Plan

## Step 1: Concrete Examples

**User triggers:**
- "Audit my subscriptions"
- "Find recurring charges in my transactions"
- "Help me cancel subscriptions"
- "What subscriptions am I paying for?"

**Workflow:**
1. User provides transaction CSVs (Apple Card, Chase, etc.)
2. Claude analyzes for recurring patterns
3. Generates interactive HTML audit with categories
4. User reviews and marks items to cancel
5. Claude executes cancellations via browser automation

## Step 2: Reusable Skill Contents

| Type | File | Purpose |
|------|------|---------|
| **assets/** | `template.html` | The HTML audit template (stripped of personal data) |
| **scripts/** | `parse_transactions.py` | Parse common CSV formats (Apple Card, Chase, Mint) |
| **scripts/** | `detect_subscriptions.py` | Pattern matching for recurring charges |
| **references/** | `common-services.md` | Known subscription services + cancellation URLs |
| **references/** | `csv-formats.md` | Documentation of supported bank export formats |

## Step 3: Skill Structure

```
subscription-audit/
├── SKILL.md
├── assets/
│   └── template.html          # Clean HTML template
├── scripts/
│   ├── parse_transactions.py  # CSV parsing
│   └── detect_subscriptions.py # Recurring charge detection
└── references/
    ├── common-services.md     # Service database + cancel URLs
    └── csv-formats.md         # Bank export format docs
```

## Key Design Decisions

1. **Input flexibility**: Support multiple bank formats (Apple Card, Chase, generic CSV)
2. **Privacy-first**: All data stays local, never uploaded
3. **Interactive output**: HTML with checkboxes, localStorage persistence
4. **Browser automation**: Leverage Claude Code's MCP tools for cancellations

## Status

- [x] Plan created
- [ ] HTML template finalized
- [ ] Skill initialized
- [ ] Scripts implemented
- [ ] References written
- [ ] Skill packaged

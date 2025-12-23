---
description: Post-task review and retrospective with session memory
---

# Post-Task Review & Retrospective

สร้าง retrospective พร้อม Before/After context (Layer 3)

## Output

`$PROJECT_ROOT/docs/retrospective/YYYY-MM/retrospective_YYYY-MM-DD_hhmmss.md`

## Instructions

1. **Gather Git info**: branch, changed files, recent commits
2. **Determine type**: feature/bugfix/refactor/decision/discovery/config/docs
3. **Fill Before/After context** (CRITICAL)
4. **Document decisions** with rationale
5. **Commit**: `git commit -m "docs(retro): [type] - [title]"`

## Type Classification

| Type | Use When |
|------|----------|
| `feature` | New functionality |
| `bugfix` | Bug fix |
| `refactor` | Code restructure |
| `decision` | Architecture decision |
| `discovery` | Research/learning |
| `config` | Configuration changes |
| `docs` | Documentation only |

## Template

```markdown
---
date: YYYY-MM-DDTHH:MM:SS+07:00
type: feature|bugfix|refactor|decision|discovery|config|docs
tags: [tag1, tag2]
branch: branch-name
issue: "#123"
duration: ~2h
files_changed:
  - path/to/file.go
---

# [Task Title]

## Session Metadata

| Field | Value |
|-------|-------|
| Date | YYYY-MM-DD |
| Time | HH:MM:SS (Asia/Bangkok) |
| Duration | estimated |
| Type | type |
| Branch | branch |

---

## Context: Before

- **Problem**: ปัญหาที่เจอ
- **Existing Behavior**: พฤติกรรมเดิม
- **Why Change**: ทำไมต้องเปลี่ยน
- **Metrics**: ตัวเลขก่อนแก้

---

## Context: After

- **Solution**: วิธีแก้
- **New Behavior**: พฤติกรรมใหม่
- **Improvements**: สิ่งที่ดีขึ้น
- **Metrics**: ตัวเลขหลังแก้

---

## Decisions & Rationale

| Decision | Options Considered | Chosen | Rationale |
|----------|-------------------|--------|-----------|
| | | | |

---

## Session Summary

### Task Description
อธิบาย task

### Outcome
ผลลัพธ์

---

## Timeline

| Time | Activity |
|------|----------|
| HH:MM | activity |

---

## Technical Details

### Files Modified

| File | Changes |
|------|---------|
| `file.go` | changes |

---

## Honest Feedback

### What Went Well
- 

### What Could Be Improved
- 

---

## Lessons Learned

- Technical insights
- Process improvements

---

## Next Steps

### Immediate
- [ ] 

### Future Improvements
- [ ] 

---

## Validation Checklist

- [ ] Code compiles
- [ ] Tests pass
- [ ] Atomic commits
- [ ] Error handling
- [ ] Consistent patterns
```

## Critical: Before/After Context

This is the most important part for future reference:

```markdown
## Context: Before
- **Problem**: MongoDB timeout under load
- **Metrics**: p99 = 2s, error rate = 5%

## Context: After
- **Solution**: Connection pool + retry
- **Metrics**: p99 = 200ms, error rate < 0.1%
```

## After Creating

1. Link related /mem files
2. Update CLAUDE.md if needed
3. Consider /distill if patterns emerge

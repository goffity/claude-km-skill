# /distill Template

## File Path

```
docs/knowledge-base/[topic-name].md
```

## Template

```markdown
# [Topic Name]

| Field | Value |
|-------|-------|
| **Created** | YYYY-MM-DD |
| **Sources** | learnings ที่ใช้ distill |
| **Tags** | `tag1` `tag2` |

---

## Key Insight

> One-sentence summary of the pattern/lesson

---

## The Problem

| Attempt | Result |
|---------|--------|
| ทำแบบ X | เกิดปัญหา Y |
| ทำแบบ Z | ยังไม่ดี เพราะ... |

---

## The Solution

### Pattern: [Pattern Name]

```go
// Code example showing the correct approach
```

**Why this works:**
- Reason 1
- Reason 2

---

## Anti-Patterns

| Don't Do This | Do This Instead |
|---------------|-----------------|
| Bad approach | Good approach |

---

## When to Apply

- Condition 1: ใช้ pattern นี้เมื่อ...
- Condition 2: ไม่ใช้เมื่อ...

---

## Related

- Learnings: `docs/learnings/...` (source files)
- Code: `path/to/relevant/code.go`
- Docs: link to external docs

---

## Changelog

| Date | Change |
|------|--------|
| YYYY-MM-DD | Initial creation |
```

## After Distilling

Mark source learnings:

```markdown
---
> **Distilled:** ถูก distill ไปที่ `docs/knowledge-base/[topic].md`
```

## Commit

```bash
git add docs/knowledge-base/ docs/learnings/
git commit -m "knowledge: [topic-name] - [summary]"
```

## When to Distill

| Trigger | Action |
|---------|--------|
| มี 3+ learnings เรื่องเดียวกัน | รวมเป็น 1 knowledge entry |
| พบ pattern ที่ใช้ซ้ำได้ | สร้าง knowledge entry |
| พบ anti-pattern สำคัญ | Document เพื่อป้องกัน |
| Weekly/Monthly review | Scan และ distill pending learnings |

# Learnings

Corrections, insights, and knowledge gaps captured during development.

**Categories**: correction | insight | knowledge_gap | best_practice

---

## [LRN-20260412-001] correction

**Logged**: 2026-04-12T12:12:00Z
**Priority**: high
**Status**: pending
**Area**: config

### Summary
When text-to-speech fails with the built-in `tts` tool, do not stop there. Check installed local TTS skills and automatically fall back to a working local provider before telling the user TTS is unavailable.

### Details
The user had already installed the `sherpa-onnx-tts` skill and its runtime/model files. I called the built-in `tts` tool, received `no provider registered; openai: not configured`, and incorrectly concluded that TTS was misconfigured. I should have discovered and tried the local skill immediately. Verification showed local fallback works by running the sherpa wrapper successfully and producing a WAV file.

### Suggested Action
Adopt a general recovery policy for all workflows: after a first failure, automatically probe alternative built-in tools, installed skills, existing local apps, and safe installations of missing dependencies when appropriate. Persist the rule in workspace guidance, with TTS as one concrete example.

### Metadata
- Source: user_feedback
- Related Files: TOOLS.md, AGENTS.md
- Tags: tts, fallback, recovery, persistence, local-skill

---

## [LRN-20260412-002] correction

**Logged**: 2026-04-12T12:15:00Z
**Priority**: high
**Status**: pending
**Area**: config

### Summary
The fallback rule must be generalized to all workflows, not just TTS.

### Details
The user explicitly wants a persistence-first operating style: do not stop after a single failed attempt. When a workflow fails, I should keep trying alternate methods and, when safe, even install missing skills or apps to complete the task. Reporting failure too early is itself a workflow error.

### Suggested Action
Turn fallback behavior into a general rule across task execution. Before saying a task failed, try multiple available paths and only stop when blocked by safety, destructive risk, credentials, explicit approvals, or genuinely exhausted options.

### Metadata
- Source: user_feedback
- Related Files: TOOLS.md, AGENTS.md
- Tags: fallback, persistence, workflow, recovery

---

## [LRN-20260412-003] correction

**Logged**: 2026-04-12T14:19:00Z
**Priority**: high
**Status**: pending
**Area**: config

### Summary
When a capability is missing, search the web for methods to implement it and prioritize free usable solutions before asking the user to provide paid credentials.

### Details
The user wants a stronger completion bias: if a task cannot be done with current tools, I should proactively search online for feasible implementation paths, especially free or locally runnable methods, install what is needed when safe, and then continue the task instead of stopping at the first capability gap.

### Suggested Action
Promote a general rule: capability gaps trigger method discovery and environment setup, with preference for free/local solutions, before reporting inability.

### Metadata
- Source: user_feedback
- Related Files: TOOLS.md, AGENTS.md
- Tags: capability-gap, fallback, web-search, free-tools, setup

---

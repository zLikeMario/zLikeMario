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
Adopt a strict TTS priority order: first use the native `tts` tool, and if it fails, automatically probe known local TTS skills such as `sherpa-onnx-tts` before reporting failure. Persist the rule in workspace guidance.

### Metadata
- Source: user_feedback
- Related Files: TOOLS.md, AGENTS.md
- Tags: tts, fallback, feishu, local-skill

---

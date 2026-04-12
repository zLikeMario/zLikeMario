# Errors

Command failures and integration errors.

---

## [ERR-20260412-001] tts_tool

**Logged**: 2026-04-12T12:12:00Z
**Priority**: high
**Status**: pending
**Area**: config

### Summary
Built-in `tts` tool failed due to missing provider registration, but a working local fallback existed.

### Error
```
TTS conversion failed: : no provider registered; openai: not configured
```

### Context
- Operation attempted: OpenClaw `tts` tool for Feishu audio reply
- Local environment also had `sherpa-onnx-tts` runtime and model installed under `~/.openclaw/tools/sherpa-onnx-tts`
- The failure should have triggered fallback discovery instead of a user-facing configuration diagnosis

### Suggested Fix
Probe local TTS fallbacks automatically after `tts` tool failure, starting with `sherpa-onnx-tts` when installed.

### Metadata
- Reproducible: yes
- Related Files: TOOLS.md, /home/zario/.npm-global/lib/node_modules/openclaw/skills/sherpa-onnx-tts/SKILL.md

---

# TOOLS.md - Local Notes

Skills define _how_ tools work. This file is for _your_ specifics — the stuff that's unique to your setup.

## What Goes Here

Things like:

- Camera names and locations
- SSH hosts and aliases
- Preferred voices for TTS
- Speaker/room names
- Device nicknames
- Anything environment-specific

## Examples

```markdown
### Cameras

- living-room → Main area, 180° wide angle
- front-door → Entrance, motion-triggered

### SSH

- home-server → 192.168.1.100, user: admin

### TTS

- Preferred voice: "Nova" (warm, slightly British)
- Default speaker: Kitchen HomePod
```

## Why Separate?

Skills are shared. Your setup is yours. Keeping them apart means you can update skills without losing your notes, and share skills without leaking your infrastructure.

## TTS Fallback Rules

- For text-to-speech, do **not** stop after the built-in `tts` tool fails.
- Always try providers in this order:
  1. OpenClaw `tts` tool
  2. Local `sherpa-onnx-tts` skill if installed
- If one path succeeds, prefer the successful path next time for the same kind of task.
- Only tell Zario that TTS is unavailable after both the built-in tool and known local fallback paths have been tried.
- Current confirmed local fallback:
  - `sherpa-onnx-tts`
  - Runtime: `~/.openclaw/tools/sherpa-onnx-tts/runtime`
  - Model: `~/.openclaw/tools/sherpa-onnx-tts/models/vits-piper-en_US-lessac-high`
  - Wrapper: `/home/zario/.npm-global/lib/node_modules/openclaw/skills/sherpa-onnx-tts/bin/sherpa-onnx-tts`

---

Add whatever helps you do your job. This is your cheat sheet.

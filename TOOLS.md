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

## Recovery and Fallback Rules

- For any task, do **not** stop after the first failed attempt.
- Always look for a second and third path before telling Zario something failed.
- Recovery order by default:
  1. Built-in tool or direct first-class tool
  2. Installed skill designed for the task
  3. Existing local CLI/app already present on the machine
  4. Safe installation of a missing skill or local dependency if that is likely to solve it
- If one path succeeds, prefer the successful path next time for the same kind of task.
- Only report failure after reasonable fallback and recovery options have been actually tried.
- Escalate to the user before continuing only when the next step is destructive, account-sensitive, needs credentials, needs explicit approval, or changes the system in a significant/risky way.

### Current confirmed TTS fallback

- `sherpa-onnx-tts`
- Runtime: `~/.openclaw/tools/sherpa-onnx-tts/runtime`
- Model: `~/.openclaw/tools/sherpa-onnx-tts/models/vits-piper-en_US-lessac-high`
- Wrapper: `/home/zario/.npm-global/lib/node_modules/openclaw/skills/sherpa-onnx-tts/bin/sherpa-onnx-tts`

---

Add whatever helps you do your job. This is your cheat sheet.

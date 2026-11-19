# SLAY — say it, log off.

Free DM wingman. Paste the convo or drop a screenshot. It reads where things stand (her interest, who's chasing, the verdict) and gives 4 lines in the SLAY voice.

## Run it (free)
1. Get a free Groq key at https://console.groq.com/keys (no card needed).
2. Open `index.html`, or serve the folder (`python -m http.server 8080` → http://localhost:8080) so it installs as an app.
3. ⚙️ → paste the key → Save.

**Phone:** push this folder to a GitHub repo and turn on GitHub Pages (free). Open the URL on your phone and choose *Add to Home Screen*.

## Providers
| Provider | Cost | Limits | Screenshots |
|---|---|---|---|
| Groq (default) | free | Qwen 3.8 27B (best voice, ~1k output tokens/min), auto-falls back to GPT-OSS-120B | yes (Qwen 3.8) |
| Gemini | free | low daily cap, changes often | yes |
| Ollama | free, local | unlimited, runs on your GPU | yes with `qwen2.5vl:7b` |

Ollama: `ollama pull llama3.1:8b`, then set `OLLAMA_ORIGINS=*` before `ollama serve`.
Model names can be changed in ⚙️ when a provider retires one.

## Files
- `prompt.js`: the brand voice and playbook rules. **Edit this to tune the rizz.**
- `index.html`: the UI, provider calls, and offline rule checks (double text, essay length, emoji spam, opening with a compliment).

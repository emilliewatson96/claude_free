---

# claude_free

A lightweight setup to run Claude-compatible workflows using OpenRouter models.

---

## ⚠️ Important Notice

Using `curl | bash` can be dangerous if the source is not trusted. Review scripts before executing them.

---

## Step 1 — Install CLI

Run the following command to install:

```bash
curl -fsSL https://claude.ai/install.sh | bash
```

---

## Step 2 — Create OpenRouter Account

Go to:

[https://openrouter.ai](https://openrouter.ai)

Create an account and generate an API key.

---

## Step 3 — Configure Environment

Create or edit your configuration file (e.g. `config.json`):

```json
{
  "env": {
    "ANTHROPIC_BASE_URL": "https://openrouter.ai/api",
    "ANTHROPIC_AUTH_TOKEN": "YOUR_OPENROUTER_API_KEY",
    "ANTHROPIC_API_KEY": "",
    "ANTHROPIC_DEFAULT_OPUS_MODEL": "openrouter/free",
    "ANTHROPIC_DEFAULT_SONNET_MODEL": "nvidia/nemotron-3-ultra-550b-a55b:free",
    "ANTHROPIC_NEW_MODEL": "qwen/qwen3-coder:free"
  },
  "model": "opus"
}
```
## Or Use 
```bash
mkdir -p ~/.claude && printf '{\n  "env": {\n    "ANTHROPIC_BASE_URL": "https://openrouter.ai/api",\n    "ANTHROPIC_AUTH_TOKEN": "YOUR_OPENROUTER_API_KEY",\n    "ANTHROPIC_API_KEY": "",\n    "ANTHROPIC_DEFAULT_OPUS_MODEL": "openrouter/free",\n    "ANTHROPIC_DEFAULT_SONNET_MODEL": "nvidia/nemotron-3-ultra-550b-a55b:free",\n    "ANTHROPIC_NEW_MODEL": "qwen/qwen3-coder:free"\n  },\n  "model": "opus"\n}\n' > ~/.claude/settings.json
```

---

## Notes

* Replace `YOUR_OPENROUTER_API_KEY` with your actual key.
* Ensure your CLI tool supports OpenRouter’s Anthropic-compatible endpoint.
* Model names may change depending on OpenRouter availability.

---


# Langflow Codespace

A ready-to-go [Langflow](https://www.langflow.org/) environment that runs in a GitHub Codespace.

## Quickstart

1. Click **Code → Codespaces → Create codespace on main** (top right of this repo on GitHub).
2. Wait for the Codespace to finish setting up. The first launch installs Langflow (~3–5 min unless prebuilds are enabled).
3. Provide an API key for your model provider. Recommended: a Codespace secret.
   - GitHub → **Settings → Codespaces → Codespace secrets** → **New secret** → name `ANTHROPIC_API_KEY` (or `OPENAI_API_KEY`, etc.) → grant access to this repo.
   - Alternative for local-only use: `cp .env.example .env` and edit.
4. Start Langflow:

   ```bash
   source .venv/bin/activate
   langflow run
   ```

5. When VS Code prompts you, open the forwarded **port 7860** in your browser. You'll land on the Langflow UI.

## Notes

- Telemetry is disabled (`DO_NOT_TRACK=true`).
- Pinned to Langflow `1.9.2` in `requirements.txt`.
- The `.venv/` is built fresh in each Codespace; it is not committed.

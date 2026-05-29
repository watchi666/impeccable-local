# Image generation paths

Use this when preview work needs image generation and the default path fails.

1. Try the harness-native image tool first.
2. If it fails, inspect the configured provider instead of inventing a workaround.
3. Verify whether the current environment has a working OpenRouter-backed image path.
4. If the primary provider is blocked, fall back to the available OpenRouter workflow.
5. Persist each successful output into the project tree immediately.

Do not skip the image step silently when the workflow depends on it.

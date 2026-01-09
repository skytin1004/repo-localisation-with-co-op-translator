# Repository localisation demo (Co-op Translator + GitHub Actions)

This repository is configured as a **live demo** for automating documentation localisation:

- You edit a Markdown file (e.g. `README.md`)
- You push to `main`
- GitHub Actions runs Co-op Translator
- The translated output is created/updated under `translations/<lang>/...`
- A **Pull Request** is opened with the changes for review

Below is the test image for the Co-op Translator.

![Co-op Translator Test Image](./images/co-op-translator-test.png)

## What’s included

- **Docs**: `README.md`, `docs/`
- **Automation**: `.github/workflows/co-op-translator.yml`

## Prerequisites (GitHub Secrets)

Add these in **Settings → Secrets and variables → Actions**:

- **`OPENAI_API_KEY`**: Your OpenAI API key

If you want image translation later, also add your Azure AI Vision secrets (optional) and enable `-img` in `.github/workflows/translate.yml`.

## Demo flow (what to do on stage)

1. Edit a single line in `README.md` (or a file under `docs/`)
2. Commit and push to `main`
3. Open the **Actions** tab and show the workflow run
4. Open the created **Pull Request**
5. Show changes under `translations/ko/` (and other languages if enabled)

## Languages

Default languages in the workflow:

- Korean: `ko`
- Japanese: `ja`
- French: `fr`

Change them in `.github/workflows/co-op-translator.yml`.

## Notes


- Co-op Translator project: `https://github.com/Azure/co-op-translator`
  

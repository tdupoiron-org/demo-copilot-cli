# demo-copilot-cli

This repository demonstrates how to use GitHub Copilot CLI in a GitHub Actions workflow.

## What it does

The workflow (`/.github/workflows/copilot-cli-demo.yml`) demonstrates:

1. **Installing GitHub Copilot CLI** in a GitHub Actions environment
2. **Authenticating** with GitHub using the built-in `GITHUB_TOKEN`
3. **Running Copilot CLI in silent/non-interactive mode** using:
   - `--prompt` flag to execute a specific prompt directly
   - `--allow-all-tools` flag to run without confirmation prompts

## Key Features

- ✅ **Non-interactive execution**: Uses `--prompt` and `--allow-all-tools` flags
- ✅ **Automatic authentication**: Uses GitHub's built-in token
- ✅ **Trusted directory setup**: Configures Copilot to trust the workspace
- ✅ **Multiple triggers**: Runs on push, PR, or manual dispatch

## How to use

1. **Push to main branch** or **create a pull request** to trigger the workflow
2. **Manual trigger**: Go to Actions tab → "Copilot CLI Demo" → "Run workflow"
3. **View results**: Check the workflow logs to see Copilot's response

## Command Reference

The workflow uses this key command:
```bash
copilot --prompt "Explain what the test.js file does" --allow-all-tools
```

Where:
- `--prompt`: Executes the prompt directly without interactive mode
- `--allow-all-tools`: Allows all tools to run automatically without confirmation (required for non-interactive mode)

## Requirements

- GitHub repository with Actions enabled
- GitHub Copilot subscription (Pro, Business, or Enterprise)
- Copilot CLI policy enabled (for organization repos)

# Copilot CLI PR Review & Documentation

This repository demonstrates how to use GitHub Copilot CLI in a GitHub Actions workflow to automatically review pull requests and suggest documentation updates.

## What it does

The workflow (`/.github/workflows/copilot-cli-demo.yml`) automatically:

1. **Triggers on Pull Requests** - Runs when PRs are opened, updated, or reopened
2. **Analyzes Changed Files** - Identifies all files modified in the PR
3. **Performs AI Code Review** - Uses Copilot CLI to review code quality, security, and best practices
4. **Suggests Documentation Updates** - Analyzes changes and recommends README/documentation improvements
5. **Posts PR Comments** - Automatically comments on the PR with review results and documentation suggestions

## Key Features

- 🤖 **Automated Code Review**: Comprehensive analysis of code quality, security, and best practices
- 📝 **Documentation Analysis**: Intelligent suggestions for updating project documentation
- 💬 **PR Integration**: Posts detailed analysis directly as PR comments
- ⚡ **Non-interactive execution**: Runs completely automated using Copilot CLI flags
- 🔒 **Secure Authentication**: Uses GitHub's built-in tokens and secrets
- 🛡️ **Error Handling**: Continues workflow execution even if individual steps fail
- 📊 **Detailed Reporting**: Provides comprehensive analysis results and summaries

## How to use

1. **Create a Pull Request** - Open a PR against the main branch to trigger the workflow
2. **Manual trigger**: Go to Actions tab → "Copilot PR Review & Documentation" → "Run workflow"
3. **View results**: Check the PR comments for detailed analysis and suggestions
4. **Review logs**: View workflow logs for technical details and debugging information

## Setup Requirements

To use this workflow in your repository:

1. **GitHub Copilot CLI Access**: Ensure you have access to GitHub Copilot CLI
2. **Repository Secret**: Add `GH_COPILOT_CLI` secret with a GitHub token that has Copilot access
3. **Workflow Permissions**: Repository must allow GitHub Actions to write to pull requests

## What the Workflow Analyzes

### Code Review
- Code quality and structure
- Potential bugs and security issues
- Performance considerations
- Error handling and edge cases
- Code conventions and best practices
- Missing tests or documentation

### Documentation Analysis
- README.md updates needed
- New sections or examples required
- Installation/usage instruction updates
- API documentation changes
- Code snippet updates

## Technical Details

The workflow uses these key Copilot CLI features:
- `--prompt`: Executes prompts directly without interactive mode
- `--allow-all-tools`: Runs all tools automatically without confirmation
- Trusted directory configuration for seamless operation

## Example Output

When you create a PR, you'll automatically get a comment like:

```
## 🤖 Copilot PR Analysis
**Pull Request:** #123
**Branch:** feature/new-api

### 📋 Code Review
[Detailed code analysis and suggestions]

### 📝 Documentation Suggestions  
[Specific documentation improvement recommendations]
```

## Requirements

- GitHub repository with Actions enabled
- GitHub Copilot subscription (Pro, Business, or Enterprise)
- Copilot CLI policy enabled (for organization repos)

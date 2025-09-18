# GitHub Workflows

This directory contains GitHub Actions workflows for automating repository processes.

## add-to-project.yml

Automatically manages new issues by:

1. **Adding to Project**: Adds new issues to the configured GitHub project (requires setup)
2. **Auto-labeling**: Applies labels based on issue content and keywords

### Setup Required

To use the add-to-project functionality:

1. Replace `PROJECT_NUMBER` in the workflow file with your actual GitHub project number
2. Create a Personal Access Token (PAT) with appropriate permissions
3. Add the PAT as a repository secret named `ADD_TO_PROJECT_PAT`

### Labels Applied

- `triage`: Added to all new issues
- `new-issue`: Added to all new issues
- `bug`: Applied when title contains bug-related keywords
- `enhancement`: Applied when title contains feature-related keywords
- `documentation`: Applied when title contains documentation-related keywords
- `question`: Applied when title contains question-related keywords
- `copilot-studio`: Applied when title contains Copilot Studio-related keywords

### Permissions

The workflow requires:
- `issues: write` - To add labels to issues
- `contents: read` - To read repository content
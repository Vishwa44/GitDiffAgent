# GitDiffAgent

An AI-powered code review assistant that automatically analyzes commits and raises pull request with detailed feedback using GPT models.

## Usage

Open `main.ipynb` and run:

```python
from code_review_assistant import CodeReviewAssistant

assistant = CodeReviewAssistant(
    repo_name="owner/repository",      # e.g., "username/project"
    head_branch="feature-branch",      # Your changes branch
    base_branch="main",                # Target branch
    github_token=os.getenv("GITHUB_TOKEN")
)

# Create PR with automated review
pr_info = assistant.create_pull_request(draft=True)
print(f"Pull request created: {pr_info['pr_url']}")
```

## Features

- Automated code review using GPT models
- Detection of bugs, code smells, and style issues
- Code improvement suggestions with examples
- Automatic PR creation with detailed descriptions
- Inline code review comments

## Requirements

- Python 3.8+
- OpenAI API key
- GitHub token with repo access

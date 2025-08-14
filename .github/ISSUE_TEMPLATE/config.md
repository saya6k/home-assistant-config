blank_issues_enabled: false
contact_links:

- name: Support
  url: https://github.com/saya6k/home-assistant-config/discussions
  about: For questions or general support, use discussions.

issue_templates:

- name: Bug Report
  description: Report a bug or unexpected behavior
  title: "[BUG] "
  labels:

  - bug
    assignees:
  - saya6k
    body:
  - type: markdown
    attributes:
    value: |
    **Describe the bug**
    A clear and concise description of what the bug is.

  - type: input
    attributes:
    label: Steps to Reproduce
    description: Provide steps to reproduce the behavior
    placeholder: | 1. Go to '...' 2. Click '...' 3. Scroll down to '...' 4. See error
    required: true

  - type: input
    attributes:
    label: Expected behavior
    description: Describe what you expected to happen
    placeholder: e.g., The page loads without errors
    required: true

  - type: input
    attributes:
    label: Additional context
    description: Add any other context about the problem
    placeholder: e.g., Error logs, screenshots, or environment info
    required: false

- name: Feature Request
  description: Suggest an idea or improvement
  title: "[FEATURE] "
  labels:

  - enhancement
    assignees:
  - saya6k
    body:
  - type: markdown
    attributes:
    value: |
    **Describe the feature**
    A clear and concise description of what you want to happen.

  - type: input
    attributes:
    label: Problem it solves
    description: Explain the problem this feature would solve
    placeholder: e.g., Current workflow is slow
    required: true

  - type: input
    attributes:
    label: Alternatives considered
    description: Describe any alternative solutions you've considered
    placeholder: e.g., Using another library, manual workaround
    required: false

  - type: input
    attributes:
    label: Additional context
    description: Add any other context or screenshots
    placeholder: e.g., Mockups or references
    required: false

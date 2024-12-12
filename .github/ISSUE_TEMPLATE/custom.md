---
name: Bug Report
description: File a bug report
title: "[Bug]: "
labels: ["bug", "triage"]
projects: 
  - "octo-org/1"
  - "octo-org/44"
assignees:
  - octocat
body:
  - type: markdown
    attributes:
      value: |
        Thanks for taking the time to fill out this bug report!
  - type: input
    id: contact
    attributes:  # Added missing indentation and proper nesting
      label: Contact Details
      description: How can we get in touch with you if we need more info?
      placeholder: ex. email@example.com
      validations:
        required: false
  - type: textarea
    id: what-happened
    attributes:
      label: What happened?
      description: Also tell us, what did you expect to happen?
      placeholder: Tell us what you see!
      value: "A bug happened!"
      validations:
        required: true
  - type: dropdown
    id: version
    attributes:
      label: Version
      description: What version of our software are you running?
      options:
        - 1.0.2 (Default)
        - 1.0.3 (Edge)
      default: 1.0.2  # Updated "default" to match an actual option
      validations:
        required: true
  - type: dropdown
    id: browsers
    attributes:
      label: What browsers are you seeing the problem on?
      multiple: true
      options:  # Added the missing "options" field
        - Firefox
        - Chrome
        - Safari
        - Microsoft Edge

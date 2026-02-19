# Contributing to eNutri

Thank you for your interest in contributing to eNutri! We welcome contributions from researchers, developers, institutions, and the broader community. This guide outlines the various ways you can support and improve eNutri.

## Table of Contents
- [Get Started](#get-started)
- [Reporting Issues & Bugs](#reporting-issues--bugs)
- [Feature Requests](#feature-requests)
- [Direct Code Contributions](#direct-code-contributions)
- [Contributing Without Coding](#contributing-without-coding)
- [Contacting the Team](#contacting-the-team)
- [Advertising & Promoting eNutri](#advertising--promoting-enutri)
- [Community Guidelines](#community-guidelines)

## Get Started

Before contributing, please:

1. **Review our roadmap** at [.github/roadmap.md](.github/roadmap.md) to understand current development priorities and long-term vision
2. **Read our Code of Conduct** - We are committed to providing an inclusive and welcoming environment for all contributors
3. **Check existing issues** at https://github.com/eNutri/.github/issues to avoid duplicate reports

## Reporting Issues & Bugs

Found a bug? We'd love to hear about it!

### How to Report a Bug

1. **Go to [GitHub Issues](https://github.com/eNutri/.github/issues)**
2. **Click "New Issue"** and select the bug report template
3. **Provide the following information:**
   - Clear, descriptive title (e.g., "FFQ validation fails on Firefox")
   - Detailed description of the problem
   - Steps to reproduce the issue
   - Expected vs. actual behavior
   - Screenshots or error messages (if applicable)
   - Your environment:
     - Browser and version
     - Operating system
     - eNutri version/instance

### Bug Report Example
```
**Title:** Authentication fails with special characters in password

**Description:** Users cannot log in when their password contains certain special characters (e.g., @, #, $).

**Steps to Reproduce:**
1. Create account with password containing "@" symbol
2. Attempt to log in
3. Error appears on login page

**Expected Behavior:** User should log in successfully

**Actual Behavior:** "Invalid credentials" error message
```

## Feature Requests

Have an idea to improve eNutri?

1. **Go to [GitHub Issues](https://github.com/eNutri/.github/issues)**
2. **Click "New Issue"** and select the feature request template
3. **Describe your feature:**
   - Problem it solves for researchers
   - Proposed solution or implementation approach
   - Alternative approaches considered
   - Potential impact on users
   - Any relevant links or context

**Note:** Feature requests aligned with our roadmap may be prioritized faster. Check the [roadmap](.github/roadmap.md) first!



## Direct Code Contributions

We welcome pull requests! Here's how to contribute code:

### Prerequisites
- Git and GitHub account
- Node.js and npm (for building and testing)
- Familiarity with Angular 21, TypeScript, or the relevant technology stack
- Docker (for local development)

### Contribution Workflow

1. **Fork the repository** on GitHub
2. **Clone your fork locally:**
   ```bash
   git clone https://github.com/YOUR-USERNAME/enutri-enutri.git
   cd enutri-enutri
   ```

3. **Create a feature branch:**
   ```bash
   git checkout -b feature/your-feature-name
   # or for bug fixes:
   git checkout -b fix/bug-description
   ```

4. **Set up development environment:**
   ```bash
   # Follow setup instructions in README or DEVELOPMENT.md
   docker-compose up  # if available
   npm install
   ```

5. **Make your changes:**
   - Follow existing code style and patterns
   - Write clear, descriptive commit messages
   - Keep commits focused and atomic
   - Add tests for new functionality
   - Update documentation as needed

6. **Push to your fork:**
   ```bash
   git push origin feature/your-feature-name
   ```
7. **Open a Pull Request (PR):**
   - Use a clear, descriptive title
   - Reference related issues (e.g., "Fixes #123")
   - Describe what you changed and why
   - Include screenshots for UI changes
   - Ensure all tests pass before submitting

### Code Quality Standards
- **Test Coverage:** Aim for >80% code coverage
- **Accessibility:** Follow WCAG 2.2 guidelines
- **Documentation:** Comment complex logic; update READMEs

### Pull Request Process
1. Ensure your PR addresses a single concern
2. All GitHub Actions checks must pass
3. At least one maintainer review required
4. Feedback will be provided within 1-2 weeks
5. Merge after approval and conflicts resolved

## Contributing Without Coding

No coding skills? Many ways to help!

### Documentation
- Improve README clarity
- Translate documentation to other languages
- Add tutorial videos or blog posts
- Create deployment guides for specific platforms
- Document user workflows and best practices

### Food Database & Data
- Add regional food composition data
- Improve portion size photography and descriptions

### Research & Validation
- Conduct usability studies
- Validate eNutri with new populations
- Compare outputs with other dietary assessment tools
- Publish validation studies

## Community Guidelines

We are committed to fostering an inclusive, respectful community. All contributors must:

- **Be Respectful:** Treat all contributors with courtesy and professionalism
- **Be Inclusive:** Welcome diverse perspectives and backgrounds
- **Be Constructive:** Provide helpful feedback and solutions
- **Respect Privacy:** Do not share personal or sensitive information without consent
- **Follow Terms of Service:** Comply with GitHub's Community Guidelines

Violations of these guidelines may result in removal from the project.

## Recognition & Credits

Contributors are recognized in:
- Git commit history
- GitHub Contributors page
- Release notes for major contributions
- Author acknowledgments in publications

## Contacting the Team

### For Technical Issues
- **GitHub Issues:** https://github.com/eNutri/.github/issues

### For General Inquiries
- **Research team email:** enutri@reading.ac.uk

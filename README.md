# OWASP BLT Documentation

Official documentation for the OWASP Bug Logging Tool (BLT) project. This repository provides the MkDocs build and deployment infrastructure for the documentation site. Documentation content is sourced from the main [OWASP-BLT/BLT](https://github.com/OWASP-BLT/BLT) repository and merged at build time.

## 🌐 Live Documentation

Visit the live documentation at: [https://owasp-blt.github.io/documentation/](https://owasp-blt.github.io/documentation/)

## 📚 Documentation Structure

The documentation is organized into the following sections:

- **Getting Started**: Setup guides and project information
- **Features**: Overview of BLT features and capabilities (merged from [BLT/docs](https://github.com/OWASP-BLT/BLT/tree/main/docs))
- **User Guide**: Comprehensive guides for using BLT
  - Authentication and user management
  - Bug reporting and tracking
  - Leaderboards and statistics
  - Company management and bug hunts
  - Community features
  - Trademark search
- **Developer Guide**: Technical documentation for contributors (merged from [BLT/docs](https://github.com/OWASP-BLT/BLT/tree/main/docs))
  - Contributing guidelines
  - Bot setup instructions
  - Architecture overview
  - GitHub Actions workflows
  - GitHub webhook setup
- **Repositories**: Documentation for related BLT repositories
- **Personas**: User personas (merged from [BLT/docs](https://github.com/OWASP-BLT/BLT/tree/main/docs))

## 🗂️ Documentation Sources

Documentation content is sourced from two places and merged at build time:

1. **This repository (`BLT-docs/docs/`)** — User guides, getting started, repository overviews, and site configuration
2. **Main BLT repository (`BLT/docs/`)** — Technical docs: architecture, GitHub Actions, webhook setup, feature checklist, personas

The CI/CD workflow automatically checks out the [OWASP-BLT/BLT](https://github.com/OWASP-BLT/BLT) repository and copies its `docs/` content before building the site, so the live documentation always reflects the latest content from both sources.

> **Contributing to docs?** If you're adding or updating *technical* documentation (architecture, workflows, developer setup), please contribute to [OWASP-BLT/BLT/docs](https://github.com/OWASP-BLT/BLT/tree/main/docs). For user-facing guides, contribute here.

## 🛠️ Local Development

### Prerequisites

- Python 3.x
- pip

### Setup

1. Clone this repository:
   ```bash
   git clone https://github.com/OWASP-BLT/BLT-docs.git
   cd BLT-docs
   ```

2. Clone the BLT repository and copy its docs:
   ```bash
   git clone --depth 1 https://github.com/OWASP-BLT/BLT.git blt-repo

   # Copy BLT docs into the local docs directory
   cp blt-repo/docs/architecture.md docs/developer-guide/architecture.md
   cp blt-repo/docs/github_actions.md docs/developer-guide/github-actions.md
   cp blt-repo/docs/github-webhook-setup.md docs/developer-guide/github-webhook-setup.md
   cp blt-repo/docs/feature-checklist.md docs/features/feature-checklist.md
   cp blt-repo/docs/features.md docs/features/blt-features.md
   cp blt-repo/docs/file-descriptions.csv docs/developer-guide/file-descriptions.csv
   mkdir -p docs/personas
   cp blt-repo/docs/Personas/"Alex Rivera - aspiring tester" docs/personas/alex-rivera-aspiring-tester.md
   cp blt-repo/docs/Personas/"Frank Patel - Startup Founder" docs/personas/frank-patel-startup-founder.md
   cp blt-repo/docs/Personas/"Harold - OWASP projects lead" docs/personas/harold-owasp-projects-lead.md
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Serve the documentation locally:
   ```bash
   mkdocs serve
   ```

5. Open your browser and navigate to `http://127.0.0.1:8000/`

### Building

To build the static site:

```bash
mkdocs build
```

The built site will be in the `site/` directory.

## 🚀 Deployment

Documentation is automatically deployed to GitHub Pages when changes are pushed to the `main` branch. The deployment is handled by GitHub Actions (see `.github/workflows/deploy-docs.yml`).

The workflow:
1. Checks out this repository (mkdocs configuration and user-facing docs)
2. Checks out the [OWASP-BLT/BLT](https://github.com/OWASP-BLT/BLT) repository
3. Copies technical docs from `BLT/docs/` into the local `docs/` directory
4. Builds the documentation site with MkDocs
5. Deploys to GitHub Pages

### GitHub Pages Setup

To enable GitHub Pages for this repository:

1. Go to repository **Settings** → **Pages**
2. Under **Source**, select **Deploy from a branch**
3. Select branch: **gh-pages** and folder: **/ (root)**
4. Click **Save**

The workflow will automatically create and maintain the `gh-pages` branch with the built documentation.

## 📝 Contributing

We welcome contributions to improve the documentation! To contribute:

1. Fork this repository (or the BLT repository for technical docs)
2. Create a new branch for your changes
3. Make your changes to the markdown files in the `docs/` directory
4. Test your changes locally with `mkdocs serve`
5. Submit a pull request

### Documentation Guidelines

- Use clear, concise language
- Include code examples where appropriate
- Add screenshots for UI-related documentation
- Follow the existing structure and formatting
- Test your changes locally before submitting

## 🔧 Technology Stack

- **Framework**: [MkDocs](https://www.mkdocs.org/)
- **Theme**: [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/)
- **Hosting**: GitHub Pages
- **CI/CD**: GitHub Actions

## 🔗 Related Links

- [OWASP BLT Main Repository](https://github.com/OWASP-BLT/BLT)
- [BLT/docs (technical documentation source)](https://github.com/OWASP-BLT/BLT/tree/main/docs)
- [OWASP BLT Website](https://owaspblt.org)
- [OWASP Slack](https://owasp.org/slack/invite)

## 📄 License

This documentation is part of the OWASP BLT project and follows the same licensing terms.

## 💬 Support

For questions or issues related to the documentation:

- Open an issue in this repository
- Join the OWASP Slack and visit the BLT channel
- Refer to the main BLT repository for project-related questions
# OWASP BLT Documentation

Official documentation for the OWASP Bug Logging Tool (BLT) project. This repository contains comprehensive documentation for users and developers.

## 🌐 Live Documentation

Visit the live documentation at: [https://owasp-blt.github.io/documentation/](https://owasp-blt.github.io/documentation/)

## 📚 Documentation Structure

The documentation is organized into the following sections:

- **Getting Started**: Setup guides and project information
- **Features**: Overview of BLT features and capabilities
- **User Guide**: Comprehensive guides for using BLT
  - Authentication and user management
  - Bug reporting and tracking
  - Leaderboards and statistics
  - Company management and bug hunts
  - Community features
  - Trademark search
- **Developer Guide**: Technical documentation for contributors
  - Contributing guidelines
  - Bot setup instructions
  - Development environment setup
  - Architecture overview
  - GitHub Actions workflows
  - GitHub webhook setup
- **Repositories**: Documentation for related BLT repositories
- **Personas**: User personas for the BLT platform

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

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Serve the documentation locally:
   ```bash
   mkdocs serve
   ```

4. Open your browser and navigate to `http://127.0.0.1:8000/`

### Building

To build the static site:

```bash
mkdocs build
```

The built site will be in the `site/` directory.

## 🚀 Deployment

Documentation is automatically deployed to GitHub Pages when changes are pushed to the `main` branch. The deployment is handled by GitHub Actions (see `.github/workflows/deploy-docs.yml`).

### GitHub Pages Setup

To enable GitHub Pages for this repository:

1. Go to repository **Settings** → **Pages**
2. Under **Source**, select **Deploy from a branch**
3. Select branch: **gh-pages** and folder: **/ (root)**
4. Click **Save**

The workflow will automatically create and maintain the `gh-pages` branch with the built documentation.

## 📝 Contributing

We welcome contributions to improve the documentation! To contribute:

1. Fork this repository
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

## 📖 Documentation Source

The documentation content is sourced from the main [OWASP-BLT/BLT](https://github.com/OWASP-BLT/BLT) repository:

- Technical docs from `docs/` directory
- User guides from `website/documents/` directory

## 📄 License

This documentation is part of the OWASP BLT project and follows the same licensing terms.

## 🔗 Related Links

- [OWASP BLT Main Repository](https://github.com/OWASP-BLT/BLT)
- [OWASP BLT Website](https://owaspblt.org)
- [OWASP Slack](https://owasp.org/slack/invite)

## 💬 Support

For questions or issues related to the documentation:

- Open an issue in this repository
- Join the OWASP Slack and visit the BLT channel
- Refer to the main BLT repository for project-related questions
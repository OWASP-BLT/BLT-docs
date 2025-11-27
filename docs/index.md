<h1 align="center"> 🐛 OWASP BLT </h1>
<h3 align="center">Bug Logging Tool - Democratizing Bug Bounties</h3>

<p align="center">
  <strong>A community-driven platform for discovering, reporting, and tracking security vulnerabilities</strong>
</p>

<p align="center">
  <a href="https://owaspblt.org">🌐 Website</a> •
  <a href="https://github.com/OWASP-BLT/BLT/blob/main/CONTRIBUTING.md">📖 Contributing Guide</a> •
  <a href="https://owasp.org/slack/invite">💬 Join Slack</a> •
  <a href="https://github.com/OWASP-BLT/BLT/issues">🐛 Report Bug</a>
</p>

---

## 💡 Our Philosophy

At OWASP BLT, we believe in building software that is **lightweight**, **organized**, and **cost-effective**. We embrace modern infrastructure approaches in the following order of preference:

1. **🚀 Serverless First** - Our first choice is serverless architecture (Cloudflare Workers, AWS Lambda, etc.) for its scalability, minimal maintenance, and pay-per-use pricing model
2. **🖥️ VPS Second** - When serverless isn't suitable, we opt for Virtual Private Servers for their balance of control and cost-effectiveness
3. **☁️ Cloud Third** - Full cloud services are used when the complexity and features justify the additional cost

This approach ensures we remain agile, minimize operational overhead, and maximize value for our community.

---

## 🎯 What is OWASP BLT?

**OWASP BLT (Bug Logging Tool)** is an open-source platform that democratizes bug bounties and security research. Built by the community for the community, BLT makes it easy for security researchers, developers, and organizations to collaborate on finding and fixing security vulnerabilities.

### ✨ Key Features

- 🔍 **Bug Discovery & Reporting** - Discover and report security vulnerabilities across various applications and websites
- 🏆 **Rewards & Recognition** - Earn rewards, badges, and recognition for your contributions to web security
- 👥 **Community Driven** - Join a vibrant community of security researchers and developers
- 🎮 **Gamification** - Leaderboards, challenges, and competitions to make security research engaging
- 💰 **Staking System** - Innovative blockchain-based reward system for contributors
- 📊 **Comprehensive Dashboard** - Track your progress, statistics, and impact
- 🌐 **Open Source** - Built with transparency and collaboration at its core
- 🛡️ **OWASP Project** - Part of the Open Worldwide Application Security Project family

---

## 🚀 Quick Start

### Prerequisites
- Python 3.11.2+
- PostgreSQL
- Docker & Docker Compose (recommended)

### Installation

#### Using Docker (Recommended)
```bash
# Clone the repository
git clone https://github.com/OWASP-BLT/BLT.git
cd BLT

# Configure environment
cp .env.example .env

# Build and start
docker-compose build
docker-compose up
```

Access the application at **http://localhost:8000**

#### Using Poetry
```bash
# Install dependencies
pip install poetry
poetry shell
poetry install

# Set up database
python manage.py migrate
python manage.py loaddata website/fixtures/initial_data.json
python manage.py createsuperuser

# Run the server
python manage.py runserver
```

For detailed setup instructions, see our [Contributing Guide](https://github.com/OWASP-BLT/BLT/blob/main/CONTRIBUTING.md).

---

## 🤝 Contributing

We welcome contributions from everyone! Whether you're fixing bugs, adding features, improving documentation, or spreading the word, your help is appreciated.

- 📚 Read our [Contributing Guide](https://github.com/OWASP-BLT/BLT/blob/main/CONTRIBUTING.md)
- 🐛 Check out [open issues](https://github.com/OWASP-BLT/BLT/issues)
- 💡 Look for issues tagged with `good first issue` if you're new
- 🎨 Follow our coding standards (Black, isort, ruff)
- ✅ Run `pre-commit` before submitting changes

---

## 💬 Community & Support

- 🌐 **Website**: [owaspblt.org](https://owaspblt.org)
- 💬 **Slack**: [Join OWASP Slack](https://owasp.org/slack/invite)
- 🐦 **Twitter**: [@OWASP_BLT](https://twitter.com/OWASP_BLT)
- 💰 **Sponsor**: [Support the project](https://github.com/sponsors/OWASP-BLT)
- 📧 **Contact**: Reach out through GitHub issues

---

## 📈 Star History

<a href="https://star-history.com/#OWASP-BLT/BLT&Date">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=OWASP-BLT/BLT&type=Date&theme=dark" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=OWASP-BLT/BLT&type=Date" />
   <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=OWASP-BLT/BLT&type=Date" />
 </picture>
</a>

---

## 📄 License

This project is licensed under the **AGPL-3.0 License** - see the [LICENSE.md](https://github.com/OWASP-BLT/BLT/blob/main/LICENSE.md) file for details.

---

<p align="center">
  <strong>⭐ Star this repository if you find it helpful!</strong><br>
  Made with ❤️ by the OWASP BLT Community
</p>

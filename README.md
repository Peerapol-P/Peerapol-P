## Hi there 👋
[![My Skills](https://skillicons.dev/icons?i=angular,react,tailwind,spring,postgres)](https://skillicons.dev)
<!--
**Peerapol-P/Peerapol-P** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
# 📌 Git Workflow Standard

To maintain software quality, ensure high stability, and facilitate a seamless CI/CD pipeline, our development team follows a **Gitflow Variant** workflow tailored for multi-environment deployments. All developers are expected to adhere to these standards.

---

## 🌲 Branch Structure

Our repository is structured around 4 main types of branches, each mapped to a specific environment:

| Branch Name | Target Environment | Description |
| :--- | :--- | :--- |
| `production` | **Production** | The most stable branch. Contains production-ready code currently live. *(Direct commits are strictly prohibited).* |
| `staging` | **Staging / UAT** | Used for integrated testing, QA verification, and User Acceptance Testing (UAT). |
| `development` | **Development** | The main integration branch for developers. Used for initial feature merging and internal testing. |
| `feature/*` | **Local / Sandbox** | Isolated branches used to develop specific features, tasks, or bug fixes. |

> ⚠️ **Note:** The `master` or `main` branch (if present) serves only as the initial project baseline. All active development, testing, and deployments track the environment branches listed above.

---

## 🔄 Workflow Steps

### 1. Start a New Task (Create a Feature Branch)
Always start by pulling the latest changes from `development` and branching off from it.
```bash
# Update your local development branch
git checkout development
git pull origin development

# Create your feature branch
git checkout -b feature/JIRA-123-login-page

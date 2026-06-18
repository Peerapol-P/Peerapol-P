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
# 📌 Git Workflow Standard (Develop -> SIT -> UAT -> Production)

To ensure a seamless development process, structured testing, and secure production deployments, our team adheres to a branch environment-based workflow. All developers are expected to follow these standards.

---

## 🌲 Branch Structure

Our repository is structured around 5 main types of branches, each mapped directly to a specific deployment environment:

| Branch Name | Target Environment | Description |
| :--- | :--- | :--- |
| `production` | **Production** | The most stable branch. Contains production-ready code currently live. *(Direct commits are strictly prohibited).* |
| `uat` | **User Acceptance Testing** | Used for business validation, product owners (PO), and client sign-off. |
| `sit` | **System Integration Testing**| Dedicated environment for the QA/Testing team to perform integration and regression testing. |
| `development` | **Development** | The main integration branch for developers. Used for initial feature merging and internal testing. |
| `feature/*` | **Local / Sandbox** | Isolated branches used to develop specific features, tasks, or bug fixes. |

> ⚠️ **Note:** The `master` or `main` branch serves only as the initial project baseline. All active development, testing, and CI/CD pipelines track the environment branches listed above.

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

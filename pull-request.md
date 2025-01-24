# Contributing to the `umsi-arwhyte` Repository

## Workflow Instructions

This repository uses a **fork-and-pull-request model**. Follow these steps to ensure proper contribution:

---

### 1. Fork the Repository
- Go to the GitHub page for the `umsi-arwhyte` repository.
- Click on the **Fork** button (located in the upper-right corner).
- This creates a copy of the repository in your GitHub account.

---

### 2. Clone Your Fork
- Copy the URL of your fork (e.g., `https://github.com/<your-username>/<github repo>.git`).
- Clone the forked repository to your local machine:
  ```bash
  git clone https://github.com/<your-username>/<github repo>.git
  ```
- Navigate to the project directory (depending in your file system, can be skipped):
  ```bash
  cd umsi-arwhyte
  ```

---

### 3. Add the Upstream Repository
- Add the original repository (`umsi-arwhyte`) as an upstream remote:
  ```bash
  git remote add umsi-arwhyte https://github.com/umsi-arwhyte/<github repo>.git
  ```
- Verify the remotes:
  ```bash
  git remote -v
  ```
  You should see something like:
  ```
  origin    https://github.com/<your-username>/umsi-arwhyte.git (fetch)
  origin    https://github.com/<your-username>/umsi-arwhyte.git (push)
  umsi-arwhyte  https://github.com/umsi-arwhyte/umsi-arwhyte.git (fetch)
  umsi-arwhyte  https://github.com/umsi-arwhyte/umsi-arwhyte.git (push)
  ```

---

### 4. Create a New Branch
- Always create a new branch for your changes:
  ```bash
  git checkout -b <new-branch-name>
  ```

---

### 5. Make Changes
- Make your changes or additions to the codebase.
- Stage the changes:
  ```bash
  git add .
  ```
- Commit the changes with a meaningful message:
  ```bash
  git commit -m "Describe what you changed"
  ```

---

### 6. Push Changes to Your Fork
- Push your branch to your forked repository:
  ```bash
  git push origin <new-branch-name>
  ```

---

### 7. Open a Pull Request
- Go to your forked repository on GitHub.
- Click the **Compare & pull request** button.
- Ensure the target branch is the `main` branch of the `umsi-arwhyte` repository.
- Add a clear title and description to your pull request.
- Submit the pull request.

---

### 8. Wait for Code Review
- Wait for maintainers to review your pull request.
- Address any feedback provided by the reviewers:
  - Make necessary changes locally.
  - Push updates to the same branch:
    ```bash
    git push origin <new-branch-name>
    ```

---

### 9. Keep Your Fork Up to Date
- Regularly update your fork with changes from the upstream repository:
  ```bash
  git fetch upstream
  git checkout main
  git merge upstream/main
  ```
- Push the updated `main` branch to your fork:
  ```bash
  git push origin main
  ```

---

Following these steps ensures that your contributions align with the repository's workflow. If you have questions, reach out to the maintainers for guidance.

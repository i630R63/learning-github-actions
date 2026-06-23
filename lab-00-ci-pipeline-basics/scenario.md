### CI Workflow Configuration Challenge

You are designing a Continuous Integration (CI) workflow for your team. You have three main tasks: preparing the environment, running heavy tests, and finally, deploying. By default, GitHub Actions will try to run everything in parallel, but that would break the process. Additionally, the team has complained that sometimes the tests get stuck in an infinite loop, consuming all their billing minutes.

**Your Requirements:**

* **Trigger:** Create a workflow that triggers on every push to your repository.
* **Structure:** The workflow must contain three jobs: `preparation`, `tests`, and `deployment`.
* **Execution Order:** You must force them to run strictly in this order: `preparation` first, followed by `tests`, and finally `deployment`.
* **Protection:** Protect the `tests` job by setting a strict execution time limit of 5 minutes. (Use commands like `sleep 400` in your `run` scripts to test what happens if a script takes longer than 5 minutes).

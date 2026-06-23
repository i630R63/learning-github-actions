### Scenario: Manual Deployment Trigger

The QA team has requested a button in the GitHub interface to trigger deployments to different environments on-demand, without the need to push new commits. They need to be able to choose between "development" and "production" environments.

**Your Requirements:**

* **Manual Trigger:** Create a workflow that can only be executed manually from the GitHub UI (workflow_dispatch).
* **Input Parameter:** Add an input parameter called `entorno_elegido` (chosen_environment) of type `choice`, offering "desarrollo" (development) and "producción" (production) as options.
* **Action:** In the workflow's single job, add a step that prints the environment selected by the user to the console.

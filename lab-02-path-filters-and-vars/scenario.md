### Path Filters and Variable Scoping

**Scenario:**
You have a project where source code and documentation are mixed. You don't want to waste resources running the entire pipeline if someone only fixes a typo in the documentation. Additionally, you are having some confusion regarding environment variable scoping between different steps.

**Your Requirements:**

* **Path Filter:** The workflow should trigger on a `push`, but *only* if the changes affect the `src/` directory. If changes are made only to the `docs/` directory, the workflow should not trigger.
* **Global Variable:** Define an environment variable called `MENSAJE` at the global (workflow) level with the value "Hola desde el workflow".
* **Scoped Variable:** Create one job with two steps. In the second step, define another variable also called `MENSAJE` with the value "Hola desde el paso".
* **Verification:** Make both steps print the value of the `MENSAJE` variable to the console to observe the override behavior.

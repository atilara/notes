- Introduction
	- Provides automation to a git repository
	- continuous integration (**CI**)
	- continuous delivery (**CD**)
	- infra as code (**IaC**)
- How GitHub Actions automate tasks?
	- GitHub helps in the team **communication**
	- GitHub Actions helps the **automation process**
		- All the tasks that must be done *after* the code is written
	- Scripts to automate tasks in a software development workflow
- Types of GitHub Actions
	- Container actions
	- JavaScript Actions
	- Composite Actions
- Structure of a GitHub Action:
  ![Image of a GitHub Actions workflow file showing the job, step, and action components.](https://learn.microsoft.com/en-us/training/github/github-actions-automate-tasks/media/github-actions-workflow-components.png)
- Schedule Workflows
  ![Diagram of the five unit-of-time fields for scheduling an event in a workflow file.](https://learn.microsoft.com/en-us/training/github/github-actions-automate-tasks/media/scheduled-events.png){:height 210, :width 615}
  
  Run every 15min:
  ```yml
  on:
    schedule:
      - cron:  '*/15 * * * *'
  ```
- Workflows can be configured to run based on triggers
	- Push
	- PR
	- Review
	- Merge
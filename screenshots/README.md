# Task 6 evidence screenshots

## Links
- PR: https://github.com/Petliuk/devops_todolist_cicd_task_6_polish_pipeline/pull/1
- Successful PR CI run: https://github.com/Petliuk/devops_todolist_cicd_task_6_polish_pipeline/actions/runs/35145891751
- Successful main pipeline (with staging approval): https://github.com/Petliuk/devops_todolist_cicd_task_6_polish_pipeline/actions/runs/35147259555

## Screenshots

| File | Requirement |
|------|-------------|
| `01a-branch-protection-list.png` | Branch protection on `main` |
| `01-branch-protection-rule.png` | Require pull request before merging |
| `01b-branch-protection-python-ci.png` | Required status check `Python CI` |
| `02-staging-manual-approval.png` | Staging environment required reviewers |
| `03-pr-checks.png` | PR matrix checks (Ubuntu/Windows + Python CI) |
| `04-pr-merge-ready.png` | PR ready to merge after checks |
| `05-staging-waiting-approval.png` | Staging deploy waiting for review |
| `06-staging-approve-dialog.png` | Manual Approve and deploy dialog |
| `07-full-pipeline-success.png` | Full main pipeline success |

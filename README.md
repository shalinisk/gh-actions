# gh-actions

Github action snippets for reference

## Notes

Every job runs on its own runner, so you can't share data between jobs. You can use artifacts to pass data between jobs.

Expressions - (<https://docs.github.com/en/actions/learn-github-actions/expressions>)

Multiline strings cannot be passed directly between jobs.

Pull-requests based on forks do not trigger a workflow

You can skip a workflow by adding `[skip ci]` or something similar to the commit message

## Todo

Terraform has state file so only one workflow can run at a time. Need to figure out how to check if any workflow is running and wait for it to finish.

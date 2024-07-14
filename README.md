# gh-actions

Github action snippets for reference

## Notes

Every job runs on its own runner, so you can't share data between jobs. You can use artifacts to pass data between jobs.

Expressions - (<https://docs.github.com/en/actions/learn-github-actions/expressions>)

Multiline strings cannot be passed directly between jobs.

Pull-requests based on forks do not trigger a workflow

You can skip a workflow by adding `[skip ci]` or something similar to the commit message

Job artifacts can be downloaded manually (UI or rest api) or automatically (i.e. an action in the workflow)
They are not available across jobs, so you need to download them in a subsequent job where you want to use them
If the name input parameter is not provided, all artifacts will be downloaded

```python
print(f'::set-output name=outputval01::{result}')
```

Environment variables can be at workflow level or job level

There is an option to set the default shell i.e. bash or python etc.,
You can't overwrite the value of the default environment variables named GITHUB*\* and RUNNER*\*

Secrets can be set at repo level but that is not scalable
Instead set them at environment level

At job level, specify the environment that contains the related secrets

Custom actions - javascript or docker container or composite actions

By default a workflow has write access to the repo that contains it except for pull_request events

## Questions

1. Can artifacts be encrypted or protected?

### Areas of use

- website deployment
- linting
- Dependabots
- deploy a dev pod
- daily routines
- rss feeds?

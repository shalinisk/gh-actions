# Self-hosted runners

## Setup

[Request token automatically](https://stackoverflow.com/questions/74031457/generate-github-self-hosted-runner-token-automatically)

[Agent-as-a-service](https://docs.github.com/en/actions/hosting-your-own-runners/managing-self-hosted-runners/configuring-the-self-hosted-runner-application-as-a-service)

[API calls for runners](https://docs.github.com/en/rest/actions/self-hosted-runners?apiVersion=2022-11-28)

[Scaling runners](https://github.com/actions/actions-runner-controller/blob/master/docs/automatically-scaling-runners.md)

```
./config.sh --url https://github.com/octo-org --token example-token --ephemeral
```

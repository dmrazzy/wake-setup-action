# Wake Setup GitHub Action

![white](https://github.com/Ackee-Blockchain/wake-setup-action/assets/56036748/d3d00a13-e1ce-40f9-a6c7-1dfd11bd4991)


A GitHub action to set up an environment on the runner for the usage of Wake in subsequent steps.

## Usage

To use this action in your GitHub workflows, you can refer to it in your workflow file. Here is an example of how to use it in a workflow:

```yaml
on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v2

      - name: Setup Wake environment
        uses: Ackee-Blockchain/wake-setup-action@0.1.0

      - name: Wake up
        run: wake --version
```

In the above example, the action is used after the code is checked out to set up an environment (install Wake and Foundry) and in the last step the `wake` command is executed.

## Limitations

- Currently, the action only takes the latest version of Wake for the sake of the newest detectors and features.

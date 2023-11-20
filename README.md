# Wake Setup GitHub Action
A GitHub action to set up an environment on the runner for the usage of Wake in subsequent steps.

## Usage
To use this action in your GitHub workflows, you can refer to it in your workflow file. Here is an example of how to use it in a workflow:

```
on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v2

      - name: Setup Wake environment
        uses: Ackee-Blockchain/wake-setup-action@0.0.1

      - name: Wake up
        run: wake --version
```

In the above example, the action is used after the code is checked out to set up an environment (install Wake and Foundry) and in the last step the `wake` command is executed.
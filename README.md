# README

## How to run multiple lines in Github Action:
Use `|` to indicate that the following lines should be treated as a single string. 

EXAMPLE: 

```yml
name: My Workflow
on: push

jobs:
  my-job:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v2
      - name: Install dependencies
        run: |
          npm install
          pip install -r requirements.txt
      - name: Run tests
        run: |
          pytest
          npm test
```
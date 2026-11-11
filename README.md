# GitHub Actions CI Demo

A small Python project that demonstrates a CI pipeline with GitHub Actions.

## Structure
```
ci-demo/
├── .github/workflows/ci.yml   # CI workflow
├── app/calculator.py          # Simple code to test
├── tests/test_calculator.py   # Unit tests
├── pytest.ini
├── requirements.txt
└── README.md
```

## What the workflow does
On every push or pull request to `main`:
1. Checks out the code
2. Sets up Python (3.10, 3.11, 3.12)
3. Installs dependencies
4. Lints with flake8
5. Runs tests with pytest

## Run locally
```
pip install -r requirements.txt
pytest -v
```

## Push to GitHub
```
git init
git add .
git commit -m "Add CI demo"
git branch -M main
git remote add origin <your-repo-url>
git push -u origin main
```
Then open the **Actions** tab in your repo to see the workflow run.

# Gitleaks Rules

> custom rules

## Usage

create a github action for your repo in `.github/workflows/.gitleaks.yml`

```
name: gitleaks

on: [push,pull_request]

jobs:
  gitleaks:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v1
    - name: wget
      uses: wei/wget@v1
      with:
        args: -N -O .gitleaks.toml https://raw.githubusercontent.com/ycjcl868/gitleaks/master/.gitleaks.toml
    - name: gitleaks-action
      uses: zricethezav/gitleaks-action@master
```

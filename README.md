# AMI Example Repository

This repository demonstrates the split GitHub Actions workflow that:

1. Detects changes to any AMI JSON under `amis/`
2. Fires one repository_dispatch per added/removed pair
3. Processes each pair individually in a second workflow

Push this repo to GitHub and ensure `Actions` are enabled. Modify or add JSON
files under `amis/` and observe Actions behaviour.

## Structure

```bash
.
├── amis/
│   ├── al2023.json
│   ├── ubuntu2204.json
│   └── windows2019.json
├── .github/workflows/
│   ├── ami-detector.yml
│   └── ami-per-pair.yml
├── scripts/
│   └── deploy-ami.sh
└── ami-ledger.txt
```

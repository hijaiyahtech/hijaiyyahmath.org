# Hijaiyyah Auditor Bundle (Offline-Ready)

## One-command audit

### Linux/macOS
```bash
chmod +x scripts/audit.sh
./scripts/audit.sh
```

### Windows (PowerShell)
```powershell
powershell -ExecutionPolicy Bypass -File .\scripts\audit.ps1
```

## What this does
1. Creates `.venv`
2. Installs dependencies from `requirements.lock.txt`
3. Installs HL-18 (editable)
4. Runs `scripts/verify_all.py` (Integrity + PASS + TRAP CORE-1)
5. Runs `scripts/run_full_demo.py` (audit letter + audit word; saves artifacts)

## Outputs
- `artifacts/verify_all/`
- `artifacts/runs/`
- `artifacts/audit_wrapper.log`

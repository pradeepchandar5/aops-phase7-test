# Self-Heal Patch

**Incident:** High CPU on API server after deploy
**Origin:** self_heal
**Severity:** high

**RCA:**
```json
{}
```

## Rollback Plan
```json
{
  "L1": {
    "desc": "Restart service / revert config",
    "cmd": "bash scripts/rollback.sh L1 aops-phase7-test"
  },
  "L2": {
    "desc": "Git revert the suspect commit + redeploy",
    "cmd": "bash scripts/rollback.sh L2 aops-phase7-test"
  },
  "L3": {
    "desc": "Full restore from last known-good artifact",
    "cmd": "bash scripts/rollback.sh L3"
  }
}
```

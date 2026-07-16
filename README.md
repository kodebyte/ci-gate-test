# ci-gate-test

Throwaway repo for exercising Vessl's **"Wait for CI"** deploy gate end-to-end.

The CI workflow **fails** when the pushed commit message contains `[fail]`, and
**passes** otherwise. That lets a single repo drive both gate outcomes:

- push a `[fail]` commit → CI red → Vessl marks the deploy `ci_failed`
- push a normal commit → CI green → Vessl releases the parked deploy

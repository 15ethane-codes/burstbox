# Burstbox plan

Single-node job scheduler that runs untrusted code in resource-limited containers. Learning project. Started Nov 2026.

## Phase 0: walking skeleton (Thanksgiving 2026)
Done: `submit "echo hi"` runs the command locally and shows output and exit code. Tests pass, CI is green, README explains how to run it.

## Phase 1: real queue (winter break 2026-27)
Done: submit 100 jobs, run 3 workers, no job runs twice. Kill a worker mid-job and the job comes back and finishes. A test proves it.

## Phase 2: sandbox (spring 2027)
Done: each job runs in a container with CPU, memory, and time limits. A job that eats memory or loops forever is killed and marked failed with a clear reason. Threat model note written.

## Phase 3: API and scheduler (summer 2027)
Done: HTTP API with API-key auth, Docker Compose to run everything, three scheduling policies, workload generator, and a decision note comparing policies with measured results. Checkpoint: decide what comes next.

## Phase 4: cloud and observability (fall 2027 to winter)
Done: stack deployed to one cloud VM, metrics and dashboards, billing alert set first.

## Phase 5: AI features (spring 2028)
Done: one or two AI features, each with an eval against a baseline.

## Phase 6: Kubernetes (summer 2028)
Done: workers running as Kubernetes Jobs locally, compared against my own scheduler.

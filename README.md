# aml-triage-agent

An LLM agent that triages transaction-monitoring alerts the way an AML
investigator does: pull the customer profile and transaction history, screen
sanctions/PEP lists, compare against prior alerts and peer baselines, then
recommend **close / escalate / needs human review** with a draft narrative and
cited evidence.

All data is synthetic. No real customer data, bank rules, or internal documents
are used.

## Status

Week 1: synthetic data generator, rule engine, FastAPI skeleton.

## Roadmap

- **v0** — synthetic data + rules + single LLM call for a disposition
- **v1** — tool-use agent, labeled eval set with regression script, audit log, FastAPI, Docker, deployed
- **v2** — cost/latency work (caching, parallel tool calls, model routing), write-up of eval results

## Run

```bash
uv run pytest
```

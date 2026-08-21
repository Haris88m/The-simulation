# Open Protocol: `WORLD/1`

`WORLD/1` is the model-independent exchange protocol between any client and the authoritative simulation server.

MCP, REST, a browser, a command-line tool, a local-model adapter, or encoded copy/paste are transport adapters. None of them owns the game state.

## Principle

> The AI is an interchangeable interpreter. The server is the universe.

A player may begin through one model and continue through another because node identity, world state, history, permissions, and receipts live on the server.

## Example intervention

```json
{
  "protocol": "WORLD/1",
  "action": "ACT",
  "node_id": "N-047821",
  "world_id": "W-81A29F",
  "origin": "HUMAN_AI_COMBINED",
  "epistemic_class": "INTERVENTION",
  "payload": {
    "actor": "BALKAN_REGION",
    "domain": "ENERGY",
    "operation": "BUILD_SHARED_RESERVE",
    "magnitude": 184,
    "horizon_months": 120,
    "premise": "Create a coordinated regional energy reserve."
  }
}
```

## Canonical actions

- `JOIN`
- `OBSERVE`
- `ACT`
- `SUBMIT_EVIDENCE`
- `FORK`
- `REQUEST_MERGE`
- `APPROVE_MERGE`
- `CREATE_FORECAST`
- `SYNC`
- `VERIFY`

## Provenance

The ledger records whether an action originated from a human, an AI, a human–AI collaboration, or the system. No source receives automatic truth status.

## Authority

Only signed server results are authoritative. An AI may summarize a result incorrectly; the signed state transition and checkpoint remain the canonical record.

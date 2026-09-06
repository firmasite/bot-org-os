# Artifact bus — phases + HANDOFF loop

Chat is control. Files are the bus.

```mermaid
flowchart TB
  OP[Operator ask] --> CH[Chief]
  CH -->|assign one owner| PH[Phase specialist]
  PH --> ART[Artifact file<br/>workspace/phase/]
  ART --> HO[HANDOFF<br/>Source · Evidence · Action]
  HO --> CH
  CH -->|collect| LOG[ACTION_LOG]
  CH -->|Action PENDING| OP
  CH -->|done| OP

  subgraph bus["Artifacts bus"]
    A1[analysis/]
    A2[planning/]
    A3[solutioning/]
    A4[implementation/]
    A5[handoffs/]
    A6[org/]
  end

  PH -.-> bus
```

**Close needs:** Artifact path + HANDOFF with three gates. Chat-only handoffs are refused.

HTML (Archify): [artifact-bus.html](artifact-bus.html) when present.

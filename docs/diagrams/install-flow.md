# Install flow — paste INSTALL-PROMPT → Bootstrap → Chief + specialists

Pasting [`INSTALL-PROMPT.md`](../../INSTALL-PROMPT.md) is the install trigger. A bare GitHub URL is not enough.

```mermaid
flowchart LR
  A[Paste INSTALL-PROMPT<br/>into a Bot] --> B[Read AGENTS.md]
  B --> C[Run BOOTSTRAP.md]
  C --> D[Create workspace folders]
  C --> E[Copy playbooks + roster]
  C --> F[Install Skills]
  C --> G[Become Chief<br/>+ 4 specialists]
  C --> H[Create Core Team channel]
  D --> I[INSTALL-STATUS.md]
  E --> I
  F --> I
  G --> I
  H --> I
  I --> J[Tell Operator]

  subgraph opt["Optional tools — Operator chooses"]
    direction TB
    O1[Grok Build CLI]
    O2[GitHub CLI gh]
    O3[Cloud / coding agents]
    O4[Other connectors later]
  end

  J -.-> opt
```

**Paste:** the block in [`INSTALL-PROMPT.md`](../../INSTALL-PROMPT.md)

**Order:** Become Chief, then CreateAgent Analyst → Product Manager → Architect → Developer. Do not CreateAgent a Chief.

Extended Bots are **not** created on first install.

Optional tools are **not** part of Core success. See [OPTIONAL-TOOLS.md](../OPTIONAL-TOOLS.md).

HTML (Archify): [install-flow.html](install-flow.html) when present.

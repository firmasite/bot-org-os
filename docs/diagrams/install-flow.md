# Install flow — paste URL → Bootstrap → Bots / Skills / folders

Linking the repo is the install trigger.

```mermaid
flowchart LR
  A[Paste repo URL<br/>into a Bot] --> B[Read AGENTS.md]
  B --> C[Run BOOTSTRAP.md]
  C --> D[Create workspace folders]
  C --> E[Copy playbooks to org/]
  C --> F[Install Skills]
  C --> G[Create Core Bots]
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

**Paste-link:** `https://github.com/firmasite/bot-org-os`

**Order for Core Bots:** Chief → Analyst → Product Manager → Architect → Developer.

Extended Bots are **not** created on first install.

Optional tools are **not** part of Core success. See [OPTIONAL-TOOLS.md](../OPTIONAL-TOOLS.md).

HTML (Archify): [install-flow.html](install-flow.html) when present.

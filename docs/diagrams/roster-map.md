# Roster map — Core Team + Extended idle

Who is always on, and who waits for a bottleneck.

```mermaid
flowchart TB
  subgraph human["Human"]
    OP[Operator]
  end

  subgraph core["Core Team — always on"]
    CH[Chief<br/>route · collect · escalate]
    AN[Analyst<br/>Analysis]
    PM[Product Manager<br/>Planning]
    AR[Architect<br/>Solutioning]
    DV[Developer<br/>Implementation]
  end

  subgraph ext["Extended — idle until bottleneck"]
    UX[UX Designer]
    QA[QA]
    TW[Tech Writer]
    VF[Verifier]
  end

  OP -->|goals · approvals| CH
  CH --> AN
  CH --> PM
  CH --> AR
  CH --> DV
  CH -.->|wake only via BOTTLENECKS| UX
  CH -.-> QA
  CH -.-> TW
  CH -.-> VF
```

**Read this as:** Chief talks to you and routes work to one Core owner. Extended Bots stay documented but idle until pain is logged twice (or you assign explicitly).

HTML (Archify): [roster-map.html](roster-map.html) when present.

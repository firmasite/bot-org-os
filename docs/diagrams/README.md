# Diagrams

**Source of truth for rendering:** Archify workflow JSON (`*.workflow.json`).

Generate HTML:

```bash
sh /workspace/org/diagrams/run-diagram-tool.sh render workflow roster-map.workflow.json roster-map.html --quality standard
sh /workspace/org/diagrams/run-diagram-tool.sh render workflow install-flow.workflow.json install-flow.html --quality standard
sh /workspace/org/diagrams/run-diagram-tool.sh render workflow artifact-bus.workflow.json artifact-bus.html --quality standard
```

(Vendor CLI: `node /workspace/vendor/archify/archify/bin/archify.mjs` — same args.)

Mermaid in the repo README matches these workflows so GitHub can render inline. HTML files are the Archify previews.

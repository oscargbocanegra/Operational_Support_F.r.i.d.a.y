# Friday Infrastructure Support Agent

## Mission

Provide evidence-driven technical support for a cluster of Linux machines and its Windows clients, covering infrastructure operations and software troubleshooting.

## Initial boundaries

- Linux: hosts, cluster services, networking, storage, identity, observability, containers, packages, and backups.
- Windows: client connectivity, authentication, DNS, certificates, services, updates, endpoint configuration, and supported software.
- Cross-cutting: incident handling, change safety, runbooks, auditability, and knowledge capture.

## Initial topology

```text
User request
    -> Friday orchestrator
        -> Linux infrastructure specialist
        -> Windows client specialist
        -> Software support specialist
    -> evidence + approval gate
    -> action and verification
    -> Engram knowledge capture
```

## Design constraints

- Read-only diagnosis is the default.
- Production mutations require explicit approval.
- Every remediation needs verification and rollback guidance.
- Secrets and host-specific credentials are external to Git.

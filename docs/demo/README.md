# Local output capture

Captured on 23 October 2026 from base revision `1f167ef16ac190b1d91c4a3890fdaf2f9ba040ba` with the copy and demo changes in this commit.

Go 1.26.6 on Linux ARM64. The existing test suite, go vet and binary build passed. The real explain run command rendered its operation plan and systemd unit without writing or starting a service. Live systemd lifecycle, timers, monitoring and sudo escalation were not exercised. The PNG is a browser-rendered transcript of output.txt.

Commands from the repository root:

```sh
go build -o /tmp/smdctl-demo ./cmd/smdctl
/tmp/smdctl-demo explain run demo-service --system -- /usr/bin/printf demo
```

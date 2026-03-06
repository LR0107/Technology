## OpenClaw on Windows (WSL2)

### Environment Setup

Requirement: **Node.js 22 or higher**

```bash
node --version
curl -fsSL https://openclaw.ai/install.sh | bash
```

### Verify Installation

```bash
openclaw --version
```

### Check Gateway Status

```bash
openclaw gateway status
```

### Open the UI (Dashboard)

```bash
openclaw dashboard
```

Open in browser:

```
http://127.0.0.1:18789
```

### Access via CLI

```bash
openclaw tui
```

### Gateway Control

Start:

```bash
openclaw gateway --port 18789
```

Stop:

```bash
openclaw gateway stop
```

Restart:

```bash
openclaw gateway restart
```

### Start Configuration

```bash
openclaw config
```

---

## Install Skills

Install repository:

```bash
npm i -g clawhub
```

Install skill:

```bash
clawhub install summary
```

After installation, **restart OpenClaw**.

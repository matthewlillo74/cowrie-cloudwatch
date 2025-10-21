# Cowrie Honeypot — CloudWatch demo

This repository contains configuration and screenshots for a containerized Cowrie SSH honeypot integrated with Amazon CloudWatch.

## Contents
- \`etc/cowrie.cfg\` — Cowrie configuration.
- \`cw-agent-config.json\` — CloudWatch Agent config (no credentials).
- \`docker-compose.yml\` — optional compose file.
- \`screenshots/\` — screenshots of logs and CloudWatch.

## How I tested
1. Launched container: \`docker compose up -d\` or \`docker run ...\`.
2. Verified cowrie JSON log output in \`logs/cowrie.json\`.
3. Installed Amazon CloudWatch Agent and used \`cw-agent-config.json\` to push log file(s) to CloudWatch.
4. Confirmed log group \`cowrie-honeypot\` contains JSON events.

**Security note:** Do NOT commit AWS credentials, private keys, or runtime logs containing sensitive data. Use the provided \`.gitignore\`.


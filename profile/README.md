<p align="center">
  <a href="https://wakehook.com">
    <img src="https://wakehook.com/brand/og-image.png" alt="WakeHook: your monitoring, louder" width="720">
  </a>
</p>

<h3 align="center">Your monitoring already knows when something breaks.<br>WakeHook makes sure somebody wakes up.</h3>

<p align="center">
  <a href="https://wakehook.com">Website</a> ·
  <a href="https://wakehook.com/docs/quickstart.html">Quickstart</a> ·
  <a href="https://wakehook.com/integrations/">Integrations</a> ·
  <a href="https://apps.apple.com/app/id6811071570">App Store</a> ·
  <a href="https://play.google.com/store/apps/details?id=com.raspiska.wakehook">Google Play</a> ·
  <a href="https://status.wakehook.com">Status</a>
</p>

---

**WakeHook** turns any alert into a phone alarm. Point your monitoring at a WakeHook address. When something fires, it rings the on-call phone through Do Not Disturb and Focus until a human acknowledges. If nobody does, it moves on to the next person.

```
your monitoring  ──►  WakeHook  ──►  the on-call phone rings
 (any webhook,                        until someone acknowledges,
  email, cron)                        then it escalates
```

### What it does

- **Rings, doesn't whisper.** A full alarm on Android, Time Sensitive alerts through Do Not Disturb and Focus on iPhone, repeated until someone answers.
- **Escalates.** On-call first, then the next person, then the whole team. Hand off a ringing incident in one tap, and optionally add a phone call.
- **Wake-proof acknowledgement**, so a half-asleep tap can't silence a real incident.
- **Fire drills and device readiness**, so you find out a pager is broken on a Tuesday afternoon, not at 3am.
- **Heartbeats** for cron jobs and backups: silence becomes an alert.
- **Works with what you run:** Alertmanager, Grafana, Datadog, Sentry, Uptime Kuma, UptimeRobot, Zabbix, New Relic, CloudWatch, Azure Monitor, GitHub Actions, email, PagerDuty and Opsgenie-compatible APIs, or any webhook.

### Repositories

| Repository | What's inside |
|---|---|
| [examples](https://github.com/Wakehook/examples) | Copy-paste examples for sending alerts: curl, Python, Node.js, Go, PowerShell, heartbeats, GitHub Actions, Alertmanager and signed requests |
| [wake-button](https://github.com/Wakehook/wake-button) | A weekend hardware project: a big physical button on USB that pages your team when you press it |

### Get started

1. Create a free account at **[app.wakehook.com](https://app.wakehook.com/register)**. The Free plan covers one person and one source, forever.
2. Add a source and copy its hook address.
3. Install the app, pair your phone, and send a test alert:

```bash
curl -X POST "$WAKEHOOK_URL" -H 'Content-Type: application/json' \
  -d '{"title": "Hello from WakeHook", "severity": "critical"}'
```

Treat a hook address like a password: anyone who has it can page your team.

---

<p align="center">
  <sub>WakeHook is a product of <a href="https://raspiska.co"><b>Raspiska</b></a>, a team that has run production infrastructure for iGaming, fintech and Web3 for over ten years.<br>
  Questions? <a href="https://wakehook.com">wakehook.com</a> · Security reports: <a href="mailto:security@wakehook.com">security@wakehook.com</a></sub>
</p>

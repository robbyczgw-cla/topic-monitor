# Changelog

## [1.3.2] - 2026-02-11

### 🆕 Real Alerting System

The alerting system is now fully functional (was a stub before):

- **Telegram Alerts:** Send immediate alerts for high-priority findings
- **Multi-Channel Support:** Telegram, Discord, and Email
- **Smart Filtering:** Importance scoring determines what gets alerted

### Changed

- **State Files:** Now stored in `.data/` directory (configurable via `TOPIC_MONITOR_DATA_DIR`)
- **Telegram ID:** Configured via `TOPIC_MONITOR_TELEGRAM_ID` environment variable (no hardcoded values)
- **web-search-plus Path:** Now relative by default, configurable via `WEB_SEARCH_PLUS_PATH`
- **No Hardcoded Paths:** All paths and IDs are now configurable

### Environment Variables

New environment variables for configuration:

| Variable | Default | Description |
|----------|---------|-------------|
| `TOPIC_MONITOR_TELEGRAM_ID` | — | Telegram chat ID for alerts |
| `TOPIC_MONITOR_DATA_DIR` | `.data/` | State and findings directory |
| `WEB_SEARCH_PLUS_PATH` | Relative | Path to web-search-plus script |

### Migration

If you had hardcoded paths in config.json, update to use environment variables:
```bash
export TOPIC_MONITOR_TELEGRAM_ID="your_telegram_id"
```

## [1.2.1] - 2026-02-04

- Privacy cleanup: removed hardcoded paths and personal info from docs

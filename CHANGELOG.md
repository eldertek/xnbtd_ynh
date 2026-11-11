# Changelog

All notable changes to the `xnbtd_ynh` YunoHost package are documented in this file.

## [2.0.1] - 2025-04-25

### Changed
- Added `django-redis` and `async-timeout` dependencies for Redis cache compatibility (`0746e7c`, `cd606b3`).
- Migrated Poetry development dependency definitions to group syntax (`2f641ae`).
- Synchronized YunoHost packaging scripts with upstream xNBTD updates (`af22eee`).

## [2.0.0] - 2025-01-04

### Changed
- Updated `manifest.json`, `requirements.txt`, `pyproject.toml`, and bilingual documentation (`5d023d8`, `a8008b9`).

## [1.0.9] - 2023-10-26

### Added
- Initial YunoHost packaging, systemd service configuration, and automated install/upgrade scripts (`0618bbe`).

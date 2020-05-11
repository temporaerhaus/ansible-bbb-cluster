# Ansible Role: bigbluebutton exporter

[![Build Status](https://travis-ci.org/stadtulm/ansible-bigbluebutton-exporter.svg?branch=master)](https://travis-ci.org/stadtulm/ansible-bigbluebutton-exporter)
[![License](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg)](https://opensource.org/licenses/MIT)
[![Ansible Role](https://img.shields.io/badge/ansible%20role-stadtulm.bigbluebutton-exporter-blue.svg)](https://galaxy.ansible.com/stadtulm/bigbluebutton-exporter/)
[![GitHub tag](https://img.shields.io/github/tag/stadtulm/ansible-bigbluebutton-exporter.svg)](https://github.com/stadtulm/ansible-bigbluebutton-exporter/tags)

## Description

Deploy [greenstatic](https://github.com/greenstatic)s [bigbluebutton exporter](https://github.com/greenstatic/bigbluebutton-exporter) using ansible.

## Requirements

- Ansible >= 2.7 (It might work on previous versions, but we cannot guarantee it)

## Role Variables

All variables which can be overridden are stored in [defaults/main.yml](defaults/main.yml) file as well as in table below.

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `bbb_exporter_version` | v0.2.0 | BBB exporter package version. Also accepts git commit hashes. |
| `bbb_exporter_listen_address` | "0.0.0.0" | Address on which bbb exporter will listen |
| `bbb_exporter_listen_port` | "9688" | Port on which bbb exporter will listen |
| `bbb_exporter_api_base_url` | | URL of your BBB api endpoint (without `api/` at the end) |
| `bbb_exporter_api_secret` | | Run `bbb-conf --secret` on your bbb host to get secret |

## Example

### Playbook

Use it in a playbook as follows:
```yaml
- hosts: all
  roles:
    - stadtulm.bigbluebutton-exporter
```

## License

This project is licensed under MIT License. See [LICENSE](/LICENSE) for more details.
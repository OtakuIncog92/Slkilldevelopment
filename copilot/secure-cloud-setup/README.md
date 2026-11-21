# Secure Cloud Setup (Personal, Free)

This guide describes a free, personal cloud setup focused on private access and strong security.

## Goal
- Keep storage under your control
- Allow access only from your own trusted devices
- Avoid recurring platform fees

## Recommended Free Stack
- **Storage app**: Nextcloud (self-hosted)
- **Access tunnel**: WireGuard or Tailscale (free tier)
- **Host**: Existing home PC, mini PC, or repurposed laptop
- **OS**: Ubuntu Server LTS
- **Backups**: Restic + local/external encrypted destination

## Security Baseline
1. Keep cloud service ports off the public internet. If using WireGuard, allow only its UDP listener port; use Tailscale or a relay for zero inbound ports.
2. Require VPN access before cloud login.
3. Use unique long passwords and enable MFA.
4. Disable guest/public sharing by default.
5. Encrypt the host disk and backup archives.
6. Enable automatic security updates.
7. Keep firewall enabled with deny-by-default rules.
8. Remove unused users and apps.

## Setup Checklist
- [ ] Install host OS and apply all updates
- [ ] Install and configure VPN (WireGuard/Tailscale)
- [ ] Verify cloud endpoint is reachable only over VPN
- [ ] Install and configure Nextcloud
- [ ] Create one admin account and one personal user account
- [ ] Enforce MFA and strong password policy
- [ ] Disable public links/guest access
- [ ] Configure encrypted backups and test restore
- [ ] Enable logs and failed-login protections

## Ongoing Maintenance
- Weekly: install updates and review login activity
- Monthly: verify backups and test restore flow
- Quarterly: rotate credentials and re-check exposed ports

## Validation
To confirm your cloud is "only mine":
- External port scan shows no public cloud service ports
- Cloud login is inaccessible without VPN
- Only your devices are listed as trusted clients

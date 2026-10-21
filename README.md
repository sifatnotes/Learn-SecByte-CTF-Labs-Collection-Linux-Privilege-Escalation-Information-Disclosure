# Learn-SecByte-CTF-Labs-Collection-Linux-Privilege-Escalation-Information-Disclosure
A curated collection of hands-on cybersecurity CTF labs covering Docker Group Abuse, LD_PRELOAD Library Hijacking, Cron Job Exploitation, NFS Root Squashing, and Exposed Environment/Git Files from Learn SecByte.
# Learn SecByte CTF & Cybersecurity Labs Collection

Welcome to the **Learn SecByte CTF & Cybersecurity Labs Collection**. This repository is a dedicated, searchable index of hands-on Information Disclosure & Sensitive Data Exposure (Exposed `.env` Files, Exposed Backup Files, Exposed `.git` Repositories, Verbose Error Messages, Debug Mode Enabled, Hidden Directory Listing) and Local Linux Privilege Escalation & OS Misconfigurations (Docker Group Abuse, `LD_PRELOAD` Library Hijacking, Cron Job Misconfigurations, NFS Root Squashing Bypass, Writable `$PATH` Hijacking, Weak File Permissions) labs designed for cybersecurity students, CTF players, system administrators, penetration testers, red team operators, and security auditors.

---

## Table of Contents
- [Introduction](#introduction)
- [Lab Collection & Index](#lab-collection--index)
- [Categories](#categories)
- [Learning Path](#learning-path)
- [How to Use the Labs](#how-to-use-the-labs)
- [Disclaimer](#disclaimer)

---

## Introduction

Achieving complete system compromise often begins with small web application information leaks that reveal credentials or source code, followed by leveraging local Linux system misconfigurations to escalate privileges to root. Hosted on [Learn SecByte](https://learn.secbyte.org/), this comprehensive information disclosure, web reconnaissance, and Linux local privilege escalation collection provides practical, hands-on technical training to discover exposed secrets and exploit core operating system vectors.

From extracting database passwords from exposed `.env` files, downloading web root backups, and dumping source code from publicly accessible `.git` directories to gaining instant host root access via the `docker` group, hijacking shared libraries via `LD_PRELOAD`, exploiting unquoted or insecure cron jobs, mounting root-squashed NFS shares (`no_root_squash`), hijacking binary search paths, and overriding world-writable system files, these exercises prepare security professionals to master internal post-exploitation and defense.

---

## Lab Collection & Index

Below is the complete, searchable index of all sensitive data exposure, web reconnaissance, and local Linux privilege escalation challenges in this collection:

| # | Lab / Challenge Name | Category | Focus / Key Topics | Lab Link |
|---|----------------------|----------|---------------------|----------|
| 1 | **Exposed Environment Files** | Information Disclosure & Web Exposure | Unprotected `.env` files, cleartext database/API credentials, cloud access key leaks, configuration exposure | [Access Lab](https://learn.secbyte.org/ctf/exposed-environment-files) |
| 2 | **Exposed Backup Files** | Information Disclosure & Web Exposure | Source code backup discovery (`.bak`, `.swp`, `.zip`), hardcoded secret extraction, database dump analysis | [Access Lab](https://learn.secbyte.org/ctf/exposed-backup-files) |
| 3 | **Exposed Git Repository** | Information Disclosure & Web Exposure | Accessing `.git` directories, reconstructing repository objects with `git-dumper`, source code leak analysis | [Access Lab](https://learn.secbyte.org/ctf/exposed-git-repository) |
| 4 | **Verbose Error Messages** | Information Disclosure & Web Exposure | Stack trace leakage, path disclosure, database technology fingerprinting, internal class/variable exposure | [Access Lab](https://learn.secbyte.org/ctf/verbose-error-messages) |
| 5 | **Debug Mode Enabled** | Information Disclosure & Web Exposure | Application framework debug consoles (Flask Debugger, Werkzeug, Django Debug Toolbar), interactive Python code execution | [Access Lab](https://learn.secbyte.org/ctf/debug-mode-enabled) |
| 6 | **Directory Listing: Hidden Surface** | Information Disclosure & Web Exposure | Server index directory browsing (`Options +Indexes`), orphan file discovery, sensitive log/document extraction | [Access Lab](https://learn.secbyte.org/ctf/directory-listing-hidden-surface) |
| 7 | **Weak File Permissions: From Misconfiguration to Privilege Escalation** | Local Linux Privilege Escalation & OS Misconfigurations | World-writable `/etc/passwd` or `/etc/shadow`, SUID binary abuse, sensitive configuration file modification | [Access Lab](https://learn.secbyte.org/ctf/weak-file-permissions-from-misconfiguration-to-privilege-esc) |
| 8 | **NFS Misconfiguration: From Enumeration to Root Access** | Local Linux Privilege Escalation & OS Misconfigurations | Network File System (NFS) share enumeration, `no_root_squash` export option abuse, remote SUID binary creation to root shell | [Access Lab](https://learn.secbyte.org/ctf/nfs-misconfiguration-from-enumeration-to-root-access) |
| 9 | **Docker Group Abuse: From Local Access to Root** | Local Linux Privilege Escalation & OS Misconfigurations | Unprivileged user membership in the `docker` Unix group, mounting host root directory (`/`) into container, host root execution | [Access Lab](https://learn.secbyte.org/ctf/docker-group-abuse-from-local-access-to-root) |
| 10 | **LD_PRELOAD Abuse: Library Hijacking Privilege Escalation** | Local Linux Privilege Escalation & OS Misconfigurations | Sudoer `env_keep += LD_PRELOAD` directive abuse, shared C library injection (`so`), arbitrary C function override to root | [Access Lab](https://learn.secbyte.org/ctf/ld-preload-abuse-library-hijacking-privilege-escalation) |
| 11 | **Writable PATH** | Local Linux Privilege Escalation & OS Misconfigurations | Insecure environment `$PATH` order, relative path execution in binary scripts, malicious replacement binary injection | [Access Lab](https://learn.secbyte.org/ctf/writable-path) |
| 12 | **Cron Job Exploitation: From Misconfiguration to Root** | Local Linux Privilege Escalation & OS Misconfigurations | Unquoted cron task parameters, world-writable cron script execution, wildcard expansion abuse (`*`), root privilege escalation | [Access Lab](https://learn.secbyte.org/ctf/cron-job-exploitation-from-misconfiguration-to-root) |

---

## Categories

### 1. Information Disclosure & Sensitive Data Exposure
Harvest sensitive cleartext credentials, API keys, source code, and application architecture details from publicly exposed environment files (`.env`), backup archives, web-accessible `.git` folders, verbose application stack traces, framework debug consoles, and directory listings.
- [Exposed Environment Files](https://learn.secbyte.org/ctf/exposed-environment-files)
- [Exposed Backup Files](https://learn.secbyte.org/ctf/exposed-backup-files)
- [Exposed Git Repository](https://learn.secbyte.org/ctf/exposed-git-repository)
- [Verbose Error Messages](https://learn.secbyte.org/ctf/verbose-error-messages)
- [Debug Mode Enabled](https://learn.secbyte.org/ctf/debug-mode-enabled)
- [Directory Listing: Hidden Surface](https://learn.secbyte.org/ctf/directory-listing-hidden-surface)

### 2. Local Linux Privilege Escalation & OS Misconfigurations
Escalate privileges from an unprivileged local user account to `root` on Linux target systems by exploiting Docker group memberships, hijacking C library calls via `LD_PRELOAD`, abusing NFS `no_root_squash` mounts, exploiting misconfigured cron tasks, tampering with binary search paths (`$PATH`), and modifying weak system file permissions.
- [Weak File Permissions: From Misconfiguration to Privilege Escalation](https://learn.secbyte.org/ctf/weak-file-permissions-from-misconfiguration-to-privilege-esc)
- [NFS Misconfiguration: From Enumeration to Root Access](https://learn.secbyte.org/ctf/nfs-misconfiguration-from-enumeration-to-root-access)
- [Docker Group Abuse: From Local Access to Root](https://learn.secbyte.org/ctf/docker-group-abuse-from-local-access-to-root)
- [LD_PRELOAD Abuse: Library Hijacking Privilege Escalation](https://learn.secbyte.org/ctf/ld-preload-abuse-library-hijacking-privilege-escalation)
- [Writable PATH](https://learn.secbyte.org/ctf/writable-path)
- [Cron Job Exploitation: From Misconfiguration to Root](https://learn.secbyte.org/ctf/cron-job-exploitation-from-misconfiguration-to-root)

---

## Learning Path

Follow this structured progression path to master web information gathering, credential extraction, and local Linux root escalation techniques:

1. **Phase 1: Web Information Reconnaissance & Data Leakage** — Inspect public web directories to extract sensitive credentials, source code, and debug execution access:
   - [Directory Listing: Hidden Surface](https://learn.secbyte.org/ctf/directory-listing-hidden-surface)
   - [Verbose Error Messages](https://learn.secbyte.org/ctf/verbose-error-messages)
   - [Exposed Environment Files](https://learn.secbyte.org/ctf/exposed-environment-files)
   - [Exposed Backup Files](https://learn.secbyte.org/ctf/exposed-backup-files)
   - [Exposed Git Repository](https://learn.secbyte.org/ctf/exposed-git-repository)
   - [Debug Mode Enabled](https://learn.secbyte.org/ctf/debug-mode-enabled)

2. **Phase 2: Local Linux Enumeration & File System Misconfigurations** — Identify world-writable configuration files, weak permissions, and writable binary search paths:
   - [Weak File Permissions: From Misconfiguration to Privilege Escalation](https://learn.secbyte.org/ctf/weak-file-permissions-from-misconfiguration-to-privilege-esc)
   - [Writable PATH](https://learn.secbyte.org/ctf/writable-path)

3. **Phase 3: Scheduled Tasks & Shared Library Injections** — Hijack local shared C libraries using `LD_PRELOAD` and exploit misconfigured, high-privilege cron jobs:
   - [Cron Job Exploitation: From Misconfiguration to Root](https://learn.secbyte.org/ctf/cron-job-exploitation-from-misconfiguration-to-root)
   - [LD_PRELOAD Abuse: Library Hijacking Privilege Escalation](https://learn.secbyte.org/ctf/ld-preload-abuse-library-hijacking-privilege-escalation)

4. **Phase 4: High-Privilege Group Memberships & Remote NFS Mounts** — Mount host root volumes via Docker socket access and create remote root SUID binaries via NFS shares:
   - [NFS Misconfiguration: From Enumeration to Root Access](https://learn.secbyte.org/ctf/nfs-misconfiguration-from-enumeration-to-root-access)
   - [Docker Group Abuse: From Local Access to Root](https://learn.secbyte.org/ctf/docker-group-abuse-from-local-access-to-root)

---

## How to Use the Labs

1. Select a challenge link from the index or category sections above.
2. Read the scenario directives, operating system environment specs, and target parameters on [Learn SecByte](https://learn.secbyte.org/).
3. Deploy analysis toolsets (`git-dumper`, `showmount`, `docker`, GCC compiler, LinPEAS, `crontab`, `find`, Curl) inside an isolated workstation or virtual machine.
4. Dump exposed `.git` object stores, compile custom C shared objects (`.so`) for `LD_PRELOAD` injection, mount host directories using Docker, spawn NFS SUID root shells, and capture target flags.

---

## Disclaimer

This repository and its linked challenge resources are strictly intended for educational, threat research, and authorized technical security training purposes. Never execute local privilege escalation scripts, Docker socket hijacking, or unauthorized git repository dumps against production servers, non-owned Linux target hosts, or live corporate infrastructure.

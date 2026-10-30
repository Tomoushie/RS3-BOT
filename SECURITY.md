# Security Policy

## Supported versions

| Version | Supported |
|---|---|
| Latest release (v1.2.x / RS3Bot V16) | ✅ |
| Older releases | ❌ (please update) |

## Reporting a vulnerability

**Please do not open a public GitHub issue for security problems.**

Email: **nowaktombe@protonmail.com** with the subject **`[SECURITY] RS3Bot`**.

Include:
- RS3Bot version and Windows version;
- steps to reproduce;
- impact (what an attacker could do);
- any proof of concept or logs.

You will receive an acknowledgement within **72 hours**. Please allow up to **30 days** for a fix before public disclosure.

## Scope

In scope:
- Premium licensing bypass that gives access to premium data without a valid license;
- Code execution, unsafe deserialization, path traversal, local privilege escalation;
- Leakage of private data (journal, bank, license, device ID) to a remote server;
- Supply-chain issues in releases (unsigned/tampered binaries).

Out of scope:
- Social engineering of the maintainer or users;
- Denial of service against public data APIs;
- Issues requiring an already-compromised operating system;
- « Pirating » the paid features by patching the local binary: the offline license deliberately raises the bar but cannot be cryptographically inviolable on a user-controlled machine. Reports about concrete bypasses are still welcome to improve hardening.

## Security design notes

- Premium backend commands are **fail-closed** and gated by a compile-time plan (`public`/`internal`) plus an offline **Ed25519** license.
- The **private signing key is never embedded** in the application; only the public key is shipped.
- No telemetry, no remote account, no game credentials.
- All personal data stays in `%APPDATA%\RS3Bot\` and browser local storage.

## Disclosure

We credit reporters (unless anonymity is requested) in the release notes once a fix is available.

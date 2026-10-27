# Hellrook Manager releases

Hellrook Manager is a Windows program that runs an RF Online server install. It starts and watches the game server
and the web server, shows their logs, and handles backups, restarts, accounts, settings and alerts.

This repository holds only its releases. The source is private.

## Install

1. Download `hellrook_manager.exe` from the [latest release](../../releases/latest).
2. Put it in the top folder of the server install, beside the `settings` and `server` folders.
3. Start it.

It needs Windows 10 or 11, 64-bit.

## Updates

From v0.5.0 on, Hellrook Manager updates itself from these releases. Each release has two files:

- `hellrook_manager.exe`, the program;
- `hellrook_manager.update`, its manifest. It holds the version, the exe's size and SHA-256, and an Ed25519
  signature made with Hellrook Studio's release key.

The manager installs a release only if the signature checks against the key built into it, and the download matches
the manifest's size and SHA-256.

# Connex Update Feed

This folder is the public-facing update feed for Windows desktop updates.

## Expected files

After running:

- `C:\connex\preparar feed de updates.bat`

this folder should contain files such as:

- `latest.yml`
- `Connex-Setup-0.1.2.exe`
- `Connex-Setup-0.1.2.exe.blockmap`

## Goal

Publish this folder through a simple public static host, for example:

- `https://updates.seudominio.com/windows`

Then point `Connex` to:

```json
{
  "deviceName": "Connex Remote Workstation",
  "signalingUrl": "wss://connex-signaling.onrender.com",
  "updateUrl": "https://updates.seudominio.com/windows"
}
```

## Important

This folder should expose only update artifacts, not source code.

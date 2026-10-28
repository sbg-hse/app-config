# app-config

Server address for the HSE-MS apps. The apps read this file on start:

https://raw.githubusercontent.com/sbg-hse/app-config/main/app-config.json

- `hse_ms_app`: the HSE-MS SDA app (observations, etc.)
- `hse_exam_app`: the exam app

To move the apps to a new server, edit `app-config.json` and commit. Apps pick it up on their next launch (GitHub may cache the file for up to ~5 minutes).
Keep the JSON valid: an invalid file is ignored and the apps fall back to the last address that worked.

This repo must stay **public** so the apps can read it without a login. Don't put secrets here.

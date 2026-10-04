# Native mobile add-in (`mobile-app`)

An Effortless **add-in seed** (kind `child`), mounted at `mobile/`. Requires
the `rulebook-backend` add-in: the app talks to its generated Node API. It has
no rulebook of its own: `rulebook-to-react-native` reads the project's
`../effortless-rulebook/effortless-rulebook.json`.

## What the build produces

`mobile/` inside this folder (so `<project>/mobile/mobile/`): an Expo
(React Native, TypeScript, expo-router) app with a list, detail, create and
edit screen per table, derived values read-only and badged, relationships as
tappable links, typed API clients per table.

## Questions

| Key | Default | Used for |
|---|---|---|
| `appName` | `My Rulebook` | `app.json` name and the home screen title |
| `bundleId` | `com.effortlessapi.myrulebook` | iOS bundle id and Android package |
| `apiBaseUrl` | `http://localhost:42441` | Where the app reaches the backend API |

## How it is used

```bash
effortless cloneSeed effortlessapi/erb-seed-mobile-app mobile
rm -rf mobile/.git
cd mobile && effortless build
cd mobile && npm install && npx expo start
```

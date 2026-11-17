# Noctis iOS

Application iOS de Noctis (Capacitor). Version **1.3.1**.

L'application affiche `https://noctis.ct.ws`. Le projet Xcode se trouve dans `App/`.

## Build

```bash
cd App
xcodebuild -project App.xcodeproj -scheme App -configuration Release \
  -destination 'generic/platform=iOS' -archivePath build/App.xcarchive \
  CODE_SIGNING_ALLOWED=NO CODE_SIGNING_REQUIRED=NO archive
```

Le workflow GitHub Actions `.github/workflows/release.yml` construit l'IPA non signé et le publie dans la release `v1.3.1`. Un poussage de tag `build-1.3.1` déclenche le build.

> L'IPA est non signé : installation possible uniquement avec outil de sideloading (AltStore, Sideloadly, etc.).

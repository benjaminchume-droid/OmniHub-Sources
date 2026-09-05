# OmniHub-Sources

Source factory for [OmniHub](https://github.com/benjaminchume-droid/OmniHub).

OmniHub Core stays stable. **Sources** ship independently via this repository.

## Layout

```
OmniHub-Sources/
├── catalog/
│   ├── index.json          # Store catalog index
│   └── categories.json
├── cores/
│   ├── webcore/            # Universal WebCore seed
│   ├── apicore/            # Universal APICore seed
│   └── mcpcore/            # Universal MCPCore seed
├── sources/
│   └── ai/                 # Provider manifests (ChatGPT, Claude, …)
├── templates/
├── manifests/
└── .github/workflows/      # Batch build → sign → publish → catalog update
```

## Pipeline

```
manifest → select seed → inject config → validate → build APK → sign → checksum → release → catalog
```

Resumable batch builds: failed source N does not rebuild 1..N-1.

## Status

Scaffold for OmniHub v1.0.2 ecosystem phase. Populate manifests and CI next.

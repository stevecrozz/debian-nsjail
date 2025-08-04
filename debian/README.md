# nsjail-debian

Debian packaging files for [`nsjail`](https://github.com/google/nsjail)

## 🛠 How to Build the Package

These instructions assume a Debian-based system with packaging tools installed.

### 1. Clone This Repo

```bash
git clone https://github.com/stevecrozz/debian-nsjail.git
```

### 2. Add a new version for the upstream release

```bash
dch -i
```

### 3. Import the upstream changes via uscan

```bash
gbp import-orig --pristine --uscan --debian-branch=main --upstream-tag='upstream/%(version)s' --upstream-branch=upstream
```

### 3. Build

```bash
gbp buildpackage --git-builder=debuild --git-debian-branch=main
```

# nsjail-debian

Debian packaging files for [`nsjail`](https://github.com/google/nsjail), a lightweight sandboxing tool based on Linux namespaces, cgroups, rlimits, and seccomp-BPF.

This repository contains only the `debian/` directory required to build `.deb` packages of `nsjail` from upstream source. It is intended for use by maintainers, packagers, and advanced users who want to create and install `nsjail` via the Debian packaging system.

---

## 📦 What is nsjail?

`nsjail` is a powerful Linux process-isolation tool designed for:

- Sandboxing untrusted applications
- Secure code execution environments (e.g., in CTFs or CI/CD)
- Restricting system calls using seccomp-BPF
- Leveraging Linux namespaces and resource limits

Upstream: [https://github.com/google/nsjail](https://github.com/google/nsjail)

---

## 🛠 How to Build the Debian Package

These steps assume you're on a Debian-based system and have packaging tools installed.

### 1. Clone This Repo

```bash
git clone https://github.com/stevecrozz/debian-nsjail.git
```

### 2. Clone Upstream Source

```bash
git clone https://github.com/google/nsjail.git
cd nsjail
git checkout <version-tag>  # e.g., v1.0.0
```

### 3. Copy ./debian Folder to Upstream Source Folder

```bash
cp ../debian-nsjail/debian .
```

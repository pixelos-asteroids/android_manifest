
# ⚡ VoltageOS

[![Repo Size](https://img.shields.io/github/repo-size/VoltageOS/manifest?style=for-the-badge)](https://github.com/VoltageOS/manifest)
[![License](https://img.shields.io/github/license/VoltageOS/manifest?style=for-the-badge)](https://github.com/VoltageOS/manifest/blob/master/LICENSE)

VoltageOS is a custom Android ROM for **OnePlus 9 series** devices.  
This guide will help you **set up, sync, and build VoltageOS** like a pro developer.  

---

## 📝 Table of Contents
- [Prerequisites](#-prerequisites)  
- [Setup Repository](#-setup-repository)  
- [Sync Local Manifests](#-sync-local-manifests)  
- [Build Instructions](#-build-instructions)  
- [Tips & Notes](#-tips--notes)  

---

## 🛠️ Prerequisites
Make sure your system has the following installed:

- Linux/macOS with required build tools  
- `repo` tool  
- `git-lfs`  
- Adequate storage (~100GB free recommended)  

---

## 📂 Setup Repository
Clone and initialize the VoltageOS repository:

```bash
mkdir VoltageOS && cd VoltageOS
repo init -u https://github.com/VoltageOS/manifest.git -b 16 --git-lfs
```

---

## 🔄 Sync Local Manifests
Add device-specific manifest for OnePlus 9 series:

```bash
mkdir -p .repo/local_manifests
wget https://raw.githubusercontent.com/voltageos-oneplus9/manifest/16/OnePlus9Series.xml      -O .repo/local_manifests/OnePlus9Series.xml
```

Sync the repository:

```bash
repo sync
```

---

## 🏗️ Build Instructions

### OnePlus 9 Pro (`lemonadep`)
```bash
. build/envsetup.sh
brunch lemonadep
```

### OnePlus 9 (`lemonade`)
```bash
. build/envsetup.sh
brunch lemonade
```

---

## 💡 Tips & Notes
- Run `source build/envsetup.sh` before building.  
- Use `brunch <device>` to build a full system image.  
- Ensure all dependencies are installed to avoid build errors.  
- Check `out/target/product/<device>/` for compiled images.  

---

Maintained with ❤️ by the **Absolute N00b**

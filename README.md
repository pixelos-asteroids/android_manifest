
# ⚡ PixelOS For Asteroids

[![Repo Size](https://img.shields.io/github/repo-size/pixelos-asteroids/android_manifest?style=for-the-badge)](https://github.com/pixelos-asteroids/android_manifest)
[![License](https://img.shields.io/github/license/pixelos-asteroids/android_manifest?style=for-the-badge)](https://github.com/pixelos-asteroids/android_manifest/blob/master/LICENSE)

PixelOS is a custom Android ROM which bring pixel features on non pixel devices.  
This guide will help you **set up, sync, and build PixelOS** for **Nothing 3A / PRO**.  

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

- Linux with required build tools  
- `repo` tool  
- `git-lfs`  
- Adequate storage (~400GB free recommended)  

---

## 📂 Setup Repository
Clone and initialize the PixelOS repository:

```bash
mkdir PixelOS && cd PixelOS
repo init -u https://github.com/PixelOS-AOSP/android_manifest.git -b sixteen-qpr1 --git-lfs
```

---

## 🔄 Sync Local Manifests
Add device-specific manifest for Nothing 3A / Pro AKA asteroids:

```bash
mkdir -p .repo/local_manifests
wget https://raw.githubusercontent.com/pixelos-asteroids/android_manifest/sixteen-qpr1/asteroids.xml      -O .repo/local_manifests/asteroids.xml
```

Sync the repository:

```bash
repo sync
```

---

## 🏗️ Build Instructions

### Nothing 3A / PRO (asteroids`)
```bash
. build/envsetup.sh
breakfast asteroids
m pixelos
```

---

## 💡 Tips & Notes
- Run `source build/envsetup.sh` before building.  
- If you face ABI_Check issue run below command
```bash
export SKIP_ABI_CHECKS=true
```  

--- 

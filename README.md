# Prebuilt open62541pp vcpkg Artifacts

This repository provides **precompiled vcpkg artifacts** for the
[open62541pp](https://github.com/open62541pp/open62541pp) library.

The goal is to make it easy to download ready‑to‑use static builds for:

- **Windows (x64-windows-static)**
- **Linux (x64-linux)**  
  (static `.a` libraries produced by vcpkg)

These builds are generated automatically using GitHub Actions.

---

## 📦 What’s included

Each artifact contains the full vcpkg installation folder for the selected triplet:

```
debug/
include/
lib/
share/
```

This means you can drop the folder directly into your project or point your
build system to it.

---

## 🚀 How to download the artifacts

1. Go to the **Actions** tab of this repository  
2. Select the workflow run you want (Windows or Linux)  
3. Scroll down to **Artifacts**  
4. Download the archive for your platform

Artifacts are named like:

```
open62541pp-x64-windows-static
open62541pp-x64-linux
```


---

## 🔧 How the builds are generated

The repository contains two GitHub Actions workflows.

### Windows workflow
```
git clone https://github.com/microsoft/vcpkg.git
.\bootstrap-vcpkg.bat
.\vcpkg\vcpkg.exe install open62541pp:x64-windows-static
```


### Linux workflow
```
git clone https://github.com/microsoft/vcpkg.git
./bootstrap-vcpkg.sh
./vcpkg/vcpkg install open62541pp:x64-linux
```


Both workflows are **manual trigger only** (`workflow_dispatch`).

---

## 📚 About open62541pp

open62541pp is a modern C++ wrapper around the
[open62541](https://github.com/open62541/open62541) OPC UA stack.

Official project:
`https://github.com/open62541pp/open62541pp`

This repository only provides **prebuilt vcpkg artifacts** for convenience.

---

## 📝 License

This repository does not modify the upstream library.  
Please refer to the open62541pp project for licensing details.

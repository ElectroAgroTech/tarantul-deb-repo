# Custom Debian Package Repository

This repository contains a custom Debian package repository structure with `.deb` packages stored under `pool/main`.  
To make packages available via `apt`, you must generate the `Packages` indexes for each architecture.

---

## 📦 Generating Package Indexes

Run the following commands from the root of the repository.

### **ARMHF (32-bit)**

```bash
dpkg-scanpackages pool/main > dists/stable/main/binary-armhf/Packages
```

```bash
gzip -k dists/stable/main/binary-armhf/Packages
```

### ***ARM64 (64-bit)**

```bash
dpkg-scanpackages pool/main > dists/stable/main/binary-arm64/Packages
```

```bash
gzip -k dists/stable/main/binary-arm64/Packages
```

### ***Architecture-independent (all)**

```bash
dpkg-scanpackages pool/main > dists/stable/main/binary-all/Packages
```

```bash
gzip -k dists/stable/main/binary-all/Packages
```

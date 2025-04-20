# 📦 p7zip — 7-Zip CLI Archiver for Linux

**p7zip** is the Unix/Linux port of the popular Windows file archiver **7-Zip**. It supports a wide range of compression formats with high compression ratios, especially `.7z`.

---

## ✅ Features

- Create and extract `.7z` archives
- Supports many formats: 7z, zip, tar, gzip, bzip2, xz, iso, rar (read-only), etc.
- AES-256 encryption in 7z format
- Command-line interface with rich options
- High compression ratio

---

## 🔧 Installation

### Debian/Ubuntu
```bash
sudo apt install p7zip-full
```

### Arch Linux
```bash
sudo pacman -S p7zip
```

---

## 🚀 Basic Usage

### 📁 Compress a Directory into `.7z`
```bash
7z a archive.7z folder/
```

- `a` = add to archive
- `archive.7z` = output archive name
- `folder/` = folder to compress

### 📄 Compress a File
```bash
7z a file.7z file.txt
```

---

### 📦 Extract `.7z` Archive
```bash
7z x archive.7z
```

- `x` = extract with full paths

### 📦 Extract `.zip` or Other Formats
```bash
7z x archive.zip
```

---

### 📄 List Contents of Archive
```bash
7z l archive.7z
```

---

### 🔐 Create Password-Protected Archive
```bash
7z a -pSECRET archive.7z folder/
```

- `-pSECRET` sets the password
- Add `-mhe=on` to also encrypt file names:
```bash
7z a -pSECRET -mhe=on archive.7z folder/
```

---

## 📂 Supported Formats

| Format | Create | Extract |
|--------|--------|---------|
| 7z     | ✅     | ✅      |
| zip    | ✅     | ✅      |
| tar    | ✅     | ✅      |
| gzip   | ✅     | ✅      |
| bzip2  | ✅     | ✅      |
| xz     | ✅     | ✅      |
| rar    | ❌     | ✅      |
| iso    | ❌     | ✅      |

---

## 📚 Help and Manual

### Quick Help
```bash
7z --help
```

### Full Manual
```bash
man 7z
```

---

## 🧩 Tips

- For `.zip` archives, `zip` and `unzip` might be simpler tools.
- `p7zip-full` includes support for most formats.
- 7-Zip is known for its **superior compression ratio** compared to `zip` or `tar.gz`.

---

## 🔄 Related Tools

| Tool     | Description                      |
|----------|----------------------------------|
| `tar`    | Archiving tool (often combined with gzip) |
| `zip`/`unzip` | Classic zip compression tools |
| `xz`     | High compression for tarballs    |
| `zstd`   | Fast compression tool (Facebook) |

---

## 📦 Example: Create `.tar.7z` for Backup

```bash
tar -cf backup.tar my_folder/
7z a backup.tar.7z backup.tar
```

> First create a tarball, then compress it with 7z for max efficiency.

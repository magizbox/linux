## Filesystem Hierarchy Standard

<img src="https://lh3.googleusercontent.com/ztPaQX-oQu5K_CgAx3eaXJPp5ZQnBq7Mo19DOeqF0squuoHDv1q7=w711-h925-no" alt="" />

## Search

```bash
# Finding all files containing a text string on Linux
grep -rnw '/path/to/somewhere/' -e "pattern"
```


## Extract Files

### tar

```bash
# tar
tar -xzf <file.tar.gz>
```

### zip

```bash
# zip
zip -r my_folder.zip my_folder
unzip my_folder.zip
```

### 7z

```bash
# 7z
yum install -y p7zip
# [e]xtract files from archive
7za e <file.7z>
# [a]dd files from archive
7za a <file.7z>
```

# FileEncryptor
利用Python实现的一个轻量级文件加解密工具，使用AES-CBC模式对一个文件或者对当前目录进行加解密操作，支持Windows/Linux下同时使用。

## Quick start

### Installation

- 依赖加密算法库：[pycryptodome](https://github.com/Legrandin/pycryptodome)

- 安装：`pip install pycryptodome`

### Usage

#### CLI

> FileEncryptor.py -p \<password> [-e/-d/-E/-D] \<filename>

#### Options

```
-h, --help
  show Usage.
-p, --pwd
  enter your password.
-e, --encrypt <filename>
  encrypt the file.
-d, --decrypt <filename>
  decrypt the file.
-E
  encrypt all files in the current directory.
-D
  decrypt all files in the current directory.
```

### Example

- 加密当前目录下所有文件（在当前目录下生成 `lockFile.enc` 文件）

> python FileEncryptor.py -p asdfqwer#@! -E

![](etc/pic1.png)

- 解密 `lockFile.enc` 文件，并还原出完整的文件目录

> python FileEncryptor.py -p asdfqwer#@! -D

![](etc/pic2.png)

## License

This project is licensed under the MIT License - see the [LICENSE](https://github.com/eW1z4rd/AES-FileEncryptor/blob/master/LICENSE) file for details.


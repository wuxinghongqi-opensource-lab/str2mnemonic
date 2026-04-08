# str2mnemonic：字符串 / 密码与助记词双向转换工具



## 项目简介 / Project Overview

**str2mnemonic** 是一款轻量命令行工具，支持将任意字符串、密码、文本内容双向转换为标准助记词，可搭配密钥实现加密转换，兼顾易用性与安全性，适用于密码备份、信息脱敏、离线存储等场景。

str2mnemonic is a lightweight command-line tool that supports bidirectional conversion between arbitrary strings, passwords, text content and standard mnemonics. It can be used with a key for encrypted conversion, combining ease of use and security, suitable for password backup, information desensitization, offline storage and other scenarios.

## 核心特性 / Core Features

- 字符串 ↔ 助记词 无损双向转换

- 支持自定义密钥加密，提升数据安全

- 纯命令行操作，跨平台兼容（Windows 可直接运行 exe）

- 转换结果符合助记词规范，易记、易抄写、易恢复

- Lossless bidirectional conversion between strings ↔ mnemonics

- Support custom key encryption for enhanced data security

- Pure command-line operation, cross-platform compatible (exe directly runnable on Windows)

- Conversion results comply with mnemonic specifications, easy to remember, copy and recover

## 快速使用 / Quick Usage

### 基础转换（无加密）/ Basic Conversion (No Encryption)

#### 编码：字符串 → 助记词 / Encode: String → Mnemonic

```
str2mnemonic.exe --encode "待转换文本/密码"
```

#### 解码：助记词 → 字符串 / Decode: Mnemonic → String

```
str2mnemonic.exe --decode "助记词词组"
```

### 加密转换（带密钥）/ Encrypted Conversion (With Key)

#### 加密编码 / Encrypted Encode

```
str2mnemonic.exe --encode "待转换文本/密码" --key "自定义密钥"
```

#### 加密解码 / Encrypted Decode

```
str2mnemonic.exe --decode "助记词词组" --key "自定义密钥"
```

## 使用示例 / Usage Examples

### 示例 1：基础转换 / Example 1: Basic Conversion

```
str2mnemonic.exe --encode "MyPassword123"
output：act immense arena orphan virus penalty fence wolf jacket carry lemon general elder 

str2mnemonic.exe --decode "act immense arena orphan virus penalty fence wolf jacket carry lemon general elder"
output：MyPassword123
```

### 示例 2：加密转换 / Example 2: Encrypted Conversion

```
str2mnemonic.exe --encode "MyPassword123" --key "MySecretKey"
str2mnemonic.exe --decode "encrypted mnemonic phrase" --key "MySecretKey"
```

## 注意事项 / Notes

1. 解码时**助记词必须完整准确**，否则无法还原。
   The **mnemonics must be complete and accurate** during decoding, otherwise restoration will fail.

2. 加密模式下，**密钥必须与编码时一致**，否则解密失败。
   In encryption mode, the **key must be the same as that used for encoding**, otherwise decryption will fail.

3. 建议妥善保管密钥与助记词，避免丢失或泄露。
   It is recommended to properly keep keys and mnemonics to avoid loss or leakage.

4. 工具仅做本地转换，不上传任何数据。
   The tool only performs local conversion and does not upload any data.

# 😄 Emoji — 用于 AI 聊天的表情包描述与资源库

QQ交流群：[964795310](https://qm.qq.com/q/iWRabmQAE0)

本项目提供一套结构化的表情包数据集，包含**图像 URL** 与 **AI 生成的语义描述**，专为大模型聊天、情感表达增强、多模态交互等 AI 应用场景设计。

---

## 📦 数据格式说明

我们提供两种常用格式，便于不同开发需求：

| 文件            | 字段                                   | 用途                           |
| ------------- | ------------------------------------ | ---------------------------- |
| `emoji.jsonl` | `uuid`, `description`, `url`, `hash` | 适用于需要唯一标识、去重校验或二次开发的场景       |
| `emoji.csv`   | `description`, `url`                 | 适用于向量化、RAG 检索、微调等 AI 训练/推理流程 |

> ✅ 所有字段均经过标准化处理，可直接用于 LLM 或多模态模型输入。

---

## 🌐 图像托管说明

所有表情图片由 **Cloudflare Pages** 提供稳定 CDN 加速服务。

- 原始资源仓库：[mcunc/emoji-src](https://github.com/mcunc/emoji-src)
- 图片 URL 示例：`https://emoji-src.mcunc.net/uuid.jpg``https://src.emoji.mcunc.net/uuid.jpg`

### 🤝 贡献新表情？

1. 将表情文件提交至 [emoji-src 仓库](https://github.com/mcunc/emoji-src)；或使用**长期稳定的第三方云存储**（如阿里云 OSS、腾讯云 COS 等），并确保链接永久有效；
2. 提交 PR 时请附带 `description`（可由 AI 生成）及文件哈希值。

> 💡 **欢迎云厂商赞助对象存储或服务器资源！** 将在 README 中鸣谢 🙏

---

## 🧠 数据来源与审核

### 表情来源

-  **MCUNC 官方贡献 全部来源于 QQ 群聊** ；
- 已通过 **AI 内容安全审核**，过滤违规、敏感或低质及包含个人隐私的内容。

### 描述生成

- 所有 `description` 由 **[阿里云百炼](https://www.aliyun.com/product/bailian)** 大模型生成

---

## 🔒 哈希与去重机制

- 使用 **SHA-256 (HEX 编码)** 对每张图片计算唯一哈希值；
- 贡献前请先校验是否已存在相同 `hash`，避免重复入库；

---

## ⚙️ API 与模型服务

我们正在构建面向开发者的服务体系，包括：

- ✨ **含表情功能预训练AI模型API**
- 🧩 **表情功能mcp接口****

> 🔔欢迎加入QQ群 **[1067667394](https://qm.qq.com/q/uVD2g1Rn1Y)** 了解详情！

---

## ⚠️ 版权与侵权处理

如您认为某表情侵犯您的版权，请通过以下方式联系我们删除：

- 提交 GitHub Issue
- 发送邮件至：**oldpear@mcunc.cn**

请务必提供：

- 表情的 `uuid` 或 `url`
- 权属证明材料（如原图、发布记录等）

我们将在 **7天内** 核实并处理。

---

## ❤️ 致谢

- 特别感谢每一位 PR 提交者与 issue 反馈者！

---



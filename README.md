# 神秘妙妙工具

## Setup

1. 克隆本项目到本地

2. 安装依赖

> 如果你使用uv，请运行
```bash
uv sync
```
> 否则请运行
```bash
pip install requests
```

## 配置说明

编辑 `config.json` 文件，配置你自己的邀请码：

```json
{
  "email_base": "https://mail.chatgpt.org.uk",
  "referral_code": "REF-****",
  "proxy": {
    "enabled": false,
    "http": "",
    "https": ""
  }
}
```

### 代理配置（可选）

如果需要使用代理，请按以下方式配置：

**HTTP代理示例：**
```json
{
  "email_base": "https://mail.chatgpt.org.uk",
  "referral_code": "REF-****",
  "proxy": {
    "enabled": true,
    "http": "http://127.0.0.1:7890",
    "https": "http://127.0.0.1:7890"
  }
}
```

**SOCKS5代理示例：**
```json
{
  "email_base": "https://mail.chatgpt.org.uk",
  "referral_code": "REF-****",
  "proxy": {
    "enabled": true,
    "http": "socks5://127.0.0.1:1080",
    "https": "socks5://127.0.0.1:1080"
  }
}
```

注意：
- 如果不使用代理，请将 `enabled` 设置为 `false`
- SOCKS5 代理需要安装额外的依赖：`pip install requests[socks]`

## 使用方法

### 启动程序

> 如果你使用uv，请运行
```bash
uv run main.py
```
> 否则请运行
```bash
python main.py
```

## 免责声明

本工具仅供学习和研究使用，请遵守相关服务的使用条款。使用本工具产生的任何后果由使用者自行承担。
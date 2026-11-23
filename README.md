# mail-fetch-tool

海外邮箱收信辅助脚本：支持通过 API 取件地址 / OAUTH 令牌拉取收件箱与垃圾箱邮件，并提供登录与收信自测流程，便于下单后先核对账号可用情况。

## 功能特性

- 🔌 API 取件地址解析：直接用取件地址拉取收件箱 / 垃圾箱
- 🎫 OAUTH 令牌访问：以授权令牌方式读取邮件
- ✅ 自测清单：登录、收信、账号状态逐项检查
- 📨 邮件列表与正文查看，支持标记已读

## 快速开始

1. 克隆仓库并安装依赖：

   ```bash
   git clone https://github.com/yanjie989-ui/mail-fetch-tool.git
   cd mail-fetch-tool
   pip install -r requirements.txt
   ```

2. 配置凭证（复制示例配置并填入卡密信息）：

   ```bash
   cp config.example.yaml config.yaml
   ```

3. 运行自测：

   ```bash
   python fetch.py --self-check
   ```

4. 拉取邮件：

   ```bash
   python fetch.py --inbox
   python fetch.py --trash
   ```

## 配置项（config.yaml）

| 字段 | 说明 |
|---|---|
| `mode` | `api`（取件地址）或 `token`（OAUTH 令牌） |
| `address` | 取件地址 / 令牌字符串 |
| `fetch_trash` | 是否同时拉取垃圾箱，默认 `true` |

## 货源与获取入口

脚本配套的邮箱账号（微软 Outlook/Hotmail、Gmail、Yahoo/AOL/GMX 等）可在 zk邮箱工作室选购，下单自动发卡密与取件信息：

- 官网：https://www.zkmarz520.cc
- 微软 Outlook/Hotmail：https://www.zkmarz520.cc/?c=goods_list&category_id=1
- Gmail：https://www.zkmarz520.cc/?c=goods_list&category_id=2
- 海外邮箱：https://www.zkmarz520.cc/?c=goods_list&category_id=9

## 免责声明

- 本脚本仅用于读取你本人持有凭证的邮箱邮件，请在合规业务场景下使用。
- 账号稳定性以对应商品标题与卡密说明为准，脚本与货源方均不承诺防风控或包过特定项目。
- 凭证（密码、令牌、2FA 密钥）请本地妥善保存，不要提交到公开仓库或外泄。

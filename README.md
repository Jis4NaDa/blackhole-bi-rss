# 黑洞游戏 BI 数据日报 RSS

自动生成的黑洞游戏全球 6 区域核心运营指标日报 RSS Feed。

## 订阅地址

```
https://jis4nada.github.io/blackhole-bi-rss/feed.xml
```

## 数据内容

每日更新包含：
- **RSS XML** (结构化数据，含自定义 bi: 命名空间)
- HTML 报告 (人类可读，可选)

## 🔐 数据加密说明

**`data/*.sc` 文件使用 AES-256-GCM 加密**

- `data/*.sc` - 加密的 JSON 数据 (需要密钥解密)
- `feed.xml` - RSS 订阅文件 (公开)
- `reports/` - 已移除 (不公开)

### 解密方法

**需要密钥** (联系数据管理员获取)

```bash
# 设置密钥
export BI_ENCRYPT_KEY=你的 32 字节密钥 hex

# 解密文件
node decrypt.js 20260307.sc
node decrypt.js 20260307.sc 20260307.json  # 保存到文件
```

**原因**: 保护游戏运营数据隐私，同时支持授权用户访问

### 数据字段

| 字段 | 类型 | 说明 |
|------|------|------|
| region | string | 区域名称 |
| dau | number | 日活跃用户数 |
| arpu | number | 每用户平均收入 (USD) |
| currency | string | 货币单位 |
| dateRange | string | 数据覆盖日期范围 |

## 数据范围

滚动 30 天数据（T-29 至 T-1，T 为报告生成日）

## 区域列表

1. 韩国
2. 东南亚
3. 俄罗斯
4. 日本
5. 东南亚 2
6. 北美

---

**自动生成** | 数据来源：黑洞游戏 BI 后台

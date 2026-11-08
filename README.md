# SurgeModules

自用 Surge 配置仓库。

## 模块

| 文件 | 说明 |
|---|---|
| `MiniAds.sgmodule` | 京东 / 拼多多 / 美团 / 得物 / 波点音乐 / 中国联通 去广告合集 |

## 安装

Surge → 首页 → 模块 → 添加模块，粘贴：

```
https://raw.githubusercontent.com/shijieheping0/SurgeModules/main/MiniAds.sgmodule
```

国内更快（jsDelivr）：

```
https://cdn.jsdelivr.net/gh/shijieheping0/SurgeModules@main/MiniAds.sgmodule
```

## 模块结构

- `[Rule]` 域名 / IP 级拦截
- `[Body Rewrite]` 用 jq 语法裁剪响应 JSON
- `[Map Local]` 把纯广告接口直接返回 `{}`
- `[Script]` 复杂逻辑脚本
- `[MITM]` 上面所有改写的前提，缺了不生效

## 注意

- 装模块后需要在 Surge 的 MITM 证书已信任（设置里显示绿色对勾）
- 改完模块若没生效，去 App 里清一次缓存

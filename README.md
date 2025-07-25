# Cloudflare ASN 信息库 (CF-ASN)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

📚 一个致力于收集和分享 Cloudflare **ASN (自治系统号)** 信息的开源项目。

本项目旨在提供一个清晰、准确、可访问的资源，帮助开发者、网络管理员、安全工程师和研究人员了解 Cloudflare 的网络基础设施。我们收集了 Cloudflare 官方公开的 ASN 描述、ASN 号以及每个 ASN 所拥有的完整 CIDR IP 地址段。

## 🤝 应用场景
* 防火墙/安全组配置: 将 CIDR 列表导入您的防火墙规则，以允许或限制来自 Cloudflare 的流量。
* 路由策略: 在您的网络设备上配置基于 Cloudflare ASN 的路由。
* 数据分析: 在日志分析或网络监控工具中，使用这些数据来识别和标记 Cloudflare 的流量。
* 开发集成: 将其作为数据源集成到您的应用程序中。
* IP的优选：利用相关工具，基于延迟和速度测试，筛选最佳IP地址，以实现更快的网络连接。

## 🌐 数据来源与更新
CIDR 数据: 来源于 Cloudflare 官方发布的 IP 地址列表 (https://www.cloudflare.com/ips/ )。
ASN 信息: 通过查询公共的互联网注册机构 (如 RIPE, ARIN) 获取。

## 📚 什么是 ASN 和 CIDR？

*   **ASN (Autonomous System Number)**: 自治系统号，是互联网上一个独立网络（如 ISP 或大型公司）的唯一身份标识。Cloudflare 作为一个大型网络，拥有多个 ASN。
*   **CIDR (Classless Inter-Domain Routing)**: 一种表示 IP 地址块的方法，格式为 `IP地址/前缀长度` (例如 `1.1.1.0/24`)。它定义了一组连续的 IP 地址。

您可以将 ASN 理解为一个“网络王国”的身份证，而 CIDR 则是这个王国所拥有的“IP 土地”范围。

## 📦 项目内容

本仓库的核心内容是基于 Cloudflare ASN 结构化的 JSON 和 TXT 数据，包含以下信息：

*   **`ASN`**: ASN 号码 (例如 `AS13335`)。
*   **`Description`**: 该 ASN 的官方描述 (例如 `CLOUDFLARENET - Cloudflare, Inc.`)。
*   **`CIDR`**: IP地址列表（IPV4 和 IPV6），包含了 Cloudflare 不同 ASN 拥有的所有 CIDR IP 地址段。
*   **`aggregated.json`**:  ASN 对应的 CIDR 地址（JSON 格式），包含 IPv4 和 IPv6。
*   **`ipv4-aggregated.txt`**: ASN 对应的 CIDR IPV4 地址（TXT 格式）。
*   **`ipv6-aggregated.txt`**: ASN 对应的 CIDR IPV6 地址（TXT 格式）。
*   **`cf-asn-list.txt`**: 一个纯文本格式的 CIDR 列表（只包括 ASN13335 和 ASN209242），便于直接导入防火墙、路由设备和进行筛选。
*   **`ASN-INFO.txt`**: Clourflare 相关的 ASN 及其描述文本。

## 🛠️ 如何使用

### 1. 获取数据

您可以直接克隆此仓库或下载相关文件。

```bash
git clone https://github.com/TYOYO1/CF-ASN.git
cd CF-ASN
```

## 📄 其他
无 ASN133877, "Cloudflare Hong Kong, LLC" CIDR数据。

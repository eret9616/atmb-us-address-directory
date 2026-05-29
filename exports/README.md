# Gold Addresses 筛选结果

基于 juzhp/atmb-us-address-directory 抓取 + Smarty 校验的输出。

筛选条件:`CMRA = N` **AND** `RDI = Residential`,从 2092 个 ATMB 地址中筛出 **115** 个候选。

## 文件

- **gold-addresses.html** — 交互式表格,在浏览器打开即可。支持:
  - 按 州 / 城市 / 价格 排序
  - 关键字搜索
  - 税务筛选:🟢 免消费税 / 🟡 免所得税 / 🩷 两税全免
  - 地区筛选:西/东/南/中西部
  - 价格区间筛选(≤$10 / $10-20 / >$20)
  - 每行 3 个按钮:🗺️ Google Maps / 📷 街景 / 🏠 ATMB 详情
- **gold-addresses.csv** — 原始 CSV
- **gold-with-maps.csv** — 带 Google Maps URL 的 CSV

## 税务分类(115 条里的分布)

| 类型 | 州 | 数量 |
|------|----|------|
| 🟢 免消费税(收包裹) | OR / NH / DE / MT / AK | 4 |
| 🟡 免所得税(银行/居住) | AK / FL / NV / SD / TN / TX / WA / WY / NH | 32 |
| 🩷 两税全免(顶配) | NH / AK | 1(NH Laconia) |

## 注意

- `RDI = Residential` 来自 USPS,不代表实际就是住宅;部分小型 Mailbox 店没向 USPS 注册 CMRA,会通过过滤但实际是商业地址。建议每个候选都在 Google Maps 上确认一下街景。
- 跨州免税(寄到 OR/NH 等免消费税州)对大平台(Amazon/Apple 等已有 nexus)无效,只对小商家/部分独立站有效。

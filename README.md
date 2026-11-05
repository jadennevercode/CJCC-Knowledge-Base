# CJCC Knowledge Base

NAND 与存储产业链知识库，按建设范围表划分为 13 个知识模块和 3 类业务材料，首期优先级均为 P0。

## 目录

```text
CJCC-Knowledge-Base/
├── README.md
├── 01-foundations/                      # 基础知识
│   ├── 01-terminology-metrics/           # 行业术语与指标
│   ├── 02-companies-organization/        # 厂商与组织结构
│   └── 03-nand-products-technology/      # NAND 产品与技术谱系
├── 02-upstream/                         # 上游
│   └── 01-semiconductor-materials/      # 半导体级原材料
├── 03-midstream/                        # 中游
│   ├── 01-supply-capacity/              # 供给形成与产能决策
│   └── 02-fabs-manufacturing-sites/     # 重点工厂与制造基地
├── 04-products/                         # 产品
│   └── 01-nand-to-finished-products/    # NAND 到 SSD、eMMC/UFS 等成品的映射
├── 05-downstream/                       # 下游
│   ├── 01-applications-demand/          # 应用与需求结构
│   └── 02-cloud-ai-demand/              # 云计算与 AI 需求传导
├── 06-cross-chain/                      # 跨链分析
│   ├── 01-inventory-procurement/        # 库存与采购概念
│   ├── 02-supply-demand-pricing/        # 供需与价格口径
│   ├── 03-events-cases/                 # 事件分类与历史案例
│   └── 04-policy-event-interactions/    # 政策及多事件交互
└── 07-business-inputs/                  # 业务材料
    ├── 01-scope-and-definitions/        # 建设范围与口径确认单
    ├── 02-relationship-corrections/     # 关键关系纠错与内部补充清单
    └── 03-event-rule-review/            # 典型事件规则审核表
```

## 内容范围与建议来源

| 目录 | 主要内容 | 建议来源 |
| --- | --- | --- |
| [基础知识](01-foundations/) | 术语与指标；Samsung、SK hynix、Kioxia、Sandisk、Micron、YMTC 等厂商及组织关系；TLC/QLC 产品与技术代际 | 原厂手册与白皮书，JEDEC、ONFI、NVMe 标准，招股书与年报，ISSCC、IEDM 论文，YOLE |
| [上游](02-upstream/) | 高纯多晶硅、单晶硅锭、半导体硅片、光刻胶、特种气体 | 行业专题研究、券商半导体产业周评 |
| [中游](03-midstream/) | 投片、稼动率、bit 产出、扩减产、Capex、产品组合；工厂、基地及运营主体 | 原厂财报与业绩会、投资者材料、建设扩产公告，Omdia、TrendForce |
| [产品](04-products/) | 企业级及消费级 SSD、eMMC/UFS、存储卡、U 盘；原厂与模组厂产品映射 | 产品手册、规格书、应用白皮书，Omdia SSD and HDD Storage Market Tracker |
| [下游](05-downstream/) | 数据中心、手机、PC、平板等应用的出货与存储需求；云厂商及 AI 需求传导 | Omdia 数据库，云厂商年报、Capex 披露与业绩会，服务器与数据中心研究 |
| [跨链分析](06-cross-chain/) | 库存与采购、供需及价格口径；停产、污染、客户变更案例及反例；政策与多事件交互 | 财报存货附注、Omdia、TrendForce、企业及交易所公告、政府政策原文、历史事件研究 |
| [业务材料](07-business-inputs/) | 首期范围与指标口径、关键关系纠错、事件规则审核 | 已有产品目录、数据字典、模型说明及经授权的业务资料 |

## 使用方式

- 资料直接放入对应子目录，按内容命名；不要求每个目录单独写 README。
- 研究笔记可用 Markdown，其他资料按需保留原格式；记录来源、日期及必要的指标口径。
- 空目录用 `.gitkeep` 占位，有实际文件后可删除。
- 当前仅建立目录，资料待补充。公开仓库不上传未经授权的付费报告或客户敏感材料。

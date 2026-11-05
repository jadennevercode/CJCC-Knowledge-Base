# CJCC Knowledge Base

面向 NAND 与存储产业链研究的知识库。按照建设范围表组织行业基础、供给形成、产品映射、需求传导和跨链事件分析，为资料检索、指标对齐、历史案例复盘与业务规则审核提供统一入口。

**当前状态：知识库框架已初始化，13 个 P0 知识模块与 3 类 P0 业务材料已建立；事实内容、外部来源和业务规则尚待采集、核验。** 下文列出的厂商、机构和文献类型是覆盖范围或建议来源，不代表已完成研究或获得数据授权。

## 快速开始

- **查知识**：从下方模块表进入；术语、厂商和技术先查基础知识。
- **补资料**：先登记[来源](08-sources/README.md)，再复制[条目模板](09-templates/README.md)到对应模块。
- **定范围与口径**：填写[建设范围与口径确认单](07-business-inputs/01-scope-and-definitions/README.md)。
- **补关键关系**：填写[关系纠错与内部补充清单](07-business-inputs/02-relationship-corrections/README.md)，未知项保留未知。
- **审事件规则**：结合[历史案例](06-cross-chain/03-events-cases/README.md)，填写[典型事件规则审核表](07-business-inputs/03-event-rule-review/README.md)。

## 目录结构

目录使用稳定的英文路径，文档使用中文标题。编号表示浏览顺序，所有附件模块的初始优先级均为 P0。

```text
CJCC-Knowledge-Base/
├── README.md
├── CONTRIBUTING.md                    # 录入、引用、审核与更新规则
├── 01-foundations/
│   ├── 01-terminology-metrics/         # 术语、定义与指标
│   ├── 02-companies-organization/      # 厂商、品牌、子公司与合资关系
│   └── 03-nand-products-technology/    # NAND 产品与技术谱系
├── 02-upstream/
│   └── 01-semiconductor-materials/    # 半导体级原材料
├── 03-midstream/
│   ├── 01-supply-capacity/            # 供给形成与产能决策
│   └── 02-fabs-manufacturing-sites/   # 工厂、基地与运营主体
├── 04-products/
│   └── 01-nand-to-finished-products/  # NAND 到 SSD / eMMC / UFS 等成品
├── 05-downstream/
│   ├── 01-applications-demand/        # 终端应用、搭载量与 bit 需求
│   └── 02-cloud-ai-demand/            # 云计算与 AI 需求传导
├── 06-cross-chain/
│   ├── 01-inventory-procurement/      # 库存、采购与消耗
│   ├── 02-supply-demand-pricing/      # 供需、价格与统计口径
│   ├── 03-events-cases/               # 事件分类、案例与反例
│   └── 04-policy-event-interactions/  # 政策、多事件共享瓶颈与反馈
├── 07-business-inputs/
│   ├── 01-scope-and-definitions/      # 业务材料① 范围与口径确认
│   ├── 02-relationship-corrections/   # 业务材料② 关键关系纠错与补充
│   └── 03-event-rule-review/          # 业务材料③ 典型事件规则审核
├── 08-sources/                        # 来源登记；授权原文的引用入口
└── 09-templates/                      # 知识、实体、指标、事件、来源模板
```

各目录均有 README；无需使用空的占位目录。事实条目随资料采集逐步新增。

## 附件模块对照与导航

| 优先级 | 环节 / 知识模块 | 对应目录与覆盖重点 |
| --- | --- | --- |
| P0 | 行业术语与指标 | [进入模块](01-foundations/01-terminology-metrics/README.md)：NAND、TLC/QLC、晶圆、裸片、SSD、eMMC/UFS；bit 量、产能、产出、稼动率、良率、ASP、供需比、TSV、堆叠等。 |
| P0 | 厂商与组织结构 | [进入模块](01-foundations/02-companies-organization/README.md)：Samsung、SK hynix、Kioxia、Sandisk、Micron、YMTC 及各产品线重点企业；子公司、品牌、合资实体、历史名称。 |
| P0 | NAND 产品与技术谱系 | [进入模块](01-foundations/03-nand-products-technology/README.md)：各原厂 TLC/QLC 产品、容量规格、主要技术代际与架构。 |
| P0 | 半导体级原材料 | [进入模块](02-upstream/01-semiconductor-materials/README.md)：硅料（高纯多晶硅、单晶硅锭、半导体硅片）、光刻胶、特种气体。 |
| P0 | 供给形成与产能决策 | [进入模块](03-midstream/01-supply-capacity/README.md)：晶圆投片、稼动率、bit 产出、扩产、减产、Capex 及产品组合。 |
| P0 | 重点工厂与制造基地 | [进入模块](03-midstream/02-fabs-manufacturing-sites/README.md)：主要 NAND 原厂的工厂、生产基地、运营主体、所在地区及合资关系。 |
| P0 | NAND 到成品的映射 | [进入模块](04-products/01-nand-to-finished-products/README.md)：企业级 SSD、消费级 SSD、eMMC/UFS、存储卡、U 盘；原厂及重点模组厂。 |
| P0 | 应用与需求结构 | [进入模块](05-downstream/01-applications-demand/README.md)：数据中心、手机、PC、平板及其他主要应用；设备出货、存储搭载量与 bit 需求。 |
| P0 | 云计算与 AI 需求传导 | [进入模块](05-downstream/02-cloud-ai-demand/README.md)：Microsoft、Amazon、Google、Meta 等需求观察对象；服务器、存储系统及设备供应链。 |
| P0 | 库存与采购概念 | [进入模块](06-cross-chain/01-inventory-procurement/README.md)：原料、在制品、原厂成品、渠道、OEM 库存；采购、消耗、备货、去库存。 |
| P0 | 供需与价格口径 | [进入模块](06-cross-chain/02-supply-demand-pricing/README.md)：分产品供给、需求、供需比；晶圆、裸片、SSD、eMMC/UFS 价格。 |
| P0 | 事件分类与历史案例 | [进入模块](06-cross-chain/03-events-cases/README.md)：优先覆盖工厂停产、材料污染、重点客户需求或设计变更；同时收录未造成明显损失、未触发或被缓冲的反例。 |
| P0 | 政策及多事件交互 | [进入模块](06-cross-chain/04-policy-event-interactions/README.md)：出口限制、关税、地区冲突；多事件共享瓶颈、替代及反馈关系。 |
| P0（业务） | 建设范围与口径确认单 | [确认范围](07-business-inputs/01-scope-and-definitions/README.md)：首期产品、应用、厂商及供给、需求、库存、供需比、AI 候选清单。 |
| P0（业务） | 关键关系纠错与内部补充清单 | [补充关系](07-business-inputs/02-relationship-corrections/README.md)：客户/供应商关系、依赖与替代限制、关键缺口及冲突。 |
| P0（业务） | 典型事件规则审核表 | [审核规则](07-business-inputs/03-event-rule-review/README.md)：停产、材料污染、客户需求或设计变更三类事件及反例。 |

## 内容如何关联

以“企业—工厂—技术/产品—成品—应用”为检索主线，供给、需求、库存、价格与事件条目通过稳定编号及相对链接关联。每项关系保留证据、适用范围和有效期。

例如，分析某基地停产时，依次引用基地档案、所涉产品、产能口径、库存缓冲与替代条件，再记录影响及恢复过程。**这是分析路径示例，不是已验证的因果结论。** 多个事件影响同一基地或同一批产品时，应说明重叠范围，避免重复计算。

## 资料与证据原则

1. 优先追溯原始披露、技术文件与标准；研究机构材料保留数据库版本及统计口径。
2. 数据注明单位、时间、地区、产品规格；产能与产出、计划与实际、出货与消耗分别记录。
3. 区分“来源披露的事实”“研究推断”“业务确认”；AI 整理内容初始状态为草稿。
4. 来源变更或结论失效时保留修订记录；未知值不以零值或默认关系代替。
5. 公开仓库仅收录可公开内容。付费报告、客户 BOM、供应商名单、认证采购资料等仅在获得公开授权后入库；否则使用脱敏摘要或不暴露敏感信息的引用编号。Git 仓库本身不提供目录级访问控制。

来源类型与收集指引见[来源目录](08-sources/README.md)，具体命名、审核和维护方法见[贡献指南](CONTRIBUTING.md)。

## 首批建设清单

- [ ] 确认首期产品、应用、厂商清单与统一指标口径。
- [ ] 登记首批原始资料，建立术语、企业、技术及基地条目。
- [ ] 补全供给—成品—需求映射，显式记录未确认关系。
- [ ] 建立库存与价格口径，注明可比范围与不能直接比较的条件。
- [ ] 各完成至少一个停产、材料污染、客户需求/设计变更案例，并补充反例。
- [ ] 由工艺、供应链、销售等相关业务人员审核事件规则，记录结论与适用边界。

以上均为待办，不表示已有审核或业务确认。

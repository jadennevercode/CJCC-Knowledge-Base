# CJCC 半导体行业材料处理说明

本项目将 164 份半导体行业材料整理为可追溯的全文，并从中筛出可用于分析外部冲击、产业依赖和业务影响的原文。查找相关证据可从[筛选结果](materials_md_relevant/)开始。需要查看被省略的上下文时，可按相同目录和文件名打开[清洗全文](materials_md_cleaned/)。

| 阶段 | 位置 | 本批次产物 |
| --- | --- | --- |
| 原始材料 | [materials/](materials/) | 96 份 PDF 和 68 份 HTML/HTM 快照 |
| 转换为 Markdown | [materials_md/](materials_md/) | 164 份全文，其中 PDF 共 4,590 页 |
| 清洗与复核 | [materials_md_cleaned/](materials_md_cleaned/) | 164 份结构化全文，附图像、处理记录与待核验项 |
| 外部冲击相关性筛选 | [materials_md_relevant/](materials_md_relevant/) | 144 份原文摘录，另 20 份经筛选无符合条件的段落 |

其中 131 份为原批次（火山引擎 OCR），新增的 33 份（32 份 PDF、1 份 HTML）按同一目录结构和两个环节补入，PDF 采用多模态逐页转录。新增 33 份的清洗稿尚未逐页人工复核，引用时请先查复核台账。

以上按源文档计数。目录说明、处理清单、图片，以及补全同一报告所用的文件均不另计。

原有的行业分类说明、业务审核表和条目模板统一收在[知识库建设框架](docs/knowledge-guide/README.md)。新增条目时可查阅[贡献指南](CONTRIBUTING.md)。

## 1. 原件获取与转换

材料取自 CJCC-Knowledge-Base 的 `materials/` 快照。各阶段沿用原分类目录，转换时在原文件名后追加 `.md`，因此同名网页和 PDF 仍可区分。Air Liquide 2025 年报的仓库副本被截断，转换时采用从官网补全的 432 页版本。完整原件已归入原分类，见 [Air Liquide 2025 年报](materials/%E4%B8%8A%E6%B8%B8%EF%BC%9A%E5%8D%8A%E5%AF%BC%E4%BD%93%E7%BA%A7%E5%8E%9F%E6%9D%90%E6%96%99/S8d9a8e162c88_airliquide.com_air-liquide-2025-universal-reg.pdf)。

- **PDF** 原批次使用火山引擎 `OCRPdf v3` 的 OCR 模式逐页识别正文和表格。新增 33 份中的 PDF 采用多模态逐页转录：逐页渲染为图像后由模型转录，再用 PDF 文本层交叉核对数字与专有名词，转换记录中的 `method` 字段注明所用方法。插图按识别坐标或图注区域从原件裁出，无识别文本的页面保留整页图。Markdown 中的来源页标记用于与 PDF 对照。
- **HTML/HTM** 从保存的网页快照提取正文、表格、链接及图片引用。有内嵌文章正文时一并提取。部分动态内容或图片未随快照保存，外部图片仍依赖原网站。

[转换清单](materials_md/conversion_manifest.json)记录各文档的源文件、转换方式、适用页数和转换稿的 SHA-256 校验值。[文档索引](materials_md/README.md)可按分类打开各份转换稿。

## 2. 全文清洗与复核

先清除重复页眉及可确认为版式元素的独立页码，再按文件分工，对照来源页检查 OCR、断句、标题层级、脚注和表格。跨页续句或续表按已能确认的上下文衔接。表格复核关注列头、单位、报告期和跨页首行，尤其保留零值、缺失值和不适用项之间的区别。

清洗稿按文档元数据、结构化正文和处理备注组织。元数据无法确定时使用 `null`。识读存疑的片段保留原文并标注 `[OCR_UNCERTAIN]`，无法辨读处用 `[OCR_UNREADABLE]`，行列关系无法可靠恢复的表格用 `[TABLE_RECONSTRUCTION_UNCERTAIN]`。

**清洗覆盖与筛选覆盖分别统计。** 清洗目录现有记录将 164 份中的 107 份列为已完整复核，新增 33 份标记为待人工复核；表格队列仍有 785 条标为待人工复核，另有 4 份网页在复核时发现动态内容缺失。引用具体数字时，可查[复核进度](materials_md_cleaned/review_progress.json)和[表格复核队列](materials_md_cleaned/table_review_queue.json)，再与原表对照。

## 3. 外部冲击相关性筛选

以清洗全文为输入，按段落、列表或表格判断相关性。同一章节内分别取舍，保留理解原文所需的标题、定义、主语、单位、脚注及条件。判断采用 A–E 类别和 0–5 分相关性口径，最终 Markdown 直接呈现原文摘录，分类与分数不写入正文。

| 类别 | 取舍依据 |
| --- | --- |
| A 外部冲击 | 保留涉及具体对象或范围的政策限制、灾害、资源中断或需求冲击等原文。 |
| B 影响与应对 | 保留与冲击或风险暴露明确相关的产能、成本、交付、需求、营收变化及应对措施，并沿用“可能”“预计”“已发生”等原文表述。 |
| C 产业依赖 | 即使未提及已发生的冲击，也保留有实质意义的供应关系、集中度、材料或设备依赖、替代难度和产能约束。 |
| D 技术与行业背景 | 保留能解释上述依赖或约束的技术细节，例如限制供应切换的兼容条件。 |
| E 无关内容 | 过滤常规治理、宣传、孤立的财务数字、普通规格和重复版式内容。 |

文件按文档并行筛选，长篇规范拆分到明确的来源页范围，再按页序合并。144 份文件含有可保留原文。其余 20 份可在前两阶段查看全文。交付时检查了筛选稿的页码顺序、本地图片引用和 Markdown 表格列数，并对可匹配的长段文字做了来源页比对。

## 4. 怎样从摘录回到原件

以 [WPG 年报筛选稿](materials_md_relevant/流通：渠道与交易关系/43_wpgholdings.com_ARP00000038.pdf.md)为例，在文内查找 `[Source Page: 99]`，即可定位该页摘录。打开[同名清洗全文](materials_md_cleaned/流通：渠道与交易关系/43_wpgholdings.com_ARP00000038.pdf.md)可补读上下文，再打开[原始 PDF](materials/流通：渠道与交易关系/43_wpgholdings.com_ARP00000038.pdf)核对图文。该页对同一预测增幅分别给出 21.0% 和 32.6%，第 109 页的销售金额与占比也存在不一致。引用时应指明采用的是正文还是图表。

筛选稿中的页码可以跳号，表示只摘录了部分页面。网页可通过文档元数据中的 `Source File`、原始快照和章节标题定位。部分筛选稿的图片使用指向相邻清洗目录的相对路径，迁移材料时应保留目录之间的位置关系。AT&S 年报第 42 页清洗源有不完整片段，引用该处时应回查原件。

这批筛选材料随后用于整理外部事件资料库和事实库。下游的抽取、建库及本体验收记录在本地《本体构建报告 1.0.0》中。

## 5. 各环节的任务 Prompt

以下按处理顺序收录定义任务的用户原文。清洗和相关性筛选两段保留全文。

### 5.1 全文清洗与结构化

````text
基于materials_md再进行cleaning，放到一个新的平行文件夹

# Role

You are a professional Document Processing and Structuring Specialist, specializing in semiconductor industry documents, including annual reports, technical reports, industry research, regulatory documents, and supply chain analysis.

Your task is to transform OCR-extracted text into clean, well-structured, semantically coherent, and traceable content suitable for downstream knowledge extraction and ontology construction.

You are NOT responsible for summarization, relevance filtering, knowledge extraction, or ontology generation.

# Objective

Convert raw OCR text into high-quality structured Markdown while preserving all meaningful information, technical accuracy, numerical data, document hierarchy, and source traceability.

# Processing Instructions

## 1. OCR Noise Cleaning

Identify and correct OCR-related formatting issues:

- Remove repeated page headers, footers, page numbers appearing as standalone layout artifacts, watermarks, and duplicated OCR text.
- Repair broken words, incorrect line breaks, fragmented sentences, and unnecessary whitespace.
- Correct obvious OCR recognition errors only when the intended text is unambiguous.
- Preserve original technical terminology, semiconductor process names, company names, product names, chemical formulas, measurement units, and numerical values.
- Do not change uncertain terms or values based on assumptions.
- Preserve meaningful footnotes, references, annotations, and disclaimers associated with substantive claims.

Do NOT remove paragraphs simply because they seem irrelevant to the semiconductor industry or external shock analysis.

## 2. Document Hierarchy Reconstruction

Reconstruct the logical document structure:

- Identify document titles, chapter headings, section headings, and subsection headings.
- Represent headings using Markdown hierarchy (#, ##, ###, ####).
- Associate paragraphs with their correct parent sections.
- Merge paragraphs incorrectly split by OCR or page boundaries when continuity is clear.
- Separate paragraphs that represent distinct topics.
- Preserve the original order of document content.

Do not invent headings or modify the logical organization of the document unless required to repair an obvious OCR layout error.

When the heading hierarchy is uncertain, retain the original heading text without inventing a hierarchical relationship.

## 3. Table Reconstruction

Identify tabular content and reconstruct it into Markdown tables when the structure can be recovered reliably.

Requirements:

- Preserve all row and column relationships.
- Preserve original column headers, categories, numerical values, percentages, currencies, units, and reporting periods.
- Preserve associated table titles, notes, and data sources.
- Preserve explicit distinctions between missing values, zero values, and not-applicable values.
- Do not calculate, estimate, interpolate, or infer missing data.
- Do not merge cells if doing so may alter their meaning.

If a table cannot be reconstructed reliably, retain its original text and mark it as:

[TABLE_RECONSTRUCTION_UNCERTAIN]

If OCR text lacks sufficient information to establish row-column relationships, do not fabricate a Markdown table.

## 4. Semantic Continuity Restoration

Restore readable paragraphs without changing their substantive meaning.

- Join sentences broken by line endings or page boundaries.
- Preserve causal expressions, conditional statements, temporal relationships, qualifiers, and uncertainty.
- Preserve distinctions such as "may", "could", "expected", "estimated", "reported", and "confirmed".
- Preserve negations, exceptions, and scope limitations.
- Keep all original facts, claims, and technical descriptions intact.

Do not paraphrase, summarize, simplify, or reinterpret the original content.

## 5. Semiconductor Terminology Preservation

Apply special care to semiconductor terminology, including but not limited to:

- Semiconductor materials, wafers, substrates, chemicals, and gases
- Lithography, deposition, etching, packaging, and testing
- Foundry, fabless, IDM, OSAT, and equipment suppliers
- Process nodes and manufacturing technologies
- Capacity, utilization, yield, lead time, inventory, and supply constraints
- Export controls, sanctions, tariffs, regulatory restrictions, and geopolitical risks

Preserve original terminology and abbreviations.

Do not normalize technical concepts into different terms unless the source explicitly defines them as equivalent.

## 6. Source Traceability

Preserve available source metadata:

- Document name
- Document type
- Company or issuing organization
- Publication date
- Reporting period
- Source page number
- Original section title

Retain page references so each structured passage can be traced back to its original document.

If metadata is unavailable, use null rather than inventing values.

Use explicit source page markers where available:

[Source Page: 12]

Do not treat a page number appearing in a table of contents or citation as the source page.

## 7. Uncertainty Handling

When OCR content is unclear, corrupted, or incomplete:

- Preserve the uncertain source fragment whenever possible.
- Flag the affected text with [OCR_UNCERTAIN].
- Flag missing or illegible content with [OCR_UNREADABLE].
- Do not guess missing numbers, dates, technical terms, or entity names.
- Do not silently correct ambiguous content.

## 8. Content Preservation Rules

Strictly prohibited:

- Summarizing the document
- Filtering content based on relevance
- Extracting entities or relationships
- Generating ontology classes or properties
- Adding information not present in the source
- Inferring unstated causal relationships
- Altering numerical values or reporting periods
- Removing technical or business information
- Rewriting the author's claims into stronger assertions

# Output Format

Return the processed document in the following structure:

## Document Metadata

- Document ID:
- Document Title:
- Document Type:
- Issuing Organization:
- Publication Date:
- Reporting Period:
- Source File:

Use null for unavailable information.

## Structured Content

Use Markdown headings, paragraphs, lists, and tables.

Preserve available source page markers.

## Processing Notes

Report only material processing issues, including:

- Uncertain OCR segments
- Unrecoverable tables
- Missing pages or text discontinuities
- Ambiguous document hierarchy
- Uncertain metadata

If no material issues exist, return "None".

# Quality Checklist

Before returning the result, verify:

1. No meaningful content has been intentionally omitted.
2. All numerical values and measurement units are preserved.
3. Section hierarchy reflects the source.
4. Table structures are not fabricated.
5. Uncertain text is clearly flagged.
6. Original causal, temporal, and conditional expressions are unchanged.
7. Source traceability is retained.
8. No summarization, relevance filtering, or ontology extraction has been performed.

# Final Instruction

Prioritize factual fidelity and traceability over readability or stylistic improvement.

When uncertain, preserve the original content and flag the uncertainty rather than making assumptions.
````

### 5.2 外部事件冲击相关性筛选

````text
帮我进行pipeline的下一步 外部事件冲击相关内容筛选，在一个新文件夹中维护，如果有相关内容就保留md，没有就无需保留



你是一名半导体行业知识工程专家，熟悉半导体产业链、制造工艺、关键技术、供应链结构及外部风险传导机制。

你的任务是对已完成 OCR 的行业文档进行**知识相关性筛选（Knowledge Relevance Screening）**，判断输入文本是否包含值得保留、供后续构建“芯片行业外部冲击影响本体（Semiconductor External Shock Impact Ontology）”使用的知识。

**注意：本阶段只负责相关性判断、知识分类与相关文本定位，不负责构建本体、不生成因果关系、不进行完整实体关系抽取。**

**1. Ontology Objective**

目标本体旨在支持理解和分析：

- **External Shock**：哪些外部事件或环境变化可能冲击半导体产业。

* **Affected Entity**：哪些企业、地区、产品、技术或产业链环节可能受到影响。

- **Industry Dependency**：产业链中存在哪些技术、设备、材料、产能及供应关系依赖。

* **Impact Mechanism**：外部冲击可能通过哪些路径传导。

- **Business Impact**：可能产生哪些产能、成本、供应、需求、收入、交付或战略影响。

筛选时不仅关注已经发生的冲击和影响，还应关注能够支持未来冲击分析的**稳定产业事实、关键依赖关系、技术瓶颈与潜在脆弱性**。

**2. Knowledge Classification**

对输入文本识别以下知识类别，允许一个文本块属于多个类别。

**A — External Shock Knowledge**

外部冲击事件、政策及环境变化，包括但不限于：

- 出口管制、贸易限制、关税、经济制裁

* 地缘政治冲突、国际关系变化

- 自然灾害、公共卫生事件

* 能源、水资源或其他关键资源供应中断

- 宏观经济变化、市场需求冲击

* 关键材料供应危机、物流与运输中断

重点关注事件的性质、涉及对象、作用范围以及时间或地域信息。

**B — Impact Knowledge**

外部冲击对半导体企业或产业链造成的实际、潜在或预测影响，例如：

- 产能受限、停产或扩产延期

* 原材料或设备获取受阻

- 制造成本、采购价格或运营成本变化

* 交付周期延长、供应链中断

- 订单、需求、营收、利润或投资计划变化

* 供应链转移、国产替代、业务调整等应对措施

需注意：一般经营数据只有在与冲击、影响或风险暴露存在明确联系时才视为相关。

**C — Industry Dependency Knowledge**

描述半导体产业的关键依赖关系和结构性脆弱性的知识，包括：

- 上下游企业、产品及供应关系

* 制造工艺与关键设备、材料之间的依赖

- EDA、IP、晶圆制造、封装测试等产业链依赖

* 供应商集中度、市场集中度及产能地域分布

- 技术替代难度、供应商切换成本

* 关键产能、基础设施或资源约束

- 产业链中的单点依赖与潜在瓶颈

**即使文本没有直接提到外部冲击，只要揭示了有意义的产业依赖、约束或脆弱性，也应优先保留。**

**D — Supporting Industry & Technology Knowledge**

有助于解释行业运行逻辑或冲击传导机制的背景知识，例如：

- 先进制程与成熟制程的技术差异

* 半导体制造的核心工艺步骤

- 关键设备或材料的技术作用

* 产品类别及应用市场差异

- 产能形成、工艺替代、供应切换的技术限制

这类知识仅在能够帮助解释产业依赖、冲击暴露、影响机制或业务后果时保留。

单纯的技术科普、产品参数或一般性行业介绍，不自动视为高相关知识。

**E — Irrelevant / Administrative Content**

与目标本体无明显关系的内容，包括但不限于：

- 公司历史、一般性宣传介绍

* 董事及管理层履历

- 企业文化、普通行政管理制度

* 与冲击无关的通用财务报表和会计说明

- 无关 ESG、社会责任或公司治理内容

* 重复页眉、页脚、目录及 OCR 噪声

- 不涉及关键产业约束的泛泛技术描述

不得仅因内容来自公司年报或技术报告就默认保留。

**4. Relevance Scoring**

为每个文本块提供 0–5 的相关性评分：

Score

Interpretation

5

直接描述明确的冲击、影响或关键传导机制

4

重要的产业依赖、结构性脆弱性或关键约束

3

与冲击分析存在明确联系的产业或技术背景

2

可能相关，但需要额外上下文或人工复核

1

关联极弱，主要是一般性背景

0

明确无关或无有效知识

**2. 无关内容过滤**

请删除与上述目标缺乏实质关联的内容，包括：

- 公司宣传、历史沿革、企业文化及一般性组织介绍。

* 董事会、管理人员履历、薪酬和常规治理信息。

- 与冲击分析无关的普通财务报表、会计政策及审计说明。

* 无关的社会责任、员工福利及 ESG 描述。

- 不涉及关键依赖、技术瓶颈或风险影响的常规产品宣传和技术科普。

* 重复的标题、目录、页眉页脚、免责声明及 OCR 噪声。

- 缺乏具体事实的空泛表述和重复性内容。

**不要仅因文本出现“芯片”“半导体”“风险”“供应链”等关键词就保留，必须具有实际分析价值。**

**3. 处理原则**

1. **按信息内容过滤，而不是按章节整体删除。** 一个章节中如果只有部分段落相关，应仅保留相关段落。

2) **优先保留原始事实和细节。** 不得因为精简而删除重要的企业名称、技术名称、设备、材料、时间、地点、数量、比例、金额及条件约束。

3. **保留产业依赖知识。** 对供应关系、技术依赖、设备约束、材料瓶颈、产能集中度等内容，即使未直接涉及冲击事件，也应保留。

4) **尽量保持原文。** 不进行概括性总结，不自行推导因果关系，不添加原文没有的信息。仅允许删除无关文字，以及修复明显的 OCR 格式错误。

5. **保留必要上下文。** 如果某段相关知识依赖标题、前置定义或解释性语句才能理解，应一并保留，避免出现缺少主语或对象的孤立片段。

6) **保留原始 Markdown 结构。** 尽可能维持有效的标题层级、段落、列表和表格。对表格可以删除无关行列，但不能破坏数据含义。

7. **保留事实与不确定性的区别。** 原文中的“可能”“预计”“假设”“已经发生”等表述不得随意修改。

8) **避免过度过滤。** 对于可能支持产业冲击分析的关键技术、供应链和行业结构性知识，应倾向于保留。

9. **不执行下游任务。** 不生成知识图谱、实体关系三元组、Ontology Schema、知识摘要或评价报告。

**4. Output Requirements**

直接输出过滤后的 Markdown 文档，要求：

- 仅包含筛选后保留的有效原文内容。

* 保持合理的 Markdown 标题与内容结构。

- 不增加原文未包含的分析、总结、解释或推断。

* 不输出 JSON。

- 如果整份文档没有任何符合条件的有效知识，则无需再维护这个md
````

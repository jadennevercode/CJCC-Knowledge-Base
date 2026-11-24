## Document Metadata

- Document ID: 30dc3314bd1d70dfb1763ad5521dfed470ece60b
- Document Title: Overview of new technologies applied to BiCS FLASH™ generation 8 | KIOXIA - Japan (English)
- Document Type: HTML
- Issuing Organization: Kioxia Corporation
- Publication Date: 2024-03-28
- Reporting Period: null
- Source File: [Scfb99794d120_kioxia.com_topics-66.html](https://github.com/jadennevercode/CJCC-Knowledge-Base/blob/564ab11aa9785e569e3853c8a4d7ce86f88e7535/materials/%E5%9F%BA%E7%A1%80%EF%BC%9A%E8%A1%8C%E4%B8%9A%E6%9C%AF%E8%AF%AD%E4%B8%8E%E6%8C%87%E6%A0%87/Scfb99794d120_kioxia.com_topics-66.html)

## Structured Content

> 原文件：[Scfb99794d120_kioxia.com_topics-66.html](https://github.com/jadennevercode/CJCC-Knowledge-Base/blob/564ab11aa9785e569e3853c8a4d7ce86f88e7535/materials/%E5%9F%BA%E7%A1%80%EF%BC%9A%E8%A1%8C%E4%B8%9A%E6%9C%AF%E8%AF%AD%E4%B8%8E%E6%8C%87%E6%A0%87/Scfb99794d120_kioxia.com_topics-66.html)
> 转换方式：HTML DOM → Markdown

# Overview of new technologies applied to BiCS FLASH™ generation 8

March 28, 2024

- [Advanced Memory Development Center](https://www.kioxia.com/en-jp/rd/technology/topics.html?sumtag=amdc)

- [3D flash memory (BiCS FLASH™)](https://www.kioxia.com/en-jp/rd/technology/topics.html?sumtag=bics-flash)

BiCS FLASH™ generation 8 is our latest high performance and high memory density 3D flash memory. Data are transferred to outside with 3.2Gbps speed, while data are read and programmed inside with 40μs time and 205MB/s throughput, respectively. With 218 world-lines stacked, the memory density of the 1Tb TLC (Triple Level Cell) product is well-scaled to 18.3Gb/mm², which is the world’s highest in the 2xx (about 218-236) word-line stacked technology node. In order to enhance performance and the memory density, we applied the two new technologies, CBA (CMOS directly Bonded to Array) and OPS (On Pitch SGD), to BiCS FLASH™ generation 8 (Figure 1). The following is a brief introduction of the two technologies.

![](https://www.kioxia.com/content/dam/kioxia/en-jp/rd/technology/topics/img/topics-66_img_001_en.png)

Fig.1 scanning electron microscopy image of BiCS FLASH™ generation 8[2] ©IEEE 2023

BiCS FLASH™ consists of the two components: the memory cell array where data are stored, and CMOS circuits which control the memory cell array. In the past technology node, CMOS circuits and the memory cell array are fabricated on a single wafer. Thus, applicable process conditions are limited, because favorable process conditions are different between the two. To address this issue, we developed CBA technology, where the two wafers are processed separately for CMOS circuits and the memory cell array, and are bonded afterwards. Since process conditions are optimized independently for CMOS circuits and the memory cell array, performance enhancement is expected in CBA. For example, we applied high temperature process during the memory cell fabrication in BiCS FLASH™ generation 8, which was not applicable to the non-CBA-type because of the severe degradation of CMOS performance, and minimized the electrical disturbance among the neighboring memory cells (Figure 2).

![](https://www.kioxia.com/content/dam/kioxia/en-jp/rd/technology/topics/img/topics-66_img_002_en.png)

Fig.2 Figure of merit for electrical disturbance among the neighboring memory cells[2] ©IEEE 2023

Next, we will explain OPS. The memory cell to access is uniquely selected, with the combination of voltage applied to word-line, bit-line, and select-gate in BiCS FLASH™. The select-gate is shared among the four lines of memory strings, and each select-gate is electrically separated by an insulator. When we look at the configuration of the select-gate and the memory strings in the in-plane direction, the insulator separating the select-gate (the insulator slit) overlaps with the dummy memory strings which do not function as memory cells in the past technology node. On the other hand, in OPS, the insulator slit is placed between the electrically active memory strings, and the dummy memory strings are eliminated to increase the memory density (Figure 3).

By adopting newly developed CBA and OPS technologies, we successfully enhanced performance and the memory density up to the level mentioned above in BiCS FLASH™ generation 8.

![](https://www.kioxia.com/content/dam/kioxia/en-jp/rd/technology/topics/img/topics-66_img_003_en.png)

Fig.3 In-plane configuration of memory strings and the insulator slit[2] ©IEEE 2023

This achievement was presented at IEDM(International Electron Devices Meeting) 2023.

Reference
[1] M. Sako et al., “A 1Tb 3b/Cell 3D-Flash Memory of more than 17Gb/mm² bit density with 3.2Gbps interface and 205MB/s program throughput”, Proc. IEEE Symp. VLSI Technol., Jun. 2023, C2-1.
[2] S. Kobayashi et al., “High Performance 3D Flash Memory with 3.2Gbps Interface and 205MB/s Program Throughput based on CBA(CMOS Directly Bonded to Array) Technology”, IEEE International Electron Devices Meeting (IEDM), Dec. 2023, 35-2.

[All Topics](https://www.kioxia.com/en-jp/rd/technology/topics.html)

Related Links


![](https://www.kioxia.com/content/dam/kioxia/ja-jp/rd/glossary/img/glossary_link_002.png)

[Technical Glossary](https://www.kioxia.com/en-jp/rd/glossary.html)

A technical glossary that covers terms related to KIOXIA products and technologies, such as memory and SSDs. We explain that it can be used by engineers and researchers to the general public.

![](https://www.kioxia.com/content/dam/kioxia/ja-jp/rd/organization/img/organization_link_008.png)

[R&D Organization and Locations](https://www.kioxia.com/en-jp/rd/organization.html)

KIOXIA has established industry-leading R&D frameworks with “memory” technology. We use our various locations to conduct technological innovation while promoting open innovation.

## Share

- [![Line](https://www.kioxia.com/content/dam/limitedlibs/logo/icon_line.svg)](https://social-plugins.line.me/lineit/share?url={{PAGE_URL}})
- [![Facebook](https://www.kioxia.com/content/dam/limitedlibs/logo/icon_facebook.svg)](https://www.facebook.com/sharer/sharer.php?u={{PAGE_URL}})
- [![X](https://www.kioxia.com/content/dam/limitedlibs/logo/icon_x.svg)](https://twitter.com/share?text={{PAGE_TITLE}}&url={{PAGE_URL}}&hashtags=kioxia)
- [![Linkedin](https://www.kioxia.com/content/dam/limitedlibs/logo/icon_linkedin.svg)](https://www.linkedin.com/shareArticle?mini=true&url={{PAGE_URL}})

---

[What is the 3D flash memory “BiCS FLASH™”?](https://www.kioxia.com/en-jp/rd/technology/bics-flash.html)

[What is NAND Flash Memory?](https://www.kioxia.com/en-jp/rd/technology/nand-flash.html)

[What is Multi-level Cell Technology?](https://www.kioxia.com/en-jp/rd/technology/multi-level-cell.html)

[Technology Topics](https://www.kioxia.com/en-jp/rd/technology/topics.html)

[Technology Development History](https://www.kioxia.com/en-jp/rd/technology/history.html)

[Awards and Research papers](https://www.kioxia.com/en-jp/rd/technology/award-paper.html)

---

## Processing Notes

- HTML 快照没有原文页码。原文使用 “218 world-lines”，已按原文保留。

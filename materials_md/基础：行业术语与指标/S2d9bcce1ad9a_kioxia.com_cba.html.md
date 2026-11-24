> 原文件：[S2d9bcce1ad9a_kioxia.com_cba.html](https://github.com/jadennevercode/CJCC-Knowledge-Base/blob/564ab11aa9785e569e3853c8a4d7ce86f88e7535/materials/%E5%9F%BA%E7%A1%80%EF%BC%9A%E8%A1%8C%E4%B8%9A%E6%9C%AF%E8%AF%AD%E4%B8%8E%E6%8C%87%E6%A0%87/S2d9bcce1ad9a_kioxia.com_cba.html)
> 转换方式：HTML DOM → Markdown

# What is CMOS directly Bonded to Array (CBA) Technology? | KIOXIA - Japan (English)

Welcome to   
KIOXIA Corporation

Please select your location and preferred language where available.

Select location and language

Japan (日本語)
Japan (English)

China (简体中文)

Hong Kong (English)
Republic of Korea (한국어)
Taiwan (繁體中文)
Asia Pacific (English)

Brazil (Português)
Canada (English)
United States (English)
Americas (Español)

France (Français)
Germany (Deutsch)
Greece (Ελληνική)
Hungary (Magyar)
Italy (Italiano)
Netherlands (Nederlands)
Poland (Polski)
Portugal (Português)

Spain (Español)
Turkey (Türkçe)
Europe (English)

Middle East & Africa (English)

GO

Close×


# What is CMOS directly Bonded to Array (CBA) Technology?

3D flash memory is a semiconductor device indispensable for realizing various technologies that support modern society, such as the internet of things (IoT), artificial intelligence (AI), and big data. To enable these technologies, improvements in 3D flash memory performance—such as faster operation speeds and lower power consumption—are required. Furthermore, if these demands can be met at low cost and supplied worldwide affordably, 3D flash memory can be utilized in a wider range of fields. At KIOXIA, to meet these requirements, we have developed the CMOS directly Bonded to Array (CBA) technology and achieved mass production, which we will introduce here.

![](https://www.kioxia.com/content/dam/kioxia/en-jp/rd/img/rd_img_008_en.png)

## What is CBA Technology?

3D flash memory has a structure in which memory cells, traditionally formed in a two-dimensional layout, are stacked vertically.

Table 1 shows a comparison of the generational structures of KIOXIA’s 3D flash memory BiCS FLASH™. The structure of 3D flash memory is broadly divided into the memory cell array region (hereafter “cell array”), which stores information, and the CMOS circuit region (hereafter “CMOS”), which operates the cell array. Up to BiCS FLASH™ generation 5 (hereafter referred to as “BiCS FLASH™ gen.”), the CMOS Next to Array (CNA) structure was adopted. In the CNA structure, CMOS is formed beside the cell array, so the chip size is approximately the sum of the CMOS and cell array sizes. Also, since the cell array is formed after CMOS, the CMOS is exposed to high-temperature heat during cell array formation. This high temperature degrades CMOS characteristics, so the heat during cell array formation had to be limited to the minimum temperature that maintains cell characteristics.

One way to reduce the cost of 3D flash memory is to reduce chip size to obtain more chips from a 300 mm wafer. Therefore, BiCS FLASH™ gen. 6 introduced the CMOS Under Array (CUA) structure, where CMOS is formed beneath the cell array. The CUA structure allows chip size reduction by forming the cell array continuously on top of CMOS on a single Si wafer. However, like CNA, the temperature during CMOS and cell array formation is limited, creating a trade-off between improving cell and CMOS performance, making it difficult to achieve both simultaneously.

The proposed solution is the CBA structure. In the CBA structure, CMOS and the cell array are formed on separate Si wafers, each with copper (Cu) bonding pads formed on their surfaces. Then, as shown in Fig.1, the Si wafers are bonded together using a Cu direct bonding process, electrically connecting CMOS and the cell array via the Cu bonding pads to form the 3D flash memory. As a result, by stacking CMOS and the cell array, chip size is reduced while allowing optimal thermal processes for both CMOS and the cell array, enabling performance improvements.

Table 1 Comparison of the generational structures of BiCS FLASH™

![](https://www.kioxia.com/content/dam/kioxia/en-jp/rd/technology/cba/img/cba_img_001_en.png)

![](https://www.kioxia.com/content/dam/kioxia/en-jp/rd/technology/cba/img/cba_img_002_en.png)

Fig.1 CBA structure formation by Cu direct bonding process

Two key technologies enable the realization of the CBA structure.

First is the Cu bonding pad step height reduction technology. As mentioned, the CBA structure requires gapless bonding of both Cu bonding pads and SiO2 interlayer films using the Cu direct bonding process. Therefore, as shown in Fig.2(a), the step height between the Cu bonding pads and SiO2 interlayer films formed on the surfaces of the CMOS and cell array wafers must be suppressed to the nanometer level.

This extremely fine step height control is achieved by the chemical mechanical polishing (CMP) process. Polishing the surface of a 300 mm wafer by CMP to achieve a step height of a few nanometers is akin to controlling morphology with the precision of reducing a step to less than the thickness of a single sheet of copy paper inside the Tokyo Dome. After bonding the CMOS and cell array wafers with such nanometer-level surface step control face-to-face at the SiO2 interlayer film surfaces, annealing causes thermal expansion of Cu, resulting in metallic bonding between Cu pads and enabling electrical connection. When the step height is small, as in Fig.2(b), the Cu pads on the upper and lower sides connect without gaps. Conversely, if the step height is large, as in Fig.2(c), gaps form between the Cu pads, preventing electrical connection. Since millions of Cu bonding pads connect CMOS and the cell array, the CBA structure requires extremely high CMP process control.

![](https://www.kioxia.com/content/dam/kioxia/en-jp/rd/technology/cba/img/cba_img_003_en.png)

Fig.2 Surface step height control process

The second key technology is the alignment technology between the upper and lower wafers in the Cu direct bonding process. Fig.3 shows the sequence of the Cu direct bonding process. In this process, the surfaces of the CMOS wafer and the cell array wafer are faced together and gradually brought closer from the center to the outer edge of the wafer. To electrically connect CMOS and the cell array from the center to the outermost edge of a 300 mm wafer, wafer positioning must be controlled within a few hundred nanometers or less. Furthermore, as shown in Table 1, the cell array wafer contains numerous memory cells and word lines, resulting in very large and complex stresses. Consequently, as shown in Fig.3, the cell array wafer exhibits a complex warp shape resembling a potato chip.

This warped cell array wafer is bonded to the nearly flat CMOS wafer with a positional deviation of only a few hundred nanometers or less. This precision is comparable to repeatedly landing a golf ball hit 200 yards within just a few millimeters of the pin. This demonstrates the extremely high process control of the Cu direct bonding process in the CBA structure.

![](https://www.kioxia.com/content/dam/kioxia/en-jp/rd/technology/cba/img/cba_img_004_en.png)

Fig.3 Cu direct bonding process and bonding position control

## Production and Future Prospects of the CBA Structure

By achieving such highly advanced process control, the CBA structure was applied in the BiCS FLASH™ gen. 8 products. Fig.4 shows a top-view photo and cross-sectional SEM image of the chip, confirming that CMOS and the cell array are connected by numerous Cu bonding pads. By separately forming CMOS and the cell array and bonding them via Cu bonding pads, cell current improved by 35% compared to the previous generation, and interface speed reached 3.6 Gbps [1][2].

![](https://www.kioxia.com/content/dam/kioxia/en-jp/rd/technology/cba/img/cba_img_005_en.png)

Fig.4 Product with CBA structure (BiCS FLASH™ gen. 8)

Moreover, the CBA structure is highly effective in meeting diverse product demands for the future of 3D flash memory. Fig.5 shows the product image of future CBA structure post BiCS FLASH™ gen. 9. By combining CMOS with different performance levels and cell arrays with different capacities, it becomes possible to realize 3D flash memory that supports the evolution of IoT, AI, big data, and other technologies.

![](https://www.kioxia.com/content/dam/kioxia/en-jp/rd/technology/cba/img/cba_img_006_en.png)

Fig.5 Future CBA structure

Reference  
[1] M. Tagami, "CMOS Directly Bonded to Array (CBA) Technology for Future 3D Flash Memory," *in Proc. 2023 IEEE International Electron Device Meeting (IEDM)*.,19-5.  
[2] S. Kobayashi et al., "High Performance 3D Flash Memory with 3.2Gbps Interface and 205MB/s Program Throughput based on CBA (CMOS Directly Bonded to Array) Technology," *in Proc. 2023 IEEE International Electron Device Meeting (IEDM)*.,35-2.

Related Links


![](https://www.kioxia.com/content/dam/kioxia/en-jp/rd/technology/topics/img/topics_link_064_en.png)

[Development of CMOS Directly Bonded to Array(CBA) Technology for 3D Flash Memory](https://www.kioxia.com/en-jp/rd/technology/topics/topics-64.html)

CMOS directly bonded to array(CBA) technology with Cu direct bonding process has been developed and applied to BiCS FLASH™ generation 8 for performance improvement and cost reduction of 3D flash memory.

![](https://www.kioxia.com/content/dam/kioxia/shared/business/memory/bics/img/bics_link_009.png)

[KIOXIA BiCS FLASH™ generation 8 3D flash memory makes the most of CBA technology (Video, 3:22)

![A modal window will open.](https://www.kioxia.com/etc.clientlibs/kioxia-libs/clientlibs/kioxia/resources/component/icon_modal.svg)](https://www.youtube-nocookie.com/embed/Vc-wG55KAsw?enablejsapi=1&autoplay=0&mute=1)

Introducing the KIOXIA BiCS FLASH™ generation 8 3D flash memory, with CBA (CMOS directly Bonded to Array) technology, in this video.

![](https://www.kioxia.com/content/dam/kioxia/en-jp/business/topics/bics-cba-202407/img/bics-cba_link_002_en.jpg)

[High-density 3D flash memory using high-precision wafer bonding brings new value to storage](https://www.kioxia.com/en-jp/business/topics/bics-cba-202407.html)

## Share

- [![Line](https://www.kioxia.com/content/dam/limitedlibs/logo/icon_line.svg)](https://social-plugins.line.me/lineit/share?url={{PAGE_URL}})
- [![Facebook](https://www.kioxia.com/content/dam/limitedlibs/logo/icon_facebook.svg)](https://www.facebook.com/sharer/sharer.php?u={{PAGE_URL}})
- [![X](https://www.kioxia.com/content/dam/limitedlibs/logo/icon_x.svg)](https://twitter.com/share?text={{PAGE_TITLE}}&url={{PAGE_URL}}&hashtags=kioxia)
- [![Linkedin](https://www.kioxia.com/content/dam/limitedlibs/logo/icon_linkedin.svg)](https://www.linkedin.com/shareArticle?mini=true&url={{PAGE_URL}})

## Document Metadata

- Document ID: 5066dba27a9493167768688756586903abcf9a7e
- Document Title: Managed Flash Background Operations Series — Part 5: Understanding Logical Block Address to Physical Block Address Translation in NAND Flash Memory
- Document Type: PDF
- Issuing Organization: KIOXIA Corporation
- Publication Date: November 2023
- Reporting Period: null
- Source File: [Sc39f5191b7e1_kioxia.com_KIOXIA_Understanding_Logical_B.pdf](https://github.com/jadennevercode/CJCC-Knowledge-Base/blob/564ab11aa9785e569e3853c8a4d7ce86f88e7535/materials/%E5%9F%BA%E7%A1%80%EF%BC%9A%E8%A1%8C%E4%B8%9A%E6%9C%AF%E8%AF%AD%E4%B8%8E%E6%8C%87%E6%A0%87/Sc39f5191b7e1_kioxia.com_KIOXIA_Understanding_Logical_B.pdf)

## Structured Content

[Source Page: 1]

# Managed Flash Background Operations Series

## Part 5: Understanding Logical Block Address to Physical Block Address Translation in NAND Flash Memory

Technical Brief

NAND flash memory enables content mobility that is relied upon daily and is considered an effective way of scaling data storage capacity and performance, as long as the proper management is applied. Logical block address to physical block address translation provides a fundamental management operation that enables efficient data storage in e-MMC¹ and UFS² devices and is the focus of this technical brief. This brief also represents the final installment in the Managed Flash Background Operations series that has covered error correction coding, bad block management, wear leveling and garbage collection.

[Source Page: 3]

### Process 4: Data Access

Once a physical block address is determined, the e-MMC/UFS controller accesses the appropriate NAND flash memory cells to read or write the data. This operation involves activating the desired memory cells, applying voltage levels, and managing data movements within NAND flash memory to perform read or write operations.

## Effects of Logical Block Address to Physical Block Address Translation in e-MMC/UFS Devices

Logical block address to physical block address translation is a fundamental operation in e-MMC/UFS devices that enables efficient data storage and is necessary due to the inherent characteristics of the NAND flash memory architecture. For example, new data written to NAND flash memory requires erasing the old data first. By utilizing logical block address to physical block address translation, e-MMC/UFS devices can simply change the physical block address without having to erase the old data, which helps to improve NAND flash memory endurance. This type of address translation also helps manage NAND bad block counts and wear leveling.

When implementing logical block address to physical block address translation in e-MMC/UFS devices, some design challenges may become apparent, and include:

### Performance Impact

Logical block address to physical block address translation introduces overhead and latency that can negatively affect the performance of e-MMC/UFS devices. This occurs from the constant updating of metadata and frequent data movements that can result in increased access times and decreased overall performance. The additional operations required for this address translation can slow down write and read operations that can lead to reduced responsiveness and low throughput.

### Write Amplification

Logical block address to physical block address translation can contribute to write amplification, a phenomenon where the number of physical writes exceeds the number of logical writes (Figure 5). This occurs because the translation process often involves data movements and updates to metadata that lead to additional write operations. Higher write amplification reduces the lifespan of the e-MMC/UFS devices, as each NAND flash memory cell has specified endurance relating to program and erase cycles.

### Write Amplification Factor

WAF = Data written to NAND flash memory / Data written by the host.

Figure 5: WAF formula.

[Source Page: 4]

## FOOTNOTES

1 Embedded MultiMediaCard (e-MMC) is a specification developed by JEDEC® for mobile applications. The current release is v5.1, published in February 2015.

2 Universal Flash Storage (UFS) devices are based on the UFS specification, of which, the v4.0 specification is the current release issued by JEDEC and published in August 2022.

3 A managed flash device combines raw NAND flash memory and an intelligent controller in one integrated package, enabling internal memory management.

## Document Metadata

- Document ID: 7077e3608ccf8c6dcb379ba2c85b9a3660e8191e
- Document Title: Managed Flash Background Operations Series — Part 1: Understanding ECC (Error Correction Code) in NAND Flash Memory
- Document Type: PDF
- Issuing Organization: KIOXIA Corporation
- Publication Date: May 2022
- Reporting Period: null
- Source File: [Sb60ebe684b8b_kioxia.com_KIOXIA_Understanding_ECC_Tech_.pdf](https://github.com/jadennevercode/CJCC-Knowledge-Base/blob/564ab11aa9785e569e3853c8a4d7ce86f88e7535/materials/%E5%9F%BA%E7%A1%80%EF%BC%9A%E8%A1%8C%E4%B8%9A%E6%9C%AF%E8%AF%AD%E4%B8%8E%E6%8C%87%E6%A0%87/Sb60ebe684b8b_kioxia.com_KIOXIA_Understanding_ECC_Tech_.pdf)

## Structured Content

[Source Page: 1]

# Managed Flash Background Operations Series

## Part 1: Understanding ECC (Error Correction Code) in NAND Flash Memory

NAND flash memory was invented by KIOXIA (formerly Toshiba Memory) in 1987 and is a very cost-effective way to scale data storage capacity and performance. As storage densities continue to increase, NAND management technologies have become increasingly more important. One of these critical management functions is Error Correction Code (ECC), and it is highlighted here as the first brief in a series of Managed Flash Background Operations.

## ECC Overview

Paramount to any application workload is the need to read or write back accurate and reliable data. As NAND flash memory cells wear down due to increasing write and erase cycles, the probability of erroneous bits being stored and/or read by the host System-On-Chip (SoC) will increase over this time frame. To ensure that stored data is accurate and reliable, both raw NAND flash memory (raw NAND) and managed NAND flash memory (managed flash) require ECC functionality to maintain data storage and recall accurate data.

Raw NAND devices do not have built-in controllers and are categorized by the number of levels that each flash memory cell supports (e.g., SLC, MLC, TLC or QLC¹). These devices are used for boot, OS code and user data storage, and support a range of capacities and endurance capabilities.

When raw NAND is deployed within devices, the host SoC manages ECC control. With raw NAND technologies continually evolving, maintaining ECC control over NAND generations can get quite complicated. They may even require more ECC functionality to a point where the host SoC may be unable to support these future technologies. The first was SLC NAND and it required only 1-bit of ECC Hamming codes² or Reed-Solomon codes³. As SLC dies shrank, 4-bit, 8-bit and higher levels of ECC was needed. When MLC and TLC NAND technologies evolved, ECC needs increased further and more complex algorithms were required, such as BCH⁴ codes and LDPC⁵ codes. With more demanding ECC methods, some lower end and/or older host SoCs are unable to support them.

Managed flash combines raw NAND and an intelligent controller in one integrated package, enabling memory management to be performed internally. ECC engine functionality can be offloaded from the host SoC to the flash device, and concerns associated with supporting a range of NAND flash memory generations, including future ones, are also eliminated.

[Source Page: 4]

## FOOTNOTES

1 Single-Level Cell (SLC) stores data 1-bit per cell; Multi-Level Cell (MLC) stores data 2-bits per cell; Triple-Level Cell (TLC) stores data 3-bits per cell; and Quad-Level Cell (QLC) stores data 4-bits per cell.

2 Hamming codes are a family of linear error-correcting codes that can detect 1-bit and 2-bit errors, or correct 1-bit errors without detecting uncorrected errors.

3 Reed-Solomon codes are a group of error-correcting codes that operate on a block of data which are treated as a set of finite-field elements called symbols, and where the codes are able to detect and correct multiple symbol errors.

4 BCH (Bose-Chaudhuri-Hocquenghem) codes are a class of cyclic error-correcting codes that are constructed using polynomials over a finite field.

5 LDPC (low-density parity-check) codes are linear error-correcting codes used to transmit data over noisy transmission channels.

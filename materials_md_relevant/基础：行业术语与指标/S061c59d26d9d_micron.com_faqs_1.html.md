## Document Metadata

- Document ID: 98207c1085aec5228bf978adb92dd11cfb6771c3
- Document Title: FAQs | Micron Technology Inc.
- Document Type: HTML
- Issuing Organization: null
- Publication Date: null
- Reporting Period: null
- Source File: [S061c59d26d9d_micron.com_faqs_1.html](https://github.com/jadennevercode/CJCC-Knowledge-Base/blob/564ab11aa9785e569e3853c8a4d7ce86f88e7535/materials/%E5%9F%BA%E7%A1%80%EF%BC%9A%E8%A1%8C%E4%B8%9A%E6%9C%AF%E8%AF%AD%E4%B8%8E%E6%8C%87%E6%A0%87/S061c59d26d9d_micron.com_faqs_1.html)

## Structured Content

# Frequently asked questions (FAQs)

## DRAM

### DDR4 SDRAM(11)

#### Can DDR4 operate at slower DDR3 speeds?

DDR4 is backward compatible as far back as DDR3-1333. For systems that do not need speed increases above DDR3-1333 and DDR3-1600, DDR4 can support these slower bandwidth requirements with substantially lower power requirements.

#### Where are DDR4 devices manufactured?

DDR4 is produced in Micron fabs around the world, including Virginia, Japan, and Taiwan.

#### Does DDR4 use the same signaling protocol as DDR3?

Not exactly.  DDR4 still uses VTT mid-point termination on the data bus for good signal quality, however it uses pseudo open-drain drivers for less switching current compared to full push-pull drivers.

#### Does DDR4 use the same power sources as DDR3?

No, DDR3 requires VDD and VDDQ equal to 1.5V, VREFCA equal to 0.5 x VDD, and VREFDQ equal to 0.5 x VDDQ, while DDR4 requires VDD and VDDQ equal to 1.2V, VREFCA equal to 0.5 x VDD, and VPP equal to 2.5V.

#### Are DDR3 and DDR4 pin-to-pin compatible to each other?

No, the DDR4 ballout is different from the DDR3 ballout. However, DDR4 uses the same package sizes and ball pitch as DDR3.

### LPDRAM (11)

#### The part I was using is obsolete and the replacement is a faster speed grade. Can I run the LPDRAM parts at a lower speed?

Yes. A LPDRAM part can be run at any speed equal to or slower than its rated speed grade.

## NAND flash

### eMMC (14)

#### How can I migrate from Micron e.MMC 4.4 to 4.41?

Micron has EOL’d its e.MMC 4.4 offering. Refer to your AE for support. A dedicated technical note “[TN-FC-08: Migrating from Micron v. 4.4 e.MMC to 4.41 e.MMC](https://www.micron.com/content/dam/micron/global/secure/products/technical-note/emmc/tnfc08-migrating-from-v4-4-emmc-to-v4-41.pdf)” is available for review.

### eUSB (7)

#### Is eU500 (eUSB 3.1) fully backward compatible with e230 (eUSB 2.0)?

Yes. Micron’s latest generation eU500 eUSB 3.1 products are backward compliant with the USB 2.0 protocol. The eU500 family also supports the same form factor, voltages and connector offerings as the previous generation e230. Please check the[part catalog](https://www.micron.com/products/obsolete) for Micron’s current eUSB offerings.

## Graphics memory

### GDDR5 (3)

#### Is GDDR5 a direct replacement for GDDR3?

No, GDDR5 is not a direct replacement for GDDR3 due to package size differences. GDDR3 has a 136-ball BGA package while GDDR5 has a 170-ball BGA package.

### GDDR5X (7)

#### Does GDDR5X replace GDDR5?

GDDR5X is not a direct replacement for GDDR5 due to package size differences. GDDR5 has a 170-ball, 0.8mm-pitch BGA package while GDDR5X has a 190-ball, 0.65mm-pitch package.

### GDDR6 (8)

#### Does GDDR6 replace GDDR5 or GDDR5X?

GDDR6 is not a direct replacement for GDDR5 nor GDDR5X due to package size differences. GDDR5 has a 170-ball, 0.8mm-pitch BGA package, GDDR5X has a 190-ball, 0.65-mm pitch BGA package and GDDR6 has a 180-ball, 0.75mm-pitch BGA package.

## Hybrid memory cube

### Why is Micron discontinuing HMC?

Micron reviews product roadmaps on a continuous basis to ensure that our current portfolio addresses current and future market needs. Since the early introduction of HMC, additional/alternate high-performance memories have entered the market, and the volume projects that drove initial HMC success are reaching maturity.

### What will replace HMC high-end performance memory?

Micron will continue to develop and design memory for high-performance applications. GDDR has roadmap support and continues to grow in this space. Micron has also established an HBM development program.

### How do I order last-time buy quantities?

Please work with the appropriate sales team or distribution contact to ensure last-time buy quantities are communicated to Micron prior to the last-time buy date.

## ONFI

### Are your NAND parts ONFI-compliant?

All our 50-series NAND devices and beyond are ONFI-compliant.

### How will ONFI help speed time-to-market for NAND-based products?

ONFI improves time-to-market in two principal ways:

1. It simplifies the design of Flash controllers that support a range of components by improving uniformity in the behavior of the interface to the NAND components.

2. It reduces the design time of Flash components in end-use applications and enables the use of a new generation of NAND components without design or firmware changes.

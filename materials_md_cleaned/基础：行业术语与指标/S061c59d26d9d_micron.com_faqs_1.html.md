## Document Metadata

- Document ID: 98207c1085aec5228bf978adb92dd11cfb6771c3
- Document Title: FAQs | Micron Technology Inc.
- Document Type: HTML
- Issuing Organization: null
- Publication Date: null
- Reporting Period: null
- Source File: [S061c59d26d9d_micron.com_faqs_1.html](https://github.com/jadennevercode/CJCC-Knowledge-Base/blob/564ab11aa9785e569e3853c8a4d7ce86f88e7535/materials/%E5%9F%BA%E7%A1%80%EF%BC%9A%E8%A1%8C%E4%B8%9A%E6%9C%AF%E8%AF%AD%E4%B8%8E%E6%8C%87%E6%A0%87/S061c59d26d9d_micron.com_faqs_1.html)

## Structured Content

1. [Home](https://www.micron.com/)
2. [Sales and support](https://www.micron.com/sales-support)
3. [Sales support](https://www.micron.com/sales-support/sales)
4. FAQs

Sales & support

# Frequently asked questions (FAQs)

![image of a laptop keyboard](https://www.micron.com/content/dam/micron/connectedassets/micron/global/banner-tertiary/segments-tertiary/personal-computing-tertiary/personal-computing-adobestock-438243864-tertiary.jpg)

## Products

## DRAM

### DDR4 SDRAM(11)

#### What newer power saving features does DDR4 provide compared to DDR3?

DDR4 added several new power saving features over DDR3, including:

1. Lower power pseudo-open drain drivers for the DQ pins

2. Optional ODT Input Buffer Disable Mode For Power-Down feature

3. Optional Maximum Power Saving Mode feature

4. Optional Command Address Latency (CAL)

#### Can DDR4 operate at slower DDR3 speeds?

DDR4 is backward compatible as far back as DDR3-1333. For systems that do not need speed increases above DDR3-1333 and DDR3-1600, DDR4 can support these slower bandwidth requirements with substantially lower power requirements.

#### Where are DDR4 devices manufactured?

DDR4 is produced in Micron fabs around the world, including Virginia, Japan, and Taiwan.

#### Are there any features on DDR3 that have been eliminated by DDR4?

Not really; however, DDR4 does not require an external VREFDQ, but it does provide an internally generated VREFDQ that requires calibration by the DRAM controller.

#### Does DDR4 use the same signaling protocol as DDR3?

Not exactly.  DDR4 still uses VTT mid-point termination on the data bus for good signal quality, however it uses pseudo open-drain drivers for less switching current compared to full push-pull drivers.

#### Does DDR4 use the same power sources as DDR3?

No, DDR3 requires VDD and VDDQ equal to 1.5V, VREFCA equal to 0.5 x VDD, and VREFDQ equal to 0.5 x VDDQ, while DDR4 requires VDD and VDDQ equal to 1.2V, VREFCA equal to 0.5 x VDD, and VPP equal to 2.5V.

#### What is DDR4’s VPP supply, and why does DDR4 have it?

The VPP supply replaces the internal word-line charge pumps that were present in earlier versions of DDR SDRAM including DDR3. Providing this voltage externally allows DDR4 to operate at a lower voltage level in a more cost-effective manner rather than providing the internal charge pumps.

#### Are DDR3 and DDR4 pin-to-pin compatible to each other?

No, the DDR4 ballout is different from the DDR3 ballout. However, DDR4 uses the same package sizes and ball pitch as DDR3.

#### DDR4 doubled the data rate of DDR3—did the prefetch also double from 8n to 16n?

No, DDR4 kept the 8n-bit prefetch used by DDR3; thus, BL8 is still supported.

#### Did DDR4 finally add boundary-scan or JTAG support?

DDR4 now has a Connectivity test mode to simplify testing with a boundary scan enabled controller. Designed to work with a boundary scan device, CT mode is supported in all Micron ×4, ×8, and ×16 devices (Though JEDEC requires only for x16). CT model allows a boundary scan device to load and read a pattern from a DDR4 in CT mode. DDR4 does not directly support IEEE 1149.1.

#### Does DDR4 support DLL Disable Mode or DLL-off Mode for slower clock rates?

Yes, DDR4 supports DLL-off Mode similar to DLL Disable Mode in DDR3, up to 125 MHz

### DDR3 SDRAM(15)

#### Are the DDR3 voltages backward compatible?

Yes, all of our 1.35V parts are backward compatible with 1.5V.

#### Can I run Micron’s DDR3 memory at clock speeds slower than 300 MHz?

Yes. Micron supports the optional feature to disable the DLL using the Mode Register, called DLL Disable Mode. This feature allows the DRAM to operate at frequencies slower than 125 MHz, however the timing still must satisfy the refresh interval. When operating in DLL Disable Mode, special conditions apply - refer to the device data sheets for details and restrictions.

#### How do I determine my CAS WRITE latency (CWL)?

In DDR3, only one CWL is valid for a given clock frequency range. - tCKavg = 2.5ns to <3.3ns, CWL = 5 - tCKavg = 1.875ns to <2.5ns, CWL = 6 - tCKavg = 1.5ns to <1.875ns, CWL = 7 - tCKavg = 1.25ns to <1.5ns, CWL = 8

#### What component densities are available?

Micron supports 1Gb, 2Gb, 4Gb, and 8Gb densities.

#### What is burst chop?

Due to use of the 8n-prefetch architecture in DDR3, a true burst length of 4 (BL4) was not possible. Burst chop mode became available in DDR3 to help mitigate this, and is also available in newer SDRAMs. Using Burst Chop in DDR3 the last 4 bits of the burst are essentially masked. Timing in Burst Chop 4 (BC4) cannot be treated like a true BL4. For READ-to-WRITE, select WRITE-to-READ, and select WRITE-to-PRECHARGE transitions, the system can achieve clock savings in the BC4 mode. While doing READ-to-READ or WRITE-to-WRITE transitions, timing must be treated like BL8; no clock savings will be realized.  DDR3 supports only either BC4 or BL8, although there is also an on-the-fly (OTF) option to switch between them via address pin A12.  Refer to the device data sheets for more details.

#### What is Dynamic ODT?

Dynamic ODT (Rtt\_WR) enables the DRAM to change termination values during a WRITE without having to perform a MODE REGISTER SET command. When Rtt\_Wr and Rtt\_Nom are both enabled, the DRAM will change termination values from Rtt\_Nom to Rtt\_Wr at the beginning of the WRITE burst. Once the burst is complete, the termination will be changed back to the Rtt\_Nom value. Rtt\_Wr can be used independently of Rtt\_Nom, but termination will be on WRITEs only.

#### What is the difference between the ZQCL and ZQCS commands?

ZQCL stands for ZQ calibration long. This command must be issued during the power-up and initialization sequence and requires 512 clocks to complete. After power-up and initialization, the command can be issued any time the DRAM is idle. These subsequent commands only require 246 clocks. This command is used when there is more impedance error correction required than a ZQCS can provide. ZQCS stands for ZQ calibration short. This command can be performed any time the DRAM is idle. One ZQCS can correct a minimum of 0.5 percent impedance error and requires 64 clocks.

#### What is the "MPR"?

MPR is a multi-purpose register. It is a specialized register designed to allow predefined data to be read out of the DRAM. Data is one bit wide and is output on a prime DQ. For Micron DDR3 parts, the prime DQs are DQ0 for x4/x8 and DQ0/DQ8 for x16. Two locations in the MPR are defined. One allows the readout of predefined data burst—in this case, 01010101. The other location is used to output the refresh trip points from the on-die thermal sensor.

#### What is the operating voltage?

DDR3 operates at Vdd = VddQ = 1.5V ±0.075V. DDR3L operates at Vdd = VddQ = 1.35V (1.283–1.45V)

#### What is the output driver impedance for DDR3?

The default output driver impedance for DDR3 is 34 ohms. The impedance is based on calibration to the external 240 ohm resistor, RZQ.

#### What is the RESET# pin used for?

RESET# is the master reset for the DRAM. It is an active LOW, asynchronous input. When the RESET# is asserted, the DRAM outputs are disabled and ODT will turn off (High-Z). The DRAM counters, registers, and data will be unknown. A RESET must be performed as part of the power-up and initialization sequence. During this sequence, the RESET# must remain LOW for a minimum of 200µs. After power-up and initialization, RESET# may be asserted at any time. Once asserted, it must stay LOW for a minimum of 100ns and a full initialization of the part must be performed afterward.

#### What is "write leveling"?

For improved signaling, DDR3 modules have adopted fly-by technology for the commands, addresses, control signals, and clocks. Due to signal routing, this technology has an inherent timing skew between the clock and DQ bus at the DRAM. Write leveling is a way for the system controller to de-skew the DQ strobe (DQS) to clock relationship at the DRAM. A simple feedback feature provided by the DRAM allows the controller to detect the amount of skew and adjust accordingly.

#### What is "ZQ Calibration"?

The ZQ calibration command can calibrate the DRAM's output drivers (Ron) and ODT values (Rtt) over process, voltage, and temperature when a dedicated 240 ohm (±1 percent) resistor is connected from the DRAM's ZQ pin to ground. In DDR3, two different calibration commands exist: ZQ calibration long (ZQCL) and ZQ calibration short (ZQCS). ZQCL is normally used during power-up initialization and reset sequences, but may be issued at any time by the controller, depending on the system environment. ZQCS is used to perform periodic calibrations to account for small voltage and temperature variations; it requires a smaller timing window to complete.

#### What termination values does DDR3 offer?

DDR3 supports RTT\_nom values of 120, 60, 40, 30, and 20 ohms. Dynamic ODT values (RTT\_WR) are 120 and 60 ohms.

#### Will Micron support an extended temperature range for DDR3?

Yes. Micron DDR3 parts will support a Tcase of 0°C to 95°C.

### DDR2 SDRAM (9)

#### Can DDR2-1066 be used with two slots?

Using DDR2-1066 with two slots is unrealistic; simulations have not shown acceptable margins.

#### How does on-die termination (ODT) affect power consumption?

On-die termination (ODT) power is very application-dependent. ODT is also variable, depending on the setting in the EMR of the DRAM. Use the DDR2 power calculator to determine the values.  
  
In a point-to-point system, ODT would only be active on WRITE cycles, and would not consume power during idle and READ cycles. On-board termination would consume power in these instances. ODT power should be about 2–3 percent of the total DDR2 DRAM power in a typical application.

#### How much power does the Vref power pin draw?

The Vref pin does not draw any power, only leakage current, which is less than 5µA.

#### Is VREF allowed to float during self refresh mode?

No, it must be maintained at VDDQ/2.

#### Should DDR2 SDRAM always have ODT turned on?

It’s not recommended, as the SDRAM reads will lose voltage margin; but technically, it is allowed.

#### Can the DLL be disabled in DDR2? Can DDR2 be put into DLL Disable mode similar to DDR3?

Although in some cases the DRAM may work with the DLL off, this mode of operation is not documented nor supported by JEDEC. Therefore, each DRAM design may behave differently when configured to run with the DLL disabled. Micron does not support or guarantee operation with the DLL disabled. Running the DRAM with the DLL disabled may cause the device to malfunction and/or violate some DRAM output timing specifications.

#### What is the DDR2 RDQS pin for?

The sole purpose of RDQS is to support the use of a x8-based RDIMM in a x4-based RDIMM system. The RDQS pin enables a x8 DDR2 SDRAM to emulate two x4s.

#### What is the maximum clock rate for DDR2 when it’s used with a single-ended DQS?

The answer depends on the design implementation. Data setup and hold timing should be designed to have 150ps or more of margin.  There are Single-Ended DQS Slew Rate derating tables in the data sheet that must be used in evaluating the timing. It is recommended to fully analyze the timing in calculations, as well as using signal integrity simulations and hardware characterization.

#### Is it OK to run clock frequencies lower than indicated in the DDR2 data sheet?

For a READ operation, the DRAM edge-aligns the strobe(s) with the data. Most controllers sense the strobe to determine where the data window is positioned. This fine strobe/data alignment requires that each DRAM have an internal DLL. The DLL is tuned to operate for a finite frequency range, which is identified in each DRAM data sheet. Running the DRAM outside these specified limits may cause the DLL to become unpredictable. The DRAM is tested to operate within the data sheet limits. Micron does not suggest or guarantee DRAM operation outside these predefined limits.

### DDR SDRAM (10)

#### Can a -6 or -6T speed grade DDR part be substituted with a faster -5B speed grade part without encountering problems due to the 2.6V operation? Can the customer run the part at slower speeds?

Yes, all speed grades are backward-compatible. So, -5B can run at -6T timing and -6T voltage levels (2.5V). At DDR400 speeds, Micron parts require (in compliance with JEDEC standard) Vdd = VddQ = 2.6V ±0.1V. At slower speed grades (DDR333 through DDR200), the Micron parts are backward compatible, only requiring Vdd = VddQ = 2.5V ±0.2V.

#### Do I need a separate voltage regulator to supply Vref power?

There is no requirement to use a separate regulator to supply Vref for Micron's DDR SDRAM. However, because Vref is the reference voltage for all single-ended inputs, any noise due to sharing the regulator with other I.C.s on a board or by using a voltage divider from the VDD supply, will directly impact the noise margin on those inputs. Many multi-drop systems already have a designated voltage regulator for DDR memory. Other systems that incorporate point-to-point memory typically use a simple voltage divider resistor network between VDD and VSS.  System designers should evaluate the priorities and trade-offs for each particular system and use the power supply scheme that is optimal for the system.

#### How long does Micron plan to support 3.3V SDRAM?

Micron is supporting and plans to support SDR for several years. Contact your local Micron sales representative for more information.

#### How long does Micron plan to support DDR?

Micron is supporting and plans to support DDR for several years. Contact your local Micron sales representative for more information.

#### Is VREF required during self refresh? I would like to put DDR memory in self refresh mode and turn off power to the CPU (the system is battery-operated). Can I disable VREF and still have correct self refresh operation?

Yes. VREF is required during self refresh. All DDR components' on-chip address counters are still operational during self refresh mode, so VDD must be maintained within the stated data sheet limits. Again, VREF must not be disabled after the DDR memory is put into self refresh mode. Doing so could easily result in inadvertently exiting self refresh. You should understand that VREF draws almost no power; any current drawn by VREF is negligible when compared to VTT and the core VDD. DDR components typically use a differential pair common source amplifier as their SSTL\_2 input receiver. Because the VREF pin is used primarily as an input to this circuit, its current draw is low. It is so low, in fact, that the device’s input leakage current (~5µA) can be considered the maximum current requirement for the VREF pin. Typical VTT power is drawn from other places on the board and depends on the other components used on the module/system in addition to DRAM devices.

#### On DDR, what happens when DQS write postamble (tWPST) maximum specification is exceeded? What problems could this cause?

The tWPST maximum specification is not a device limit. The device will operate with a greater value for this parameter, but system performance (bus turnaround) will degrade accordingly.

#### On DRAM, can a READ or WRITE command be given instead of a refresh?

If all of the different row addresses are read or written within the refresh time (tREF), a refresh need not be performed. (The different row addresses are the same number of rows as the number of REFRESH cycles. For example, in the case of 8,192/64ms, the number of rows equal 8,192.) With DRAM, selecting row addresses causes the same action as a refresh, so a REFRESH command need not be executed.

#### On DRAM, can unused DQ (data) pins be left floating?

Micron recommends that unused data pins be tied HIGH or LOW. Because Micron uses CMOS technology in DRAM manufacturing, letting them float could leave the pins susceptible to noise and create a random internal input level. Unused pins can be connected to VDD or ground through resistors.

#### What is the difference between no connect (NC), no function (NF), and do not use (DNU) pins? How should external connections to them be handled?

An NC (no connect) pin indicates a device pin to which no internal connection is present or allowed. Micron recommends that no external connection be made to this pin. However, if a connection is inadvertently made, it will not affect device operation. Sometimes NC pins could be reserved for future use. Refer to the part’s data sheet to confirm whether the pin is reserved for future use. An NF (no function) pin indicates a device pin that is electrically connected to the device but for which the signal has no function in the device operation. Micron strongly recommends that no external connection be made to this pin. A DNU (do not use) pin indicates a device pin to which there may or may not be an internal connection but to which no external connections are allowed. Micron requires that no external connection be made to this pin. Refer to the part’s data sheet for more details.

#### What is the maximum junction temperature at which DDR SDRAM functionality is guaranteed?

Please refer to page 3 of Micron’s technical note on thermal applications: [TN-00-08](https://www.micron.com/content/dam/micron/global/secure/products/technical-note/dram/tn0008-thermal-apps.pdf). If functionality or operation is not a concern, refer to storage temperature specification limits on the part’s data sheet.

### SDRAM (3)

#### Can CKE be tied HIGH throughout SDRAM operation (initialization and normal operation)?

Yes, all speed grades are backward-compatible. So, -5B can run at -6T timing and -6T voltage levels (2.5V). At DDR400 speeds, Micron parts require (in compliance with JEDEC standard) Vdd = VddQ = 2.6V ±0.1V. At slower speed grades (DDR333 through DDR200), the Micron parts are backward compatible, only requiring Vdd = VddQ = 2.5V ±0.2V.

#### Can the SDRAM clock frequency be changed?

Micron SDR SDRAM data sheets require that the clock frequency be constant during access or precharge states. However, because there is no DLL in SDRAM, it may be possible to shift the clock frequency dynamically, though this is not recommended by Micron. If a design requires shifting frequency, lowering SDRAM frequency may be OK, even if you are not doing an LMR and CAS latency change. In case of increasing frequency, ensure tCK and CAS latency specifications are met. In either case, all other data sheet timing specifications must always be adhered to.

#### Is there a minimum clock frequency for SDR SDRAM?

Because SDR SDRAM does not have a DLL, there is no minimum clock frequency.  However, if the device is clocked at lower frequencies, it is still important to maintain a reasonably fast slew rate on the clock edges to avoid risk of setup and/or hold-time violations. Also, for operating frequencies of 45 MHz, tCKS = 3.0ns. For more information, see LVTTL Derating for SDRAM Slew Rate Violations ([TN-48-09](https://www.micron.com/content/dam/micron/global/secure/products/technical-note/dram/tn4809.pdf)).

### RLDRAM (6)

#### Are CK/CK# and DK/DK# true differential inputs?

Yes, the CK/CK# and DK/DK# input buffers are true differential inputs. Both sets of clocks need to meet the specifications that are defined in the Clock Input Operating Conditions tables in the RLDRAM data sheets.

#### Can I connect the “Do Not Use” (DNU) pins to ground (GND)?

Yes. However, when on-die termination (ODT) is enabled, the DNU pins will be connected to VTT. Connecting the DNU pins to GND under these circumstances will cause a substantially larger load on your VTT supply.

#### How is RLDRAM II memory similar to SRAM?

Simplified command set of only four commands and a Fast cycle time, as low as 7ns tRC

#### I’ve heard about the new multibank write feature on RLDRAM 3. What exactly is this feature?

Multibank write is a feature that allows for SRAM-like random read access time. Using this feature can reduce RLDRAM 3’s already low tRC (<10ns) by up to 75% during reads. Through the RLDRAM 3 mode register, you can choose to write to one, two, or four banks simultaneously. By storing identical data in multiple banks, the memory controller has the flexibility to determine which bank to read the data from in order to minimize tRC delay.

#### What new features does RLDRAM 3 add?

Multibank write that enables SRAM-like random read capabilities. MULTIBANK REFRESH makes managing refresh overhead more flexible than ever, allowing refresh of one to four banks simultaneously. RLDRAM3 also supports a mirror function to ease layout of clamshell designs.

#### Will I be able to leverage any existing DRAM technology to ease the adoption of RLDRAM 3 in my system?

Yes. Even though RLDRAM 3 is a new architecture, it leverages many features from both DDR3 and RLDRAM 2 to make adoption and integration as easy as possible. The command protocol, addressing, and strobing scheme are the same as RLDRAM 2, while the I/O, AC timing, and read training register very closely resemble those found in DDR3.

### LPDRAM (11)

#### Are Micron's LPDRAM products green/RoHS compliant?

Yes. Micron’s green engineering program is RoHS-compliant and conforms with most of the world’s emerging environmental standards, including those in Asia and Europe.

#### Are your LPDRAM parts JEDEC-compliant?

We design our parts to meet or exceed the JEDEC specification. As standards change, we will make the necessary changes to ensure our parts meet new specifications. Any changes made will be noted in a product change notice (PCN) and sent to our customers.

#### How does LPDDR4X differ from LPDDR4?

VDDQ is reduced from 1.1V to 0.6V in LPDDR4X for further power reduction from LPDDR4. Max data rate for LPDDR4X is the same with LPDDR4 as 4266Mbos/pin. Single ended CK/DQS features are supported with LPDDR4X.

#### How does LPDDR5 differ from LPDDR4X?

LPDDR5 achieves 6400Mbps max data rate per pin, which is 1.5x faster than LPDDR4. max data rate 4266Mbps, at the same time improving the energy efficiency (pJ/bit). Many power reduction features are introduced in LPDDR5. See the technical notes below.

[TN-62-02: LPDDR5 Interface](https://www.micron.com/content/dam/micron/global/secure/products/technical-note/dram/lpddr5/tn6202-lpddr5-interface.pdf): Description of LPDDR5 Interface, how it diffres from LPDDR4X  
Rev. A – 4/19

[TN-62-03: LPDDR5 Training](https://www.micron.com/content/dam/micron/global/secure/products/technical-note/dram/lpddr5/tn6203-lpddr5-training.pdf): General overview of LPDDR5 SDRAM Training  
Rev. A – 5/19

[TN-62-04: LPDDR5 Clocking](https://www.micron.com/content/dam/micron/global/secure/products/technical-note/dram/lpddr5/tn6204-lpddr5-clocking.pdf): Description of LPDDR5 clocking, including a brief comparison with LPDDR4.  
Rev. A – 5/19

[TN-62-06: LPDDR5 Architecture](https://www.micron.com/content/dam/micron/global/secure/products/technical-note/dram/lpddr5/tn6206-lpddr5-architecture.pdf): General overview of LPDDR5 Architecture  
Rev. A – 7/19

[TN-62-07: LPDDR5 ZQ Calibration](https://www.micron.com/content/dam/micron/global/secure/products/technical-note/dram/lpddr5/tn6207-lpddr5-zq-cal.pdf): General overview of LPDDR5 ZQ calibration  
Rev. A – 12/19

[TN-62-08: LPDDR5 NT ODT](https://www.micron.com/content/dam/micron/global/secure/products/technical-note/dram/lpddr5/tn6208-lpddr5-nt-odt.pdf): LPDDR5 NT ODT  
Rev. A – 7/19

#### What’s the difference between Mobile LPDRAM, Automotive LPDRAM, and Embedded LPDRAM?

There is no difference in a die. We opted to add the "Mobile”, “Automotive” and “Embedded" prefix to our LPDRAM product line to align with each market segment. Mobile is for portable devices such as smartphones and tablets. Automotive is for devices relating to motor vehicles. Embedded is devices for dedicated computer system designed for one or two specific functions, unlike the general-purpose computers. In embedded applications, the device is embedded as a part of a complete device system, for example, into a digital television, a camera, and a set top box, etc. Each market segment has different product requirements such as operating temperatures which is noted in the part number. Please refer to each datasheet for the actual operating temperature range.

Operating Temperatures  
Blank = Commercial temperature  
IT  = Industrial temperature  
AT = Automotive temperature  
WT = Wireless temperature  
XT = Wide temperature  
UT = Ultra temperature  
ET = Extreme temperature

#### Does Micron's LPDRAM cost more than standard DRAM?

It depends. Density plays a major role in price comparisons between LPDRAM and standard SDR/DDR. Also, since LPDRAM is offered in standard configurations of x16, x32 and x64, you may be able to reduce your overall BOM cost if your application currently uses two x16 components to support a x32 bus. You could use one x32 LPDRAM instead of two x16 standard DRAM. Contact your local rep for cost information.

#### How does LPDDR3 differ from DDR3L-RS?

LPDDR3 is optimized for battery life and portability. DDR3L-RS is a low IDD6 version of the DDR3L die and offers a balance in price versus performance, along with improved standby power.

#### The part I was using is obsolete and the replacement is a faster speed grade. Can I run the LPDRAM parts at a lower speed?

Yes. A LPDRAM part can be run at any speed equal to or slower than its rated speed grade.

#### What is LPDRAM?

Optimized for products where power consumption is a concern, our low-power LPDRAM devices combine leading-edge technologies and packaging options to meet space requirements and extend battery life. LPDRAM is available with DDR/SDR interface.

#### What is the life expectancy of Micron's LPDRAM products?

We're excited about this fast-growing market. We plan to manufacture LPDRAM for many years to come and plan to continue to shrink our designs to achieve higher densities.

#### What makes Micron's LPDRAM unique?

We offer a comprehensive LPDRAM product portfolio, with a wide range of densities and package options (including JEDEC-standard FBGA, xMCP, and package-on-package). With Micron's extensive LPDRAM experience, our worldwide technical support team can provide the expertise and assistance you need to get your designs to market faster.

## DRAM modules

### Can Vtt and Vref be supplied by the same supply in my system design?

With proper decoupling this can be an acceptable design. However, Micron recommends ensuring all supplies are separated. Vref tends to have more noise on it because it supplies signals that are regularly switching. A robust design would typically not connect these supplies due to the possibility of introducing this noise onto the Vtt plane which should be as stable as possible. Additionally, Vref requires much less current than Vtt.

### Is there a set of trace lengths and routing rules that are standard for use when designing a system that uses a specific module technology and form factor?

No. A robust memory subsystem design that includes the use of 1 or more memory modules must be simulated in order to determine the optimum trace lengths, terminations. However, our design guides such as [TN-47-01](https://www.micron.com/content/dam/micron/global/secure/products/technical-note/dram/tn-47-01.pdf) and [TN-41-08](https://www.micron.com/content/dam/micron/global/secure/products/technical-note/dram-modules/tn4108-ddr3-design-guide.pdf) have some best practices and design examples based on some typical system assumptions. This information is not meant to be the only way your system can be designed. It is a starting point and moreover an example of the steps used to determine the best design for your system.

### NVDIMM (8)

#### What is NVDIMM?

NVDIMM is a nonvolatile persistent memory solution that combines NAND flash, DRAM and an optional power source into a single memory subsystem. Micron’s NVDIMM is capable of delivering the performance levels of DRAM combined with the persistent reliability of NAND, ensuring data stored in-memory is protected against power loss.

#### How do NVDIMMs work?

NVDIMMs operate in the DRAM memory slots of servers to execute workloads at DRAM speeds. In the event of a power fail or system crash, an onboard controller safely transfers data stored in DRAM to the onboard nonvolatile memory, thereby preserving the data that would otherwise be lost. When the system stability is restored, the controller transfers the data from the NAND back to the DRAM, allowing the application to efficiently pick up where it left off.

#### What is persistent memory?

Persistent memory is a new addition to the memory/storage hierarchy that enables greater flexibility in data management by providing nonvolatile, low-latency memory closer to the processor. Essentially, persistent memory accelerates application performance by removing what otherwise are constricting I/O bottlenecks placed on the application by standard storage technologies. By placing nonvolatile memory on the DRAM bus, this architecture enables customers to significantly optimize data movement in order to deliver faster access to variables stored in DRAM.

With persistent memory, system architects are no longer forced to sacrifice latency and bandwidth when accessing critical data that must be preserved. Critical data can be stored close to the processor, dramatically cutting access times. Persistent memory delivers a unique balance of latency, bandwidth, capacity and cost, delivering ultra-fast DRAM-like access to critical data and enabling system designers to better manage overall costs.

#### What are the key use cases for NVDIMM?

Any application where performance depends on variables stored in nonvolatile media (HDD or SSD) can benefit from NVDIMMs (most applications can be accelerated). Persistent variables include metadata logs, checkpoint state, host write caches, write buffers, journals and general logs. Applications that can be accelerated by placing these variables in NVDIMM include 2-node, high-availability storage using RAID cards, SSD mapping, RAMDisk and write caching for SSDs.

#### What products are available today?

Micron will be offering three DDR4 NVDIMM products:

1. 8GB DDR4 NVDIMM with legacy firmware
2. 8GB DDR4 NVDIMM with JEDEC firmware
3. PowerGEM® ultracapacitor for 8GB NVDIMM

#### What is the difference between the legacy and JEDEC firmware?

Legacy firmware refers to the firmware features and controller register locations for features determined by AgigA Tech, Inc., for initial DDR4 NVDIMM designs. JEDEC has now standardized the NVDIMM firmware features, register locations and APIs so that one vendor’s NVDIMM can be compatible with any other vendor’s NVDIMM. All new Micron NVDIMM solutions will leverage the JEDEC firmware interface.

#### How will NVDIMMs be enabled? What platforms support NVDIMM?

Many motherboards, servers and storage appliances support NVDIMMs today. Many more will come to market in 2016. Contact your supplier for more details.

#### Are there software requirements for NVDIMM?

NVDIMMs leverage either block mode or direct access drivers. NVDIMMs used in conjunction with a block mode driver are compatible with OS and applications with little to no necessary software modifications. Additional performance capability can be tapped by leveraging an NVDIMM with a direct mapped driver, but OS and application software will likely need some modification. Micron is currently working with major OEMs and software companies to incorporate NVDIMM hardware, driver and software support into their mainstream products.

## NAND flash

### eMMC (14)

#### What is e.MMC?

Embedded MultiMediaCard (e.MMC) is a NAND Flash-based memory solution defined by JEDEC that comes in a small BGA package. JEDEC defines both the hardware and software, enabling easy customer design-in and the ability to multisource.

#### What are the benefits of e.MMC?

e.MMC is a fully managed solution (all media management and ECC are handled internally), making NAND technology transitions invisible to the host and providing customers with the ability to reduce their time-to-market and to sustain products longer and more easily.

#### What does the term "broad market" signify?

Our embedded market e.MMC products are divided into two families: automotive and broad market. This is due to the unique requirements that are required in the automotive market; thus, there is a separate product line supported by Micron’s automotive team. Broad market covers all other market segments such as consumer, gaming, server, networking, industrial, medical, military, etc. Broad market e.MMC includes two sub-families: WT with commercial temperature grade and IT with an extended temperature range.

#### How can I order samples?

You can order samples through the [Micron Sample Center](https://www.samplecomponents.com/scripts/samplecenter.dll?micron).

#### Is it necessary to refer to the JEDEC specification as well as to Micron’s data sheet?

Yes, the JEDEC specification has to be read in conjunction with the data sheet. Micron e.MMC complies with the JEDEC standard; hence, Micron's data sheets provide information that is specific only to Micron’s e.MMC devices.

#### Are simulation models available?

Yes, IBIS models are available for WT and IT products (JEDEC 153-/169-ball and 100-ball)

#### What is the e.MMC offering for industrial applications?

Micron is offering an extensive number of solutions for industrial customers, such as five densities and JEDEC-standard BGA 153-/169-ball and custom 100-ball packaging. All of these products will operate in the extended temperature range of -40° to 85°C.

#### What are the advantages of 100-ball IT e.MMC?

Micron’s 100-ball e.MMC BGA package features a 1.0mm ball pitch for board routing simplification (saving PCB costs) and improved board-level reliability (temp cycling). This solution is particularly attractive to automotive, industrial, and networking market segments. See the following table for additional benefits.

| Features of 100-ball e.MMC | Benefits |
| --- | --- |
| Large 1.0mm ball pitch | Allows for low-cost PCB trace/space designs<br>Simplifies PCB routing<br>Enables a reduction in the number of PCB layers<br>Reduces costs via a lower drill size<br>Lower DAR (drill aspect ratio) for better PCB yields<br>Allows for wider traces for better thermal dissipation |
| Large 0.45mm nominal ball diameter | Provides high PCB board-level reliability<br>Improves surface-mount yields (vs. smaller ball packages)<br>Provides better thermal dissipation |
| Low ball count (compared to 153-ball e.MMC JEDEC-standard) | Allows for easier, low-cost PCB routing<br>Reduces package and PCB costs |
| 100-ball pattern contains 12 mechanical support balls (3 in each corner) | Provides excellent PCB board-level reliability<br>Allows for flexible “large package size” variations |
| Flexible ball-out design | Allows for future e.MMC feature upgrades and next-generation technology |


#### How can I migrate from Micron e.MMC 4.4 to 4.41?

Micron has EOL’d its e.MMC 4.4 offering. Refer to your AE for support. A dedicated technical note “[TN-FC-08: Migrating from Micron v. 4.4 e.MMC to 4.41 e.MMC](https://www.micron.com/content/dam/micron/global/secure/products/technical-note/emmc/tnfc08-migrating-from-v4-4-emmc-to-v4-41.pdf)” is available for review.

#### Is it possible to perform a system boot from e.MMC?

Yes, e.MMC provides two boot partitions to provide fast access to boot code for improved system boot time. Booting from boot partitions can provide access to stored data in ~50ms, whereas booting from the user area can take hundreds of milliseconds. However, in order to utilize the boot partitions, the chipset must be able to support booting from the boot partition. Check with your chipset vendor to understand if booting from the e.MMC boot partitions is supported.

#### Does Micron e.MMC support power-loss protection?

Yes, ESG e.MMC devices support static data protection. Devices are shipped from Micron factories as COMBO with a configuration optimized for best write performance. Customers can reconfigure the devices to protect static (previously written) data if there is power loss during a write operation.

#### What are the enhanced technology features mentioned in JEDEC specification, and what are the benefits?

Yes, ESG e.MMC devices support static data protection. Devices are shipped from Micron factories as COMBO with a configuration optimized for best write performance. Customers can reconfigure the devices to protect static (previously written) data if there is power loss during a write operation.

#### Can I set up partitions within e.MMC to suit different usage models?

The e.MMC specification allows customers to configure the user data area into a maximum of four separate partitions that can each be configured as MLC (default) or enhanced mode (pSLC). Enhanced mode provides better reliability in exchange for twice the space as MLC.

For more information refer to "[TN-FC-40: Embedded e.MMC Configuration](https://www.micron.com/content/dam/micron/global/secure/products/technical-note/emmc/tnfc40-emmc-configuration.pdf)"

#### What is the required software support for e.MMC?

e.MMC drivers are generally available on the market due to the fact that it is an industry-standard product.

### eUSB (7)

#### What is eUSB?

The embedded universal serial bus (eUSB) is a NAND flash-based memory solution that is compliant with the USB industry standards. USB is a widely adopted interface used across multiple platforms and operating systems, providing a low-cost, efficient data transfer solution for current applications and beyond.

#### What are the benefits of eUSB?

eUSB is a fully managed solution that utilizes NAND memory and, through an onboard controller, internally handles all media management and ECC control. The eUSB provides customers with a complete storage solution that easily integrates into their system and, in turn, fuels a reduced time to market.

Using native SLC NAND memory, combined with a rich set of management features such as global wear leveling and dynamic data refresh, eUSB offers a superior combination of performance and reliability.

#### How does the eUSB attach to my system board?

The eUSB device has a 10-pin (2x5) USB female connector compatible with the industry-standard 10-pin connector found on most motherboards. A mounting hole (connected directly to internal ground) is also provided on the PCB to ensure a stable connection to the system board.  Additional holes in the PC board, utilized during manufacturing for de-paneling, can also be used as additional mounting locations if required.

#### Can I use the eUSB as a boot device?

Yes. Micron’s eUSB can be used as the operating system boot and main storage device. However, the application’s BIOS must support the boot mode feature, which should not be a concern for most systems that were manufactured in the last five years and support USB 2.0. In either the main storage or boot mode, the eUSB should be recognized as a fixed hard drive in the system.

#### Does Micron offer the eUSB with a 3.3V option?

Yes. Please check the [part catalog](https://www.micron.com/products/obsolete)for Micron’s current eUSB offerings.

#### Does Micron provide a way for me to determine the useful life remaining on the device?

Our latest generation eU500, eUSB 3.1 products do provide a method to extract relevant lifetime data through the use of SMART commands. However, previous generations of eUSB products do not support a runtime method to collect lifetime data.

#### Is eU500 (eUSB 3.1) fully backward compatible with e230 (eUSB 2.0)?

Yes. Micron’s latest generation eU500 eUSB 3.1 products are backward compliant with the USB 2.0 protocol. The eU500 family also supports the same form factor, voltages and connector offerings as the previous generation e230. Please check the[part catalog](https://www.micron.com/products/obsolete) for Micron’s current eUSB offerings.

### 3D NAND (4)

#### Why is 3D NAND necessary?

Planar NAND flash memory is nearing its practical scaling limits, which poses challenges for the memory industry.  Industry innovation requires state-of-the-art NAND technology that scales with higher densities and lower cost per bit. 3D NAND allows flash storage solutions to continue aligning with Moore’s Law, bringing significant improvements in density while lowering the cost of NAND flash.

#### What sets apart this 3D NAND from other offerings in the industry?

The 3D NAND technology developed by Intel and Micron offers significant improvements in density and cost, and it’s the first 3D NAND to use floating gate cells.  This 3D NAND enables flash devices with three times higher capacity than other planar NAND die in production, and the first generation is architected to achieve better cost efficiencies than planar NAND. There are also various features that will improve latency, increase endurance and make system integration easier.

#### Micron’s 3D is a “smarter” NAND technology. What do you mean?

We have integrated various features to deliver improved performance and new functionality, including new programming algorithms and power management modes that help make system integration easier. See [FortisFlash](https://www.micron.com/products/storage/nand-flash/mlc-nand/ibm-collaboration-fortis-flash "Learn more about FortisFlash") to learn more about these features.

#### What are the details of your cell and process technology for 3D NAND?

The new 3D NAND technology uses floating gate cells and stacks flash cells vertically in 32 layers to achieve 256Gb multilevel cell (MLC) and 384Gb triple-level cell (TLC) die that fit within a standard package.

### Do you support small block devices?

Currently, Micron only offers large block devices. For more information, please refer to Technical Note, [TN-29-07: Small Block vs. Large Block NAND Devices](https://www.micron.com/content/dam/micron/global/secure/products/technical-note/nand-flash/tn2907.pdf).

### How do I achieve greater PROGRAM/READ throughput for the NAND device?

To get the maximum PROGRAM/READ throughput for Micron NAND Flash devices, use the PROGRAM and READ CACHE operations. See the NAND device data sheet and our NAND Technical Notes Page for details on how to use these commands.

### How is High-Speed NAND different from traditional NAND?

High-Speed NAND can read data at speeds up to 200 megabytes per second (MB/s) and can write data at speeds up to 100 MB/s. These speeds are achieved by leveraging the new ONFI 2.0 interface specification and a four-plane architecture with higher clock speeds. In comparison, conventional SLC NAND is limited to 40 MB/s for reading data and less than 20 MB/s for writing data. To maximize the performance benefits of High-Speed NAND, users must use the new ONFI 2.0 synchronous interface standard.

### How is Nvb specified?

Nvb is specified as the minimum number of valid blocks at the end of the P/E cycle spec.

### How much ECC do I need to support your devices?

We define our ECC requirement per 512-byte section. MLC NAND devices have a higher ECC requirement than SLC NAND due to the increased number of bits per cell. ECC requirements differ for designs, so consult the device data sheet for the amount of ECC needed.

### I am seeing a lot of READ DISTURB errors. Can you tell me if there is a problem with your part?

READ disturb occurs when the same data is read repeatedly. By its nature, NAND technology has a very low occurrence of read-disturb errors. But, to mitigate any errors received due to read disturb, we recommend that users refresh the data to reduce the amount of times the same data is read.

### I am using the correct amount of error correction code (ECC) for the NAND device, but I’m still seeing bit/byte errors in data I read back from the NAND device.

Make sure that you are issuing a READ STATUS command to the NAND device after any type of PROGRAM or ERASE operation. Checking status after a PROGRAM or ERASE operation will report whether the PROGRAM or ERASE operation was successful. If the READ STATUS command reports a failure with a PROGRAM operation, that data should be programmed somewhere else and the block being programmed should be retired. If the READ STATUS command reports a failure with an ERASE operation, that block should also be retired.

### I’ve heard that NAND has too many errors to boot from. Is this true?

With ECC, NAND can achieve bit error rates (BER) that are comparable with NOR, which is commonly used as a booting device. Applications that use NAND typically copy the booting code to DRAM and execute from DRAM. For more information, read [Tech Note 29-16](https://www.micron.com/content/dam/micron/global/secure/products/technical-note/nand-flash/tn2907.pdf), which is geared to a specific processor, but the concepts can be applied generally. [TN-29-19](https://www.micron.com/content/dam/micron/global/secure/products/technical-note/nand-flash/tn2916.pdf) is a very useful technical note on the general concepts of NAND.

### Should I be marking blocks bad due to READ errors?

Yes.

### When I issue a Read ID command (90h) to a two-die NAND device, I get a device ID back that states it is a one-die NAND device.

In a two-die NAND device, where a single die is on each CE#, the device ID that is returned is per CE# for one die. For example, an 8Gb two-die NAND device with two CE# pins would return a 4Gb device ID on each CE#. See the Read ID section of the NAND device data sheet for more details.

### Where can I find additional technical information about Micron NAND devices that is not covered in the device data sheets?

Additional Micron NAND Flash technical information—including details on performance enhancing commands—can be found on the Technical Notes page for NAND.

### Where can I find simulation models for NAND Flash devices?

Micron posts Verilog, HSPICE, and IBIS models for NAND devices. To find the right model for your needs, see the appropriate NAND part catalog and select your device to view the available models.

### Why am I getting a bit/byte error reading back the information I programmed into the NAND device?

Check that you are using the appropriate amount of error correction code (ECC) for the NAND device. The ECC threshold can be found in the "Error Management" section of the NAND device data sheet. Also ensure that none of the bad blocks marked by the NAND manufacturer (Micron) are used. See the "Error Management" section of the NAND device data sheet for more details on how to search for manufacturer-marked bad blocks.

### Why doesn't the NAND Flash device respond correctly to commands issued to it?

Be sure you are issuing a reset command (FFh) to the NAND device after powering on the device. A reset command (FFh) must be issued to each valid chip enable (CE#) of the NAND device before any commands are allowed to be issued to that CE#.

## Graphics memory

### GDDR5 (3)

#### How does Graphics DRAM differ from regular DRAM?

Graphics DRAM is a category of DDR SDRAM designed to handle very large bandwidth requirements. Unlike standard DRAM, graphics DRAM is typically soldered down on the same PCB as the SoC and always supports 32 DQs per memory component. Besides graphics cards and game consoles, graphics DRAM is being used in high-bandwidth applications like networking, automotive and high-performance computing.

#### What features and functions does GDDR5 have versus previous generations of Graphics DRAM?

GDDR5 provides higher densities, lower external voltage and more than twice the memory bandwidth compared to its predecessor, GDDR3. GDDR5’s 4X relationship between data rate and the CK clock is unique compared to the 2X relationship in DDR3 and GDDR3.

#### Is GDDR5 a direct replacement for GDDR3?

No, GDDR5 is not a direct replacement for GDDR3 due to package size differences. GDDR3 has a 136-ball BGA package while GDDR5 has a 170-ball BGA package.

### GDDR5X (7)

#### How does Graphics DRAM differ from regular DRAM?

Graphics DRAM is a category of DDR SDRAM designed to handle very large bandwidth requirements. Unlike standard DRAM, graphics DRAM is typically soldered down on the same PCB as the SoC and always supports 32 DQs per memory component. Besides graphics cards and game consoles, graphics DRAM is being used in high-bandwidth applications like networking, automotive and high-performance computing.

#### What features and functions does GDDR5X have compared to previous generations of Graphics DRAM?

GDDR5X provides higher densities and lower external voltage (1.35V) compared to its predecessor, GDDR5. GDDR5X also doubles the bandwidth (10–16 Gb/s) of GDDR5 while remaining on traditional discrete package technology (FBGA).

#### Can GDDR5X operate in GDDR5-like mode?

Yes, GDDR5X has two operation modes:

* QDR mode: Supports speeds of 10 Gb/s and above
* DDR mode: Supports 0.2–6 Gb/s speeds and is compatible with GDDR5

#### Does GDDR5X support JTAG boundary scan?

Yes, GDDR5X has IEEE 1149.1 compliant boundary scan.

#### What is Micron’s competitive position with GDDR5X?

Micron is the first memory supplier in the industry supporting GDDR5X in mass production.

#### Is GDDR5X a JEDEC standard?

Yes, the GDDR5X SGRAM standard was first published in Dec. 2015 as JESD232. The latest JEDEC release is JESD232A.

#### Does GDDR5X replace GDDR5?

GDDR5X is not a direct replacement for GDDR5 due to package size differences. GDDR5 has a 170-ball, 0.8mm-pitch BGA package while GDDR5X has a 190-ball, 0.65mm-pitch package.

### GDDR6 (8)

#### How does Graphics DRAM differ from regular DRAM?

Graphics DRAM is a category of DDR SDRAM designed to handle very large bandwidth requirements. Unlike standard DRAM, graphics DRAM is typically soldered down on the same PCB as the SoC and always supports 32 DQs per memory component. Besides graphics cards and game consoles, graphics DRAM is being used in high-bandwidth applications like networking, automotive and high-performance computing.

#### What features and functions does GDDR6 have compared to previous generations of graphics DRAM?

GDDR6 provides higher densities than previous-generation graphics memory. It doubles the bandwidth of GDDR5, extending past GDDR5X speeds. In addition, it is based on a dual-channel architecture, which enables a huge performance increase while still providing backward compatibility to GDDR5 memory access size.

#### Can GDDR6 operate in GDDR5-like mode?

No

#### Can GDDR6 operate in GDDR5X-like mode?

Yes

#### Does GDDR6 support JTAG boundary scan?

Yes, GDDR6 has IEEE 1149.1 compliant boundary scan

#### What is Micron’s competitive position with GDDR6?

Micron is leveraging its GDDR5X-based high-speed signaling know-how from more than two years of design, mass production, test and application learning in Micron GDDR6 products. This allows Micron to remain in the leading position on high-speed signaling with traditional memory components.

#### Is GDDR6 a JEDEC standard?

Yes, the GDDR6 SGRAM standard was first published in July 2017 as JESD250.

#### Does GDDR6 replace GDDR5 or GDDR5X?

GDDR6 is not a direct replacement for GDDR5 nor GDDR5X due to package size differences. GDDR5 has a 170-ball, 0.8mm-pitch BGA package, GDDR5X has a 190-ball, 0.65-mm pitch BGA package and GDDR6 has a 180-ball, 0.75mm-pitch BGA package.

## Hybrid memory cube

### Why is Micron discontinuing HMC?

Micron reviews product roadmaps on a continuous basis to ensure that our current portfolio addresses current and future market needs. Since the early introduction of HMC, additional/alternate high-performance memories have entered the market, and the volume projects that drove initial HMC success are reaching maturity.

### What will replace HMC high-end performance memory?

Micron will continue to develop and design memory for high-performance applications. GDDR has roadmap support and continues to grow in this space. Micron has also established an HBM development program.

### How do I order last-time buy quantities?

Please work with the appropriate sales team or distribution contact to ensure last-time buy quantities are communicated to Micron prior to the last-time buy date.

### I am ramping production in 2019; how do I secure HMC for the lifetime of my product?

See above.

### Does this mean that Micron is no longer focusing on the networking space?

Micron is the leading supplier of memory in the networking space, and we will continue to focus on and evaluate future opportunities.

### What about the HMCC?

The Hybrid Memory Cube Consortium (HMCC) is a working group made up of industry leaders who build, design in or enable HMC technology. The goal of the HMCC is to define industry-adoptable HMC interfaces and to facilitate the integration of HMC into a wide variety of applications that enable developers, manufacturers and enablers to leverage this revolutionary technology.

The HMCC is engaged in great exploratory work. Micron will continue to support/provide input to HMCC for technology discussions and learnings from customer engagements.

## Multichip packages

### Do you have any reliability data on the PoP?

Yes. We do have reliability data on the PoP. [Contact Micron](https://www.micron.com/forms/contact-us) for more information.

### For a PoP/MCP, does the qualification testing at the factory differ from testing on the discrete components?

No. the PoP/MCP parts undergo the same qualification testing as the discrete components.

### How do I know the Micron part number for the part on the Beagle Board?

The Beagle Board uses our NAND + Mobile LPDDR PoP combination parts, and the densities vary depending on which version of the Beagle Board you have. Type the second 5-digit alphanumeric code on the physical part into our FBGA Decoder, which will provide you with the corresponding Micron part number.

### I’ve heard that opting for a PoP/MCP solution is more expensive than using discretes, so why should I use it?

From a system-solution perspective, because the PoP mates directly onto the processor, it eliminates the need to have traces routed on the PCB. This saves costs for the customer, as well as provides better signal integrity.

### Our contract manufacturer has little experience with PoP. Why should we try something new?

The market is driving the requirement for the smaller PoP form factor, and several contract manufacturers have already enabled this technology. PoP can help save in routing costs and improve signal integrity. Given those cost and performance advantages, Micron recommends that you work very closely with your CM to ensure a good transition to this technology.

### We designed in discrete parts, but now we are using PoP parts. They appear to be limited in what speeds we can achieve. What is the problem?

When moving from testing with discrete parts to PoP, care should be taken that no stubs are left from the design containing the discrete components. If needed, a 0 Ohm resistor could isolate the memory from the traces used for the discrete part.

### What are your PoP/MCP offerings for x8 NAND and/or x16 Mobile LPDD

Our standard offerings are x16 NAND and x32 Mobile LPDDR. We also have x8 NAND and x16 Mobile LPDDR. For the most current information, [contact your local Micron support.](https://www.micron.com/forms/contact-us)

### What is an MCP? What is a PoP? What is the difference between the two devices?

MCP is multichip package that contains multiple die and can be used by any controller. PoP is a form of an MCP made specifically to stack on top of a processor that has pads on the top side that mate to the ballout of the PoP. Because the PoP package stacks right on top of the processor, it eliminates the need to have traces routed on the PCB and provides better signal integrity. A variety of PoP packages are designed for various processors. PoP and MCP devices give designers the ability to take advantage of z space and to provide the flexibility to offer different logic in one package (for example, NAND + Mobile LPDDR or e.MMC™ + NAND + Mobile LPDDR). We have a wide selection of offerings to meet our customer’s needs.

## Solid state storage

### Can I buy a Micron SSD for personal use?

We sell SSDs (and memory) direct to the consumer through our Crucial brand. Crucial SSDs offer the same great quality, reliability, and performance of Micron SSDs, but are packaged for consumer sales. You can buy one today at [crucial.com/ssd](https://www.crucial.com/products/ssd).

## Bare die

### Does Micron offer product in whole wafer form and singulated die?

Nearly all Micron memory die shipments are now sold as whole wafers, not singulated die (check with your local sales contact for availability). Wafer maps are provided in each wafer shipment. For more information on wafer mapping, see [TN-00-21](https://www.micron.com/content/dam/micron/global/secure/products/technical-note/nand-flash/tn0021.pdf).

### How does Micron ship bare die product?

Micron die are provided as whole wafers and are shipped in horizontal wafer shippers ("coin stacks") or vendor boxes. Customers must have a clean room environment to store and unpack Micron wafers. For more information, see [CSN 20: Whole Wafer Packaging](https://assets.micron.com/adobe/assets/urn:aaid:aem:b5c01ed7-fe91-4424-9e29-99e65f43715f/renditions/original/as/csn20.pdf).

### What wafer thickness options does Micron offer?

Standard "unground" wafer thickness is 750µm for 200mm wafers and 790µm for 300mm wafers. Micron offers additional wafer thickness options for 200mm wafers, depending on the product. Please see the applicable die data sheet for die thickness options beyond the standard thickness. Depending on customer demand, Micron may consider processing alternative thicknesses. Please consult your sales representative for more information.

## Support

## Serial presence detect

### Can I verify that the hexadecimal SPD values are correct?

Converting the hexadecimal value to binary and then matching it against the associated SPD byte in the appropriate JEDEC SPD specification will provide a translation of what the byte is for and how it is set.

### How are SPD values determined?

Micron utilizes a proprietary application that generates SPD values for each part number based on engineer’s input and a database of rules. The rules housed within the database are carefully written to ensure that JEDEC SPD specifications are adhered to. This process ensures compatibility and consistency.

### What are the JEDEC SPD specifications?

The SPD specifications for modules are determined by JEDEC. Micron uses several SPD specifications within JEDEC Standard No. 21-C to determine and generate SPD data for SDRAM, DDR, DDR2, DDR3 and FBDIMM modules. These specifications are available (if ratified) to the public at [www.jedec.org](https://www.jedec.org/). Specifications that have not yet been completed or ratified are available to JEDEC members only.

### What is the acronym SPD stand for?

Serial Presence Detect

### What is the SPD data used for?

The SPD data represents different electrical and physical characteristics of the module. This data is permanently stored in an electrically erasable programmable read-only memory (EEPROM) on the module. A basic input/output system (BIOS) access SPD information through the SMBus. The system BIOS can then use this data to configure the system to optimize the memory that has been installed.

### What is the SPD table for?

The SPD table shows the hexadecimal values for each byte that is held in the EEPROM on each memory module.

## Sim models

### Are Verilog models available for Micron modules?

Verilog models can be created for DDR, DDR2, and DDR3 modules by using a Micron-provided wrapper in conjunction with the Verilog model for the DRAM components used on the specific module you're working with. The configurable DIMM model file (ddr\_dimm.v, ddr2\_module.v, or ddr3\_dimm.v) is included in the DRAM Verilog model .zip file download for DDR, DDR2, and DDR3 components. The readme.txt file included in the .zip provides instructions for configuring the DIMM model.

### Can a parity module be used in a system that is not designed to use parity?

Micron’s modules are manufactured to be hardware-compatible with both parity and non-parity systems. Par\_in (parity in) and the high order address signals have a weak (100K-ohm) pull-down resistor to stabilize the inputs from oscillating around the switch point. Err\_out (parity error out) is an open drain and should be left as a true no connect unless used in a parity system. The SPD data on a parity module does reflect parity. In rare occasions, the firmware or BIOS of a non-parity system will err on the parity bit in the SPD. For this reason, the system designer should ensure that the firmware of the non-parity system expects or ignores this portion of the SPD data.

### Can Micron provide models for the module connectors?

It is suggested that models for connectors be acquired from the connector manufacturers to ensure an accurate model. Micron may be able to provide a simple, uncoupled RLC connector model to be used as is or to create your own connector model. Please e-mail [DRAM Support](mailto:DRAMSUPPORT@micron.com) to request this model.

### Can Micron provide module Gerber files to customers?

As a rule, Gerber and ODB++ files are not provided to customers, because the files contain proprietary information about our design and could be used to mass-produce our product without our consent. There is normally no reason that a customer would need Gerber files. Gerber files are provided to PCB manufacturers to mass-produce PCBs. IBIS, EBD, or board files provide enough information for customers to create models and perform signal integrity simulations.

### Does Micron provide Hyperlynx models?

Micron can provide Hyperlynx models upon request for most modules. Please e-mail [DRAM Support](mailto:DRAMSUPPORT@micron.com) with your request and provide the complete part number of the module you are interested in. Please note, it may take up to two weeks to receive the model once your request has been acknowledged.

### Does Micron provide VHDL models for modules?

Micron does not provide VHDL models for modules. We have focused our modeling resources on higher utilized modeling standards such as IBIS, Verilog, and HSPICE. However, alternatives to VHDL models are available: Denali and Synopsys both have libraries of memory components and module models available on their Web sites. These EDA packages may be an alternate way to create behavioral simulations in the absence of VHDL model. Some simulators such as ModelSim provide a dual language option (VHDL and Verilog). To simulate in this manner, a VHDL wrapper can be used around currently available Verilog models.

### Does the model that I'm downloading support all the drive strengths listed in the data sheet?

To discover the model’s supported drive strengths, do the following:  
- HSPICE model: Look at the .sp files for information on supported drive strengths and how to select them.  
- IBIS model: Do a text search for the [Model Selector] section. This section describes the drive strengths that can be selected for a given input/output or output buffer.

### How do I tell if I have the correct IBIS or HSPICE model for a given die revision indicator?

HSPICE model: Look in the readme file for die revision information.  
IBIS model: Look at the top of the file for die revision information.

### How does Micron validate the quality of its IBIS and HSPICE models?

To validate a model to lab measurements, Micron compares several items, such as input capacitance, power and ground clamp diode characteristics, output buffer drive strength, and output buffer slew rates. New Micron models include a quality report that compares model characteristics to lab measurements and data sheet specifications.

### My simulation software does not support IBIS 4.0 and newer standards. How do I make Micron's IBIS 4.0 level model work with my IBIS 3.2-compliant simulator?

Most Micron models contain very few keywords specific to IBIS 4.0. In many cases, the model can be made IBIS 3.2-compliant with a few simple changes. First, change the [IBIS Ver] keyword to 3.2. Next, place a comment character ("|") in front of the "Vref" section under each [Model Spec] keyword. Finally, comment out each [Receiver Thresholds] section.

### What advantage do dual-rank modules have over single-rank modules?

Having two ranks available to the memory controller is advantageous in terms of both performance and power. For example, while the controller is waiting for a 64-bit word to be available on one rank, the second 64-bit rank can be accessed. This interleaving increases the overall performance of the module. Power can also be reduced on a rank that is not in use, reducing the power consumption of the module.

### What does the model revision number indicate when it changes from a 1.x level to a 2.x level?

1.x level model indicates that the model has not been correlated to any lab measurements. Typically, 1.x level models are provided for pre-silicon or pre-production devices. A 2.x level model has been correlated to lab measurements.

### What is a board (.brd) file?

A board file is a complete electrical and mechanical representation of a PCB. EBD and ODB++ files are generated from board files. Board files are not to be provided to customers without an NDA since the files contain confidential and proprietary information about the module design.

### What is a Gerber file?

Gerbers are files sent to PCB manufacturers to produce PCBs. Gerber is a dated term because board shops currently require ODB++ files to mass-produce PCBs. The term Gerber is used loosely. It sometimes refers to any of the files that represent the PCB’s electrical and mechanical characteristics, including EBD, ODB++, and board files. When a customer asks for Gerber files for a module, it is important to determine what specific files they really need.

### What is a "rank"?

A rank typically refers to the data bus width of a system. This width is generally 64 or 72 bits. For example, if 8 components with a width of 8 bits each are mounted to a PCB, this creates a module that is 64 bits wide, enabling a 64-bit word to be read out of the module. We refer to this as a "single-rank" module. Sixteen components with a width of 8 bits each can be mounted to a PCB to form two, 64-bit-wide ranks, creating a "dual-rank" module.

### What is an EBD (.ebd) file?

A rank typically refers to the data bus width of a system. This width is generally 64 or 72 bits. For example, if 8 components with a width of 8 bits each are mounted to a PCB, this creates a module that is 64 bits wide, enabling a 64-bit word to be read out of the module. We refer to this as a "single-rank" module. Sixteen components with a width of 8 bits each can be mounted to a PCB to form two, 64-bit-wide ranks, creating a "dual-rank" module.

### What is an IBIS (.ibs) file?

An .ibs or IBIS file is a representation of a circuit meant to be read by a simulation application such as Cadence® Allegro® or HyperLynx®. IBIS (Input/output Buffer Information Specification) is an EIA (Electronic Industries Alliance) standard. IBIS is a text file in a specific format that represents the current versus voltage and voltage vs. time characteristics of the inputs and outputs of a circuit. IBIS models are the preferred files to provide to customers since the files do not contain any proprietary information about the internal makeup of the components. NDAs are not normally required for IBIS files.

### What is the advantage of multiple banks within a component?

Memory controllers can begin an operation in one bank and perform a separate operation in a different bank while the first operation is completing. This interleaving increases the performance of the DRAM as a whole.

### What is the difference between a "bank" and a "rank?"

Banks are specific to individual DRAM components and refer to sub-arrays within the DRAM component. Ranks are specific to memory modules and refer to a sub-array made of multiple DRAM components.

### What makes up an IBIS model for a module?

The complete IBIS model for a module consists of several files:  
  
1. The IBIS models of the DRAM used on that particular module  
2. The IBIS models of the PLL, registers, and EEPROMs (as needed)  
3. The IBIS model of the resistive parallel terminations on the PC  
4. The EBD (electronic board description) file of the PCB. This file references the IBIS file of the terminations mentioned above.  
  
Together, these files provide a complete representation of the PCB.

### What trace lengths and termination values does Micron suggest I use on my memory interface?

Board designers often ask this question when they’re looking for a starting point for their CAD drawings or simulations. Because there are so many variables to consider, it is difficult to provide a "correct" answer. Clock speed, timing, registered or unbuffered modules, and trace impedance are all important factors. Some controllers have on-die termination, some do not. Some controllers have multiple copies of the command and address bus. All of these factors can affect trace lengths and termination and can affect how acceptable signal integrity is achieved.  
  
Micron design guide technical notes for each technology can be used as a starting point, but trace length and termination must ultimately be proven by simulation and physical testing. Please find our simulation models by searching through each technology part catalog.

### Why are IBIS models for DRAM components regularly posted to micron.com but not IBIS models for modules?

We have found that it is more efficient to create module models as they are requested by our customers. If you are unable to locate the IBIS model for the module you are interested in, please e-mail your request to [DRAM Support](mailto:DRAMSUPPORT@micron.com).

## About Micron

## Elpida Acquisition

### General Information (5)

#### I currently do business with Elpida; has their employee contact information changed?

You can continue to reach your contact at the same phone number and office location. Your contact should provide you with their new Micron email address to use moving forward.

#### Will Elpida's company name change?

Effective Feb. 28, 2014, Elpida changed its name to Micron Memory Japan and Elpida Akita changed its name to Micron Akita, Inc.

#### Have Elpida sales offices or locations changed?

As we continue to integrate Elpida into Micron some of the sales office locations will change. Please contact your local sales representative for further details.

#### Where can I find out more information on the Micron/Elpida Transition?

Your sales representative is available to answer any questions you may have and will work closely with you to ensure that all issues are defined and resolved to the greatest degree possible.

#### I am interested in applying for a job with Micron (or the former Elpida); who do I contact?

Go to [www.micron.com/careers](https://www.micron.com/about/careers) to apply for a job.

### For Customers (7)

#### I buy from both Micron and Elpida. Whom should I contact now?

Continue working with the same sales and customer service representatives as before. If changes are made to these contacts you will be notified immediately.

#### Where can I find Elpida product information?

Elpida product-related information has been integrated into www.micron.com. Use these helpful hints for identifying Elpida parts and navigating our expanded part catalogs:

* All Elpida part numbers begin with the letter “E.”
* Elpida parts appear at the beginning of the part catalog because part lists are sorted alphabetically based on the part number.
* Part catalogs are sortable; use the filter at the top of the part catalog to narrow down part listings based on technology, density, or other features.

#### Will there be new part numbers for the former Elpida product line?

The ordering part number will change to include the Package Media designator (Tape & Reel or Tray). A Product Change Notification was issued in December 2013. Please contact your sales representative if you have any additional questions.

#### Where do I get data sheets and product support information for Elpida products?

For Elpida part information, including access to Elpida-specific part catalogs and data sheets, visit micron.com/elpidaparts.

#### Will the marking and labeling of Elpida products change?

At this time, there are no plans to change the logo or part mark on Elpida branded products. If there are any changes, Micron will work to minimize any impact to our customers and will use appropriate channels to communicate those changes to our customers.

#### If I am in the process of qualifying a Micron/Elpida part, what should I do?

Continue any qualifications that are in progress, unless you hear otherwise from your account support team. If you have questions about support or what to qualify, please rely on your existing Micron or Elpida technical contacts for information.

#### I am currently buying Elpida products from a distributor; where do I go now for products?

Micron has made changes to the Micron Distribution network. For a complete list of authorized Micron distributors, reference the [Micron Authorized Distributor list](https://www.micron.com/sales-support/sales-network/authorized-distributors). Micron Authorized distributors will sell both Micron and Elpida products. If you have any questions or issues ordering products, please send an email to [distribution@micron.com](mailto:distribution@micron.com); and we will ensure that someone assists you. If over time, Micron decides to make further changes to its distribution network, we will work proactively with distribution and customers on their supply chain needs.

### For Suppliers (3)

#### What will become of Elpida/Rexchip’s purchase orders, invoice & payment systems/processes?

* Business systems migrate to Micron’s SAP Procurement environment.
* The purchase order layout and numbering will change beginning in March 2014.
* Replacement Micron purchase orders will be created for open Elpida/Rexchip purchase orders between Feb. 28, 2014 to March 7, 2014, and will reference the former Elpida/Rexchp purchase order number.
* The bill-to address on Micron purchase orders may be different than previous Elpida/Rexchip addresses. A letter was distributed to Elpida/Rexchip suppliers the first week of February 2014 with the new legal entity and billing address.
  + [Legal Entity name and billing addresses](https://assets.micron.com/adobe/assets/urn:aaid:aem:ce413436-7ebd-4bf5-80c5-235b51c06de4/renditions/original/as/new-micron-legal-entity-and-billing-address.pdf)

#### What will become of Elpida’s agreements and contracts with its suppliers?

* Third party agreements that are in effect for each of the Elpida legal entities will be assigned to Micron and/or ultimately terminated. Impacted suppliers will be contacted.
* A core team of Micron and former Elpida team members are working to address these agreements. No change is anticipated however you may be contacted by Micron in the event an agreement is impacted.

#### I do business with both Micron and Elpida and/or Rexchip, what terms and conditions will we be using?

Micron’s terms and condition will be applicable to all purchases. Generally these are contained in a Purchase Order. For Micron Memory Japan, they are typically contained in a Master Purchase Agreement. However, if you have an existing signed agreement with Elpida, in general, the terms and conditions contained therein will continue to apply until such agreement is modified or its term ends.

## Foundation

### What are the funding priorities and initiatives of the Micron Foundation?

The Micron Foundation’s primary focus areas are to provide equitable opportunities for underrepresented populations, enrich our communities and increase access to STEM education to create lasting social impact. These priorities are discussed throughout our homepage.

### What kinds of organizations can the Micron Foundation support?

The Micron Foundation supports a range of eligible, nonprofit and academic organizations. Eligibility requirements vary by funding opportunity and must align with our primary giving areas.

### What is the relationship between the Micron Foundation and Micron Technology?

Established in 1999 by Micron Technology, the Micron Foundation is a private nonoperating corporate foundation with an endowment fund. It is recognized as a 501(c)(3) organization by the IRS.

### Where is the Micron Foundation located?

The Micron Foundation has no single physical office. It is incorporated in Idaho, United States, and has team members based at Micron locations around the globe.

### How does my organization apply for a grant or sponsorship from the Micron Foundation?

The Micron Foundation identifies partners in our site communities through grass roots efforts and other partner interactions. We are not currently accepting unsolicited funding proposals or requests.

### Does the Micron Foundation support youth sports teams, school events or fundraisers, or similar activities?

Micron supports these types of causes through our employee giving program. The Micron Foundation matches team member contributions dollar for dollar to qualified nonprofits or schools registered in the [Benevity Causes portal](https://causes.benevity.org/). Team members must donate directly via the Micron Gives platform or submit receipts for donations to be matched within the calendar year they are made.

### Does the Micron Foundation support organizations globally or in the United States only?

The Micron Foundation supports both U.S. and eligible international organizations.

### Does the Micron Foundation focus on specific geographic areas?

The Micron Foundation focuses primarily on the communities where Micron team members live and work, but we also work at regional levels, in alignment with our giving strategies, to make a difference.

### Does the Micron Foundation give funding directly to individuals in need?

No, the Micron Foundation's funding supports eligible nonprofit organizations and schools; it is not for individuals.

## Green Engineering

### Are Micron’s Pb-free products RoHS-compliant? What does 5/6 RoHS mean?

Yes. Directive 2011/65/EU (replacing the Directive 2002/95/EC), Restriction of the use of certain Hazardous Substances in Electrical and Electronic Equipment (RoHS), does impact Micron's semiconductor products. The purpose of this directive is to restrict the use of certain hazardous substances in electrical and electronic equipment and protect human health and the environment. Micron’s products have always been 5/6 RoHS compliant, meaning they contain Pb solder, but otherwise comply with RoHS regulations (they meet five of six stipulations). Micron’s Pb-free products are completely RoHS compliant.  
  
Micron's RoHS compliant module level products do contain electronic parts that may use Pb for applications exempt from Directive 2011/65/EU (see Article 4, Annex 3). Please contact your sales/marketing representative for more information.  
  
The European Commission FAQ sheet distributed under the Directorate-General Environment may serve as a formal (but not legally binding) point of reference.

### Do Micron’s Pb-free products comply with China RoHS reporting requirements? Does Micron label its products with the Environmental Protection Use Period?

Micron’s Pb-free component, die, and wafer-level products do not contain any of the six substances restricted by the China RoHS. Micron’s modules may contain Pb in both not exempted and exempted EU RoHS applications (where not reliable Pb-free alternatives are available in the market).

Micron’s products are not sold directly to consumers. The EPUP and other marking and labeling requirements apply only to the products sold directly on the consumer market. For more information contact your sales/marketing representative.

*These substances are not intentionally added by Micron during the manufacturing process but can be present in trace amounts in the raw materials used to manufacture the finished products.*

### Is Micron aware of REACh requirements?

Micron is fully aware of product requirements coming from Regulation 2006/1907/EC, Registration, Evaluation **A**uthorization and **R**estriction of **Ch**emicals. Micron constantly monitors new additions to the Candidate List and timely verifies if any **S**ubstance of **V**ery **H**igh **C**oncern is used in the manufacturing processes and the potential impact on the final products. Micron is committed to provide our customers with information about substances in its products as required. For any documentation needs, please contact your sales representative.

### How does Micron define green products?

In addition to being RoHS compliant, Micron's Green packages do not contain substances that have been identified as harmful to the environment or known to pose serious reliability: bromine, chlorine, antimony containing substances, and inorganic red phosphorus. These substances are not intentionally added to packaging materials such as encapsulants, die attach materials, underfill epoxies, and substrates. The maximum trace amounts of these substances allowable in Micron’s green packages are listed below.  
  
<900 ppm Chlorine  
<900 ppm Bromine  
<1500 ppm Chlorine & Bromine  
<900 ppm Antimony  
<100 ppm Red Phosphorus  
  
Please note that while our Pb-free and green products do not contain any intentionally added Pb, our Pb-free parts are not necessarily green, since they may contain halogen or antimony compounds.  
  
*\*These substances are not intentionally added by Micron during the manufacturing process but can be present in trace amounts in the raw materials used to manufacture the finished products.*

### Does Micron still make parts that comply with RoHS 5/6 standards?

Yes, along with our Pb-free product line, Micron also supports RoHS 5/6 products. We recognize that certain applications are exempt from the [RoHS directive](https://www.gov.uk/government/publications/restriction-of-hazardous-substances-rohs-regulations).

### Where can I find Micron's green and RoHS products part numbers?

Micron’s full line of RoHS compliant memory products can be found in the part list tables for each product type. To perform a quick compliance check on a single part number, use the "Part Number Search" tool. For information on green products, please contact your local Micron sales representative.

### How do I get Micron's RoHS certificate of compliance?

You can find a part-specific RoHS Certificate of Compliance by navigating to the part detail page or using the main products family navigation.

### How do Micron’s green products comply with international standards?

Micron’s green engineering program is RoHS-compliant and conforms with most of the world’s emerging environmental standards, including those in Asia and Europe.

### What materials does Micron use in its Pb-free semiconductors?

* For solder balls, Micron is replacing tin-lead alloys (Sn36Pb2Ag or Sn37Pb ) with a tin (Sn), silver (Ag), and copper (Cu) alloys (e.g., SAC105, SAC305, SAC405, LF35).
* For solder paste on modules, Micron is replacing Sn37Pb with Sn3.8Ag0.7Cu.
* For leaded TSOP, Micron is replacing 90Sn10Pb with matte Sn plating.

These substitutions ensure Micron’s Pb-free parts are RoHS-compliant. Parts are certified for a surface mount temperature of 260°C.

### When will Micron complete its transition from Pb-free to green products?

Micron can currently provide Pb-free and green product to customers who require it. The availability of these products is highly dependent on customer demand, as well as on the availability of "green" non-memory components and materials.  
  
Please contact your local Micron sales representative for more information (look up regional sales representatives on the [Sales Network](https://www.micron.com/sales-support/sales-network/authorized-distributors)page).

## ISO 14001

### Is Micron ISO 14001 Certified?

In February of 1997, Micron Technology, Inc., was one of the first companies in the United States to attain certification under the new ISO 14001 Environmental Management Systems Standard. Micron was selected by KEMA Registered Quality, Inc., to be a pilot participant in the ANSI-RAB National Accreditation Program and is one of five U.S. pilot companies who participated in this program.

### What are the Basic Elements of Certification?

Certification under ISO 14001 requires conformance with four basic elements:

* implementation of an environmental management system
* assurance that procedures are in place to maintain compliance with applicable regulations
* commitment to continual improvement
* commitment to overall prevention of pollution

### What is ISO 14001?

ISO 14001 are voluntary international environmental management standards, which ensure that organizations have effective environmental systems. It is the environmental equivalent to the ISO 9000 quality standards. Various countries and companies have implemented the ISO 9000 quality standards worldwide.

### Who Certified Micron?

In the ISO 14000 process, a company's environmental management systems are audited by third party registrars. Micron was audited by KEMA Registered Quality, Inc. KEMA is a worldwide full-service third party registrar accredited to ISO 9000, QS9000, and ISO 14001 by ANSI-RAB and RvA, as well as being a "Notified Body" for several areas of CE marketing, mandatory product certification of the European Union. KEMA's clients number in the thousands worldwide and include a wide variety of product and service industries. KEMA specializes in the electronics, information technology, and high technology manufacturing areas.

### Why Did Micron Become Certified?

Micron has a very proactive approach to environmental compliance and protection that serves our employees, our customers, and the communities in which we operate. We are proud of both our environmental and worker safety programs. We view compliance to minimum regulations, as a baseline and work to always be better than the minimum regulations require. ISO 14001 is a good fit with our company and culture. The primary force behind the development of standards for environmental management has been the desire for environmental stewardship and accountability. ISO 14001 embodies an approach, which looks beyond regulatory compliance and challenges an organization to take stock of its environmental programs, continually improve, and commit itself to effective processes and pollution prevention. Micron already had most of the elements needed to conform to ISO 14001 in place. We saw this as an opportunity to be recognized for our commitment, level of effort, and record of accomplishments.

## Other

## General product

### Does thermal information change for IT parts?

Thermal information includes temperature limits and thermal impedance values. Temperature limits do change for IT parts (TC, TJ, and TA), but thermal impedance values (θJA, θJB, and θJC) do not because thermal impedance depends primarily on the package.

### My design was based on a specification stating the JTAG was relative to VDD (1.8V), but now we’ve discovered that JTAG is actually relative to VDDQ (1.5V). It’s a fairly significant board spin to change this; what do I risk by leaving the design as-is? I assume that the specification is still for VDDQ + 0.3V = 1.8V, but with CMOS parts there’s no way I can guarantee that it won’t swing past that on transitions.

Your particular board design should not be a cause of major concern. The pins can handle the VDD voltage regardless of the VDDQ voltage.

### Should the ECC memory chip share chip select and CKE signals with the other two main memory chips in our point-to-point application?

The ECC chip(s) should share the same CKE and CS# as the other devices because they are accessed as the same piece of data.

### What is a "bank"?

A bank is an array of memory bits. Multiple arrays or banks are contained within a DRAM component. Depending on density, DRAM components may consist of 4 or 8 banks. For example, a bank may consist of 32 million rows, 4 bits across. This would equate to 128 megabits. Four of these banks in a single DRAM component would yield a 512Mb component.

### What is the impedance tolerance of the driver in match-impedance mode relative to the expected value base on the perfect reference resistor connected to ZQ pin?

The impedance tolerance of the driver is ±15 percent.

## ONFI

### Are your NAND parts ONFI-compliant?

All our 50-series NAND devices and beyond are ONFI-compliant.

### How will ONFI help speed time-to-market for NAND-based products?

ONFI improves time-to-market in two principal ways:

1. It simplifies the design of Flash controllers that support a range of components by improving uniformity in the behavior of the interface to the NAND components.

2. It reduces the design time of Flash components in end-use applications and enables the use of a new generation of NAND components without design or firmware changes.

### What is ONFI?

ONFI stands for Open NAND Flash Interface. ONFI is an industry working group that is dedicated to simplifying the integration of NAND Flash memory into consumer electronic products, computing platforms, and various other applications that require solid state mass storage. The ONFI working group defines standardized component-level interface specifications for NAND Flash. ONFI is also defining module connector and module form factor specifications (similar to DRAM DIMMs) for NAND Flash. For more information, visit [www.onfi.org](https://www.onfi.org/).

### What types of products will ONFI 2.1 be seen in first?

ONFI improves the embedded integration of Flash components into a range of products, including many that use Flash today, such as mobile phones, PDAs, MP3 players, and notebooks. It’s likely, however, that the benefits of ONFI 2.1 will first be realized in PC platforms. Because of the significantly faster speeds that ONFI 2.1 delivers, SSDs and caching solutions will be able to deliver substantive benefits for PC platform workloads.

## Processing Notes

- 原始 HTML 快照无页码；按原始嵌套结构区分产品类别和问答，并保留网页中的全部问答和链接。

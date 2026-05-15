Introduction
############

.. toctree::
   :maxdepth: 2
   :hidden:

   Introduction <self>
   user/index
   reference/index
   developer

.. figure:: images/7nyI2b-Q_8-1280.avif
   :align: center
   :width: 600

LimeSDR X3 is software defined radio board based on Lime LMS7002M Field Programmable Radio Frequency (FPRF) transceiver and Xilinx Artix-7 FPGA, through which apps can be programmed to support any type of wireless standard, e.g. UMTS, LTE, 5G, LoRa, GPS, WiFi, Zigbee, RFID, Digital Broadcasting, Radar and many more.

This board is a sophisticated version featuring three LMS7002M transceiver chips which allows to implement various 5G network configurations. It supports 5G non-standalone architecture (NSA) as well as standalone architecture (SA) with simultaneous sniffing implementation using single PCIe interface based board.

The main difference of NSA and SA is that NSA delivers the control data of 5G Radio Networks to the 4G Core, while the SA connects the 5G Radio directly to the 5G core network, and the control data does not depend on the 4G network at all. NSA is a 5G service that does not "stand alone" but is built over an existing 4G network. SA, on the other hand, allows completely independent operation of a 5G service without any interaction with an existing 4G core.

As described above, 5G NSA configuration requires 4G core along 5G Radio Network. LimeSDR X3 allows to implement such configuration using two dedicated LMS7002M transceivers - one for 4G radio while second delivers 5G radio. Third LMS7002M transceiver may be utilized for calibrations, spectrum sniffing or as a RF feedback for various DSP algorithms running on FPGA.

There is a provision for White Rabbit for high accuracy of synchronization between multiple LimeSDR X3 cards. The high accuracy of synchronization in White Rabbit is achieved by extending the Precision Time Protocol (PTP, IEEE 1588-2008). This extension has been incorporated into the new 2019 revision of IEEE 1588 standard by the P1588 Working Group. White Rabbit provides sub-nanosecond accuracy and picoseconds precision of synchronization for large distributed systems which is perfect for telco applications.

All these features requires considerable data throughput between LimeSDR X3 and host processor. Second generation four lane PCI Express (Peripheral Component Interconnect Express) bus is used to manage all the data transfers between the board and host system CPU. Four lane Gen2 PCIe bus is rated for 2 GBytes/s data throughput which is sufficient for 5G NSA and sniffing applications working in parallel.

Specifications
**************

RF
==

.. list-table:: 
   :header-rows: 1
   :stub-columns: 1

   * - Parameter
     - Value
     - Notes
   * - Configuration
     - 3x MIMO (2T2R)
     - Full duplex
   * - Frequency Range
     - 30 MHz – 3.55 GHz
     - Non-continuous coverage
   * - Bandwidth
     - Up to 120 MHz
     - Software configurable
   * - Sample depth
     - 12 bit
     - 
   * - Sample rate
     - Up to 160 MSPS
     -
   * - Transmit Power
     - max 10 dBm
     - Depending on frequency

Digital Interface
=================

PCIe x4 Gen 2.

Power Supply
============

.. list-table:: 
   :header-rows: 1
   :stub-columns: 1

   * - Parameter
     - Value
     - Notes
   * - Input Voltage
     - 12 V DC
     - Via 6-pin PCIe power connector / PCIe slot (not available by default)
   * - Maximum Power
     - 75 W
     - 6-pin PCie power connector limit

.. note::
   Power consumption depends on configuration.

.. warning::
   Incorrect voltage or inadequate current capacity may cause damage or unstable operation.

Environmental
=============

.. list-table:: 
   :header-rows: 1
   :stub-columns: 1

   * - Parameter
     - Value
     - Notes
   * - Operating Temperature
     - 0 °C to +70 °C
     - Commercial-grade
   * - Storage Temperature
     - 0 °C to +70 °C
     - N/A
   * - Operating Humidity
     - 10% to 90% RH  
     - Non-condensing

Mechanical
==========

Compact single slot (X4) PCIe form factor, 232.5 × 106.7 mm (without enclosure).

Features
********

Devices
=======

* RF transceiver: 3x Lime Microsystems LMS7002M
* FPGA: Artix-7 XC7A200T:

 * 676-FCBGA (27x27) package
 * 215,360 logic elements
 * 740 DSP slices
 * 13 Mb block RAM
 * x4 Gen 2 PCIe interface
 * 10 clock management tile (CMT), each containing one MMCM and one PLL
	
* Temperature sensor
* Crypto Authentication Device
* GNSS receiver

Clock system
============

* 30.72MHz (default) VCOCXO and 38.4MHz (optional) VCTCXO
* VCOCXO disciplined (synchronisation) options:
* GNSS PPS signal
* Reference clock input or onboard DAC
* White Rabbit PTP (slave or grandmaster)
* Clock generator/PLL for baseband DACs, ADCs

Memory
======

* 256 Mbit FPGA configuration flash
* 4x 128Kbit (16K x 8) EEPROM (for each RF transceiver and FPGA data)

General user inputs/outputs:
============================

* 2x PMOD headers (0.1” pitch) connected to FPGA
* 4x dual color (RG) LEDs connected to FPGA
* 4x Switches connected to FPGA

Connections
===========

* Coaxial RF (SMA and uFL/MMCX) connectors
* uFL/MMCX connectors and headers for reference clock IN/OUT, GNSS antenna
* 12V header for powering external devices
* Fan headers
* FPGA JTAG connector (2mm pitch)

Purchasing
**********

Please see the  `Lime Micro website`_ for purchasing options.

RoHS
====

This product is RoHS compliant and does not contain hazardous substances as defined by Directive 2011/65/EU.

WEEE
====

This product must be disposed of properly according to local regulations. Do not dispose of with general household waste.

RF Transmission Notice
======================

.. warning::
   Operating RF transmitting equipment may require appropriate licensing. Users are responsible for ensuring compliance with local regulations. Unauthorised transmission may result in legal penalties.


.. _Lime Micro Website: https://limemicro.com/sdr/limesdr-x3/



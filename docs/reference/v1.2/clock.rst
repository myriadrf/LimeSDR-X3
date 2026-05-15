Clock Distribution
##################

Clock distribution block diagram is as shown in Figure 7.

.. figure:: /images/LimeSDR-X3_v1.1_diagrams_r0_clock.png
  :width: 600

  Figure 7: LimeSDR X3 v1.2 board clock distribution block diagram

LimeSDR X3 board has onboard VCOCXO U7475LF (XO3 – 30.72 MHz), VCTCXO E6245LF, E5280LF (XO4, XO5 - 30.7 MHz), ASVTX-12-A-38.400MHZ-H10-T (XO7 – 38.4 MHz) and RTX5032A (XO6 – 40 MHz) oscillators that can be used as source for clock buffer LMK00101 and clock generator CDCM6208. Only XO3 (VCOCXO, U7475LF, 30.72 MHz) is mounted and is connected to the clock buffer primary reference input. All these XOs can be tuned by 16-bit DAC (IC65), phase detector (IC64) or by FPGA using GPIO in PWM mode (not connected by default). 

Using header J30 connector is possible to connect external reference clock and PPS signal from another board. Header J31 can be used to feed reference clock and PPS signal to another board. Headers J30 and J31 can be used to synchronize several boards by daisy chaining each other.

Using J27 coaxial connector it is possible to feed external reference clock.

For Frequency and phase synchronization over network implementation (Precision Time Protocol (White Rabbit)) there is some dedicated hardware on the board: 25 MHz VCTXCO (XO1) and 20 MHz VCXO (XO2), clock generator CDCM61004 (IC59), 16 bit XO DACs (IC58, IC61) and SFP cage (J24).

100 MHz crystal oscillator (XO4) is connected to FPGA.


.. table:: Table 11. Clock signals configuration

   +---------------------------+---------------------------+------------------+--------------+---------------------------+
   | **Source**                | **Schematic signal name** | **I/O standard** | **FPGA pin** | **Description**           |
   +===========================+===========================+==================+==============+===========================+
   | Clock buffer (LMK1 –IC62) | LMK1_CLK1                 | 2.5V             | W21          |                           |
   +                           +---------------------------+------------------+--------------+---------------------------+
   |                           | LMK1_CLK2                 | 2.5V             | R3           |                           |
   +                           +---------------------------+------------------+--------------+---------------------------+
   |                           | LMK2_CLKIN0               | 2.5V             |              | Connected to LMK2         |
   +                           +---------------------------+------------------+--------------+---------------------------+
   |                           | ADF_RF_IN                 | 2.5V             |              | Connected to ADF4002      |
   +                           +---------------------------+------------------+--------------+---------------------------+
   |                           | CDCM_PRI_REF              | 2.5V             |              | Connected to CDCM6208     |
   +                           +---------------------------+------------------+--------------+---------------------------+
   |                           | LMK1_CLKOUT               | 3.3V             |              | Connected to J28          |
   +                           +---------------------------+------------------+--------------+---------------------------+
   |                           | EXT_CLK_OUT               | 3.3V             |              | Connected to J31          |
   +---------------------------+---------------------------+------------------+--------------+---------------------------+
   | Clock buffer (LMK2 –IC66) | LMS1_TxPLL_CLK            | 1.8V             |              | Connected to LMS1         |
   +                           +---------------------------+------------------+--------------+---------------------------+
   |                           | LMS1_RxPLL_CLK            | 1.8V             |              | Connected to LMS1         |
   +                           +---------------------------+------------------+--------------+---------------------------+
   |                           | LMS2_TxPLL_CLK            | 1.8V             |              | Connected to LMS2         |
   +                           +---------------------------+------------------+--------------+---------------------------+
   |                           | LMS2_RxPLL_CLK            | 1.8V             |              | Connected to LMS2         |
   +                           +---------------------------+------------------+--------------+---------------------------+
   |                           | LMS3_TxPLL_CLK            | 1.8V             |              | Connected to LMS3         |
   +                           +---------------------------+------------------+--------------+---------------------------+
   |                           | LMS3_RxPLL_CLK            | 1.8V             |              | Connected to LMS3         |
   +---------------------------+---------------------------+------------------+--------------+---------------------------+
   | RF transceiver #1 (IC1)   | LMS1_MCLK1                | 2.5V/3.3V        | AA3          |                           |
   +                           +---------------------------+------------------+--------------+---------------------------+
   |                           | LMS1_FCLK1                | 2.5V/3.3V        | AB2          |                           |
   +                           +---------------------------+------------------+--------------+---------------------------+
   |                           | LMS1_MCLK2                | 2.5V/3.3V        | AA4          |                           |
   +                           +---------------------------+------------------+--------------+---------------------------+
   |                           | LMS1_FCLK2                | 2.5V/3.3V        | AC3          |                           |
   +---------------------------+---------------------------+------------------+--------------+---------------------------+
   | GNSS module (IC46)        | GNSS_TPULSE               | 3.3V             | L20          | 1PPS time pulse output    |
   +---------------------------+---------------------------+------------------+--------------+---------------------------+
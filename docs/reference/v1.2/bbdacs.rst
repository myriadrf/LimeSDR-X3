Baseband DACs
#############

There are two Dual-Channel 16-Bit, 250Msps, digital-to-analog converters (MAX5878 – IC48, and IC49). DAC analog outputs are connected to baseband TX inputs of RF transceivers #2 (IC3). Digital input pins are connected to FPGA.

Detailed interface between DACs and other components including DAC pins, schematic signal names, FPGA pins and FPGA I/O standards is as shown in Table 9 and Table 10.

.. tabs::

   .. tab:: LMS2 TX1 BB DAC

    .. list-table:: Table 9. 16-bit LMS2 TX1 BB DAC (IC48) digital interface
      :header-rows: 1
      :stub-columns: 1

      * - Chip pin (IC48)
        - Chip reference (IC48)
        - Schematic signal name
        - FPGA pin
        - I/O standard
      * - 9
        - B0N
        - LMS2_BB_DAC1_B0_N
        - M1
        - 2.5V
      * - 8
        - B0P
        - LMS2_BB_DAC1_B0_P
        - N1
        - 2.5V
      * - 7
        - B1N
        - LMS2_BB_DAC1_B1_N
        - R6
        - 2.5V
      * - 6
        - B1P
        - LMS2_BB_DAC1_B1_P
        - R7
        - 2.5V
      * - 5
        - B2N
        - LMS2_BB_DAC1_B2_N
        - L7
        - 2.5V
      * - 4
        - B2P
        - LMS2_BB_DAC1_B2_P
        - M7
        - 2.5V
      * - 3
        - B3N
        - LMS2_BB_DAC1_B3_N
        - T7
        - 2.5V
      * - 2
        - B3P
        - LMS2_BB_DAC1_B3_P
        - T8
        - 2.5V
      * - 1
        - B4N
        - LMS2_BB_DAC1_B4_N
        - P8
        - 2.5V
      * - 68
        - B4P
        - LMS2_BB_DAC1_B4_P
        - R8
        - 2.5V
      * - 67
        - B5N
        - LMS2_BB_DAC1_B5_N
        - U5
        - 2.5V
      * - 66
        - B5P
        - LMS2_BB_DAC1_B5_P
        - U6
        - 2.5V
      * - 65
        - B6N
        - LMS2_BB_DAC1_B6_N
        - P5
        - 2.5V
      * - 64
        - B6P
        - LMS2_BB_DAC1_B6_P
        - P6
        - 2.5V
      * - 63
        - B7N
        - LMS2_BB_DAC1_B7_N
        - R5
        - 2.5V
      * - 62
        - B7P
        - LMS2_BB_DAC1_B7_P
        - T5
        - 2.5V
      * - 60
        - B8N
        - LMS2_BB_DAC1_B8_N
        - U1
        - 2.5V
      * - 59
        - B8P
        - LMS2_BB_DAC1_B8_P
        - U2
        - 2.5V
      * - 58
        - B9N
        - LMS2_BB_DAC1_B9_N
        - R2
        - 2.5V
      * - 57
        - B9P
        - LMS2_BB_DAC1_B9_P
        - T2
        - 2.5V
      * - 56
        - B10N
        - LMS2_BB_DAC1_B10_N
        - P1
        - 2.5V
      * - 55
        - B10P
        - LMS2_BB_DAC1_B10_P
        - R1
        - 2.5V
      * - 54
        - B11N
        - LMS2_BB_DAC1_B11_N
        - T3
        - 2.5V
      * - 53
        - B11P
        - LMS2_BB_DAC1_B11_P
        - T4
        - 2.5V
      * - 52
        - B12N
        - LMS2_BB_DAC1_B12_N
        - L4
        - 2.5V
      * - 51
        - B12P
        - LMS2_BB_DAC1_B12_P
        - M4
        - 2.5V
      * - 50
        - B13N
        - LMS2_BB_DAC1_B13_N
        - J3
        - 2.5V
      * - 49
        - B13P
        - LMS2_BB_DAC1_B13_P
        - K3
        - 2.5V
      * - 48
        - B14N
        - LMS2_BB_DAC1_B14_N
        - J1
        - 2.5V
      * - 47
        - B14P
        - LMS2_BB_DAC1_B14_P
        - K1
        - 2.5V
      * - 46
        - B15N
        - LMS2_BB_DAC1_B15_N
        - H1
        - 2.5V
      * - 45
        - B15P
        - LMS2_BB_DAC1_B15_P
        - H2
        - 2.5V
      * - 37
        - CLKN
        - LMS2_BB_DAC1_CLK_N
        - L2
        - 2.5V
      * - 38
        - CLKP
        - LMS2_BB_DAC1_CLK_P
        - M2
        - 2.5V
      * - 43
        - SELIQP
        - LMS2_BB_DAC1_SELIQ_P
        - M6
        - 2.5V
      * - 44
        - SELIQN
        - LMS2_BB_DAC1_SELIQ_N
        - M5
        - 2.5V
      * - 40
        - PD
        - LMS2_BB_DAC1_PD
        - M26
        - 3.3V

   .. tab:: LMS2 TX2 BB DAC

    .. list-table:: Table 10. 16-bit LMS2 TX2 BB DAC (IC49) digital interface
      :header-rows: 1
      :stub-columns: 1

      * - Chip pin (IC49)
        - Chip reference (IC49)
        - Schematic signal name
        - FPGA pin
        - I/O standard
      * - 9
        - B0N
        - LMS2_BB_DAC2_B0_N
        - D6
        - 2.5V
      * - 8
        - B0P
        - LMS2_BB_DAC2_B0_P
        - E6
        - 2.5V
      * - 7
        - B1N
        - LMS2_BB_DAC2_B1_N
        - G7
        - 2.5V
      * - 6
        - B1P
        - LMS2_BB_DAC2_B1_P
        - H7
        - 2.5V
      * - 5
        - B2N
        - LMS2_BB_DAC2_B2_N
        - E3
        - 2.5V
      * - 4
        - B2P
        - LMS2_BB_DAC2_B2_P
        - F3
        - 2.5V
      * - 3
        - B3N
        - LMS2_BB_DAC2_B3_N
        - K6
        - 2.5V
      * - 2
        - B3P
        - LMS2_BB_DAC2_B3_P
        - K7
        - 2.5V
      * - 1
        - B4N
        - LMS2_BB_DAC2_B4_N
        - H4
        - 2.5V
      * - 68
        - B4P
        - LMS2_BB_DAC2_B4_P
        - J4
        - 2.5V
      * - 67
        - B5N
        - LMS2_BB_DAC2_B5_N
        - E2
        - 2.5V
      * - 66
        - B5P
        - LMS2_BB_DAC2_B5_P
        - F2
        - 2.5V
      * - 65
        - B6N
        - LMS2_BB_DAC2_B6_N
        - D1
        - 2.5V
      * - 64
        - B6P
        - LMS2_BB_DAC2_B6_P
        - E1
        - 2.5V
      * - 63
        - B7N
        - LMS2_BB_DAC2_B7_N
        - B1
        - 2.5V
      * - 62
        - B7P
        - LMS2_BB_DAC2_B7_P
        - C1
        - 2.5V
      * - 60
        - B8N
        - LMS2_BB_DAC2_B8_N
        - C3
        - 2.5V
      * - 59
        - B8P
        - LMS2_BB_DAC2_B8_P
        - D3
        - 2.5V
      * - 58
        - B9N
        - LMS2_BB_DAC2_B9_N
        - A4
        - 2.5V
      * - 57
        - B9P
        - LMS2_BB_DAC2_B9_P
        - B4
        - 2.5V
      * - 56
        - B10N
        - LMS2_BB_DAC2_B10_N
        - A2
        - 2.5V
      * - 55
        - B10P
        - LMS2_BB_DAC2_B10_P
        - A3
        - 2.5V
      * - 54
        - B11N
        - LMS2_BB_DAC2_B11_N
        - A5
        - 2.5V
      * - 53
        - B11P
        - LMS2_BB_DAC2_B11_P
        - B5
        - 2.5V
      * - 52
        - B12N
        - LMS2_BB_DAC2_B12_N
        - G6
        - 2.5V
      * - 51
        - B12P
        - LMS2_BB_DAC2_B12_P
        - H6
        - 2.5V
      * - 50
        - B13N
        - LMS2_BB_DAC2_B13_N
        - F7
        - 2.5V
      * - 49
        - B13P
        - LMS2_BB_DAC2_B13_P
        - F8
        - 2.5V
      * - 48
        - B14N
        - LMS2_BB_DAC2_B14_N
        - G9
        - 2.5V
      * - 47
        - B14P
        - LMS2_BB_DAC2_B14_P
        - H9
        - 2.5V
      * - 46
        - B15N
        - LMS2_BB_DAC2_B15_N
        - G8
        - 2.5V
      * - 45
        - B15P
        - LMS2_BB_DAC2_B15_P
        - H8
        - 2.5V
      * - 37
        - CLKN
        - LMS2_BB_DAC2_CLK_N
        - D5
        - 2.5V
      * - 38
        - CLKP
        - LMS2_BB_DAC2_CLK_P
        - E5
        - 2.5V
      * - 43
        - SELIQP
        - LMS2_BB_DAC2_SELIQ_P
        - L8
        - 2.5V
      * - 44
        - SELIQN
        - LMS2_BB_DAC2_SELIQ_N
        - K8
        - 2.5V
      * - 40
        - PD
        - LMS2_BB_DAC2_PD
        - N24
        - 3.3V

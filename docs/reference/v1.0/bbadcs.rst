Baseband ADCs
#############


There are four Dual-Channel 14-Bit, 160 Msps, analog-to-digital converters (ADS4246 – IC62, IC64, IC66 and IC68). ADC analog inputs are connected to baseband RX outputs of RF transceivers #2 and #3 (IC4 and IC21). Digital output pins are connected to FPGA.

Detailed interface between ADCs and other components including ADC pins, schematic signal names, FPGA pins and FPGA I/O standards is as shown in Table 5, Table 6, Table 7 and Table 8.

.. tabs::

    .. tab:: LMS2 RX1 BB ADC

        .. list-table:: Table 5. 14-bit LMS2 RX1 BB ADC (IC62) digital interface
            :header-rows: 1
            :stub-columns: 1

            * - Chip pin (IC62)
              - Chip reference (IC62)
              - Schematic signal name
              - FPGA pin
              - I/O standard
            * - 41
              - DA0_P/DA1
              - LMS2_BB_ADC1_DA0_P
              - B20
              - 2.5V
            * - 40
              - DA0_M/DA0
              - LMS2_BB_ADC1_DA0_N
              - A20
              - 2.5V
            * - 43
              - DA2_P/DA3
              - LMS2_BB_ADC1_DA1_P
              - A17
              - 2.5V
            * - 42
              - DA2_M/DA2
              - LMS2_BB_ADC1_DA1_N
              - A18
              - 2.5V
            * - 45
              - DA4_P/DA5
              - LMS2_BB_ADC1_DA2_P
              - G17
              - 2.5V
            * - 44
              - DA4_M/DA4
              - LMS2_BB_ADC1_DA2_N
              - F17
              - 2.5V
            * - 47
              - DA6_P/DA7
              - LMS2_BB_ADC1_DA3_P
              - B19
              - 2.5V
            * - 46
              - DA6_M/DA6
              - LMS2_BB_ADC1_DA3_N
              - A19
              - 2.5V
            * - 51
              - DA8_P/DA13
              - LMS2_BB_ADC1_DA4_P
              - C17
              - 2.5V
            * - 50
              - DA8_M/DA12
              - LMS2_BB_ADC1_DA4_N
              - B17
              - 2.5V
            * - 53
              - DA10_P/DA9
              - LMS2_BB_ADC1_DA5_P
              - E16
              - 2.5V
            * - 52
              - DA10_M/DA8
              - LMS2_BB_ADC1_DA5_N
              - D16
              - 2.5V
            * - 55
              - DA12_P/DA11
              - LMS2_BB_ADC1_DA6_P
              - B22
              - 2.5V
            * - 54
              - DA12_M/DA10
              - LMS2_BB_ADC1_DA6_N
              - A22
              - 2.5V
            * - 61
              - DB0_P/DB1
              - LMS2_BB_ADC1_DB0_P
              - A23
              - 2.5V
            * - 60
              - DB0_M/DB0
              - LMS2_BB_ADC1_DB0_N
              - A24
              - 2.5V
            * - 63
              - DB2_P/DB3
              - LMS2_BB_ADC1_DB1_P
              - C26
              - 2.5V
            * - 62
              - DB2_M/DB2
              - LMS2_BB_ADC1_DB1_N
              - B26
              - 2.5V
            * - 3
              - DB4_P/DB5
              - LMS2_BB_ADC1_DB2_P
              - F18
              - 2.5V
            * - 2
              - DB4_M/DB4
              - LMS2_BB_ADC1_DB2_N
              - F19
              - 2.5V
            * - 5
              - DB6_P/DB7
              - LMS2_BB_ADC1_DB3_P
              - C21
              - 2.5V
            * - 4
              - DB6_M/DB6
              - LMS2_BB_ADC1_DB3_N
              - B21
              - 2.5V
            * - 7
              - DB8_P/DB13
              - LMS2_BB_ADC1_DB4_P
              - E21
              - 2.5V
            * - 6
              - DB8_M/DB12
              - LMS2_BB_ADC1_DB4_N
              - D21
              - 2.5V
            * - 9
              - DB10_P/DB9
              - LMS2_BB_ADC1_DB5_P
              - C24
              - 2.5V
            * - 8
              - DB10_M/DB8
              - LMS2_BB_ADC1_DB5_N
              - B24
              - 2.5V
            * - 11
              - DB12_P/DB11
              - LMS2_BB_ADC1_DB6_P
              - B25
              - 2.5V
            * - 10
              - DB12_M/DB10
              - LMS2_BB_ADC1_DB6_N
              - A25
              - 2.5V
            * - 35
              - CTRL1
              - LMS2_BB_ADC1_CTRL1
              - 
              - 
            * - 36
              - CTRL2
              - LMS2_BB_ADC1_CTRL2
              - 
              - 
            * - 34
              - CTRL3
              - LMS2_BB_ADC1_CTRL3
              - 
              - 
            * - 29
              - INP_A
              - LMS2_BB_ADC1_INA_P
              - 
              - 
            * - 30
              - INM_A
              - LMS2_BB_ADC1_INA_N
              - 
              - 
            * - 23
              - VCM
              - LMS2_BB_ADC1_VCM
              - 
              - 
            * - 57
              - CLKOUTP/CLKOUT
              - LMS2_BB_ADC1_CLKOUT_P
              - D18
              - 2.5V
            * - 56
              - CLKOUTM/UNUSED
              - LMS2_BB_ADC1_CLKOUT_N
              - C18
              - 2.5V
            * - 19
              - INP_B
              - LMS2_BB_ADC1_INB_P
              - 
              - 
            * - 20
              - INM_B
              - LMS2_BB_ADC1_INB_N
              - 
              - 
            * - 25
              - CLKP
              - LMS2_BB_ADC1_CLKC_P
              - 
              - 
            * - 26
              - CLKM
              - LMS2_BB_ADC1_CLKC_N
              - 
              - 
            * - 13
              - SCLK
              - FPGA_SPI1_SCLK
              - M16
              - 2.5V
            * - 14
              - SDATA
              - FPGA_SPI1_MOSI
              - M14
              - 2.5V
            * - 64
              - SDOUT
              - FPGA_SPI1_MISO_BB_ADC_LS
              - E22
              - 2.5V
            * - 15
              - SEN
              - FPGA_SPI1_LMS2_BB_ADC1_SS
              - C22
              - 2.5V
            * - 12
              - RESET
              - FPGA_LMS2_BB_ADC1_RESET
              - D23
              - 2.5V

    .. tab:: LMS2 RX2 BB ADC
    
        .. list-table:: Table 6. 14-bit LMS2 RX2 BB ADC (IC64) digital interface
            :header-rows: 1
            :stub-columns: 1

            * - Chip pin (IC64)
              - Chip reference (IC64)
              - Schematic signal name
              - FPGA pin
              - I/O standard
            * - 41
              - DA0_P/DA1
              - LMS2_BB_ADC2_DA0_P
              - E25
              - 2.5V
            * - 40
              - DA0_M/DA0
              - LMS2_BB_ADC2_DA0_N
              - D25
              - 2.5V
            * - 43
              - DA2_P/DA3
              - LMS2_BB_ADC2_DA1_P
              - K16
              - 2.5V
            * - 42
              - DA2_M/DA2
              - LMS2_BB_ADC2_DA1_N
              - K17
              - 2.5V
            * - 45
              - DA4_P/DA5
              - LMS2_BB_ADC2_DA2_P
              - F23
              - 2.5V
            * - 44
              - DA4_M/DA4
              - LMS2_BB_ADC2_DA2_N
              - E23
              - 2.5V
            * - 47
              - DA6_P/DA7
              - LMS2_BB_ADC2_DA3_P
              - J19
              - 2.5V
            * - 46
              - DA6_M/DA6
              - LMS2_BB_ADC2_DA3_N
              - H19
              - 2.5V
            * - 51
              - DA8_P/DA13
              - LMS2_BB_ADC2_DA4_P
              - G24
              - 2.5V
            * - 50
              - DA8_M/DA12
              - LMS2_BB_ADC2_DA4_N
              - F24
              - 2.5V
            * - 53
              - DA10_P/DA9
              - LMS2_BB_ADC2_DA5_P
              - E26
              - 2.5V
            * - 52
              - DA10_M/DA8
              - LMS2_BB_ADC2_DA5_N
              - D26
              - 2.5V
            * - 55
              - DA12_P/DA11
              - LMS2_BB_ADC2_DA6_P
              - G25
              - 2.5V
            * - 54
              - DA12_M/DA10
              - LMS2_BB_ADC2_DA6_N
              - F25
              - 2.5V
            * - 61
              - DB0_P/DB1
              - LMS2_BB_ADC2_DB0_P
              - H26
              - 2.5V
            * - 60
              - DB0_M/DB0
              - LMS2_BB_ADC2_DB0_N
              - G26
              - 2.5V
            * - 63
              - DB2_P/DB3
              - LMS2_BB_ADC2_DB1_P
              - J25
              - 2.5V
            * - 62
              - DB2_M/DB2
              - LMS2_BB_ADC2_DB1_N
              - J26
              - 2.5V
            * - 3
              - DB4_P/DB5
              - LMS2_BB_ADC2_DB2_P
              - J24
              - 2.5V
            * - 2
              - DB4_M/DB4
              - LMS2_BB_ADC2_DB2_N
              - H24
              - 2.5V
            * - 5
              - DB6_P/DB7
              - LMS2_BB_ADC2_DB3_P
              - J18
              - 2.5V
            * - 4
              - DB6_M/DB6
              - LMS2_BB_ADC2_DB3_N
              - H18
              - 2.5V
            * - 7
              - DB8_P/DB13
              - LMS2_BB_ADC2_DB4_P
              - K20
              - 2.5V
            * - 6
              - DB8_M/DB12
              - LMS2_BB_ADC2_DB4_N
              - J20
              - 2.5V
            * - 9
              - DB10_P/DB9
              - LMS2_BB_ADC2_DB5_P
              - G22
              - 2.5V
            * - 8
              - DB10_M/DB8
              - LMS2_BB_ADC2_DB5_N
              - F22
              - 2.5V
            * - 11
              - DB12_P/DB11
              - LMS2_BB_ADC2_DB6_P
              - L17
              - 2.5V
            * - 10
              - DB12_M/DB10
              - LMS2_BB_ADC2_DB6_N
              - L18
              - 2.5V
            * - 35
              - CTRL1
              - LMS2_BB_ADC2_CTRL1
              - 
              - 
            * - 36
              - CTRL2
              - LMS2_BB_ADC2_CTRL2
              - 
              - 
            * - 34
              - CTRL3
              - LMS2_BB_ADC2_CTRL3
              - 
              - 
            * - 29
              - INP_A
              - LMS2_BB_ADC2_INA_P
              - 
              - 
            * - 30
              - INM_A
              - LMS2_BB_ADC2_INA_N
              - 
              - 
            * - 23
              - VCM
              - LMS2_BB_ADC2_VCM
              - 
              - 
            * - 57
              - CLKOUTP/CLKOUT
              - LMS2_BB_ADC2_CLKOUT_P
              - K21
              - 2.5V
            * - 56
              - CLKOUTM/UNUSED
              - LMS2_BB_ADC2_CLKOUT_N
              - J21
              - 2.5V
            * - 19
              - INP_B
              - LMS2_BB_ADC2_INB_P
              - 
              - 
            * - 20
              - INM_B
              - LMS2_BB_ADC2_INB_N
              - 
              - 
            * - 25
              - CLKP
              - LMS2_BB_ADC2_CLKC_P
              - 
              - 
            * - 26
              - CLKM
              - LMS2_BB_ADC2_CLKC_N
              - 
              - 
            * - 13
              - SCLK
              - FPGA_SPI1_SCLK
              - M16
              - 2.5V
            * - 14
              - SDATA
              - FPGA_SPI1_MOSI
              - M14
              - 2.5V
            * - 64
              - SDOUT
              - FPGA_SPI1_MISO_BB_ADC_LS
              - E22
              - 2.5V
            * - 15
              - SEN
              - FPGA_SPI1_LMS2_BB_ADC2_SS
              - K22
              - 2.5V
            * - 12
              - RESET
              - FPGA_LMS2_BB_ADC2_RESET
              - K23
              - 2.5V

    .. tab:: LMS3 RX1 BB ADC

        .. list-table:: Table 7. 14-bit LMS3 RX1 BB ADC (IC66) digital interface
            :header-rows: 1
            :stub-columns: 1

            * - Chip pin (IC66)
              - Chip reference (IC66)
              - Schematic signal name
              - FPGA pin
              - I/O standard
            * - 41
              - DA0_P/DA1
              - LMS3_BB_ADC1_DA0_P
              - AD25
              - 2.5V
            * - 40
              - DA0_M/DA0
              - LMS3_BB_ADC1_DA0_N
              - AD26
              - 2.5V
            * - 43
              - DA2_P/DA3
              - LMS3_BB_ADC1_DA1_P
              - AC22
              - 2.5V
            * - 42
              - DA2_M/DA2
              - LMS3_BB_ADC1_DA1_N
              - AC23
              - 2.5V
            * - 45
              - DA4_P/DA5
              - LMS3_BB_ADC1_DA2_P
              - AE25
              - 2.5V
            * - 44
              - DA4_M/DA4
              - LMS3_BB_ADC1_DA2_N
              - AE26
              - 2.5V
            * - 47
              - DA6_P/DA7
              - LMS3_BB_ADC1_DA3_P
              - AF24
              - 2.5V
            * - 46
              - DA6_M/DA6
              - LMS3_BB_ADC1_DA3_N
              - AF25
              - 2.5V
            * - 51
              - DA8_P/DA13
              - LMS3_BB_ADC1_DA4_P
              - AF19
              - 2.5V
            * - 50
              - DA8_M/DA12
              - LMS3_BB_ADC1_DA4_N
              - AF20
              - 2.5V
            * - 53
              - DA10_P/DA9
              - LMS3_BB_ADC1_DA5_P
              - AE18
              - 2.5V
            * - 52
              - DA10_M/DA8
              - LMS3_BB_ADC1_DA5_N
              - AF18
              - 2.5V
            * - 55
              - DA12_P/DA11
              - LMS3_BB_ADC1_DA6_P
              - AE17
              - 2.5V
            * - 54
              - DA12_M/DA10
              - LMS3_BB_ADC1_DA6_N
              - AF17
              - 2.5V
            * - 61
              - DB0_P/DB1
              - LMS3_BB_ADC1_DB0_P
              - AC17
              - 2.5V
            * - 60
              - DB0_M/DB0
              - LMS3_BB_ADC1_DB0_N
              - AD17
              - 2.5V
            * - 63
              - DB2_P/DB3
              - LMS3_BB_ADC1_DB1_P
              - Y16
              - 2.5V
            * - 62
              - DB2_M/DB2
              - LMS3_BB_ADC1_DB1_N
              - Y17
              - 2.5V
            * - 3
              - DB4_P/DB5
              - LMS3_BB_ADC1_DB2_P
              - Y18
              - 2.5V
            * - 2
              - DB4_M/DB4
              - LMS3_BB_ADC1_DB2_N
              - AA18
              - 2.5V
            * - 5
              - DB6_P/DB7
              - LMS3_BB_ADC1_DB3_P
              - AD20
              - 2.5V
            * - 4
              - DB6_M/DB6
              - LMS3_BB_ADC1_DB3_N
              - AE20
              - 2.5V
            * - 7
              - DB8_P/DB13
              - LMS3_BB_ADC1_DB4_P
              - AD21
              - 2.5V
            * - 6
              - DB8_M/DB12
              - LMS3_BB_ADC1_DB4_N
              - AE21
              - 2.5V
            * - 9
              - DB10_P/DB9
              - LMS3_BB_ADC1_DB5_P
              - AE22
              - 2.5V
            * - 8
              - DB10_M/DB8
              - LMS3_BB_ADC1_DB5_N
              - AF22
              - 2.5V
            * - 11
              - DB12_P/DB11
              - LMS3_BB_ADC1_DB6_P
              - AE23
              - 2.5V
            * - 10
              - DB12_M/DB10
              - LMS3_BB_ADC1_DB6_N
              - AF23
              - 2.5V
            * - 35
              - CTRL1
              - LMS3_BB_ADC1_CTRL1
              - 
              - 
            * - 36
              - CTRL2
              - LMS3_BB_ADC1_CTRL2
              - 
              - 
            * - 34
              - CTRL3
              - LMS3_BB_ADC1_CTRL3
              - 
              - 
            * - 29
              - INP_A
              - LMS3_BB_ADC1_INA_P
              - 
              - 
            * - 30
              - INM_A
              - LMS3_BB_ADC1_INA_N
              - 
              - 
            * - 23
              - VCM
              - LMS3_BB_ADC1_VCM
              - 
              - 
            * - 57
              - CLKOUTP/CLKOUT
              - LMS3_BB_ADC1_CLKOUT_P
              - AA20
              - 2.5V
            * - 56
              - CLKOUTM/UNUSED
              - LMS3_BB_ADC1_CLKOUT_N
              - AB20
              - 2.5V
            * - 19
              - INP_B
              - LMS3_BB_ADC1_INB_P
              - 
              - 
            * - 20
              - INM_B
              - LMS3_BB_ADC1_INB_N
              - 
              - 
            * - 25
              - CLKP
              - LMS3_BB_ADC1_CLKC_P
              - 
              - 
            * - 26
              - CLKM
              - LMS3_BB_ADC1_CLKC_N
              - 
              - 
            * - 13
              - SCLK
              - FPGA_SPI1_SCLK
              - M16
              - 2.5V
            * - 14
              - SDATA
              - FPGA_SPI1_MOSI
              - M14
              - 2.5V
            * - 64
              - SDOUT
              - FPGA_SPI1_MISO_BB_ADC_LS
              - E22
              - 2.5V
            * - 15
              - SEN
              - FPGA_SPI1_LMS3_BB_ADC1_SS
              - F20
              - 2.5V
            * - 12
              - RESET
              - FPGA_LMS3_BB_ADC1_RESET
              - D24
              - 2.5V

    .. tab:: LMS3 RX2 BB ADC

        .. list-table:: Table 8. 14-bit LMS3 RX2 BB ADC (IC68) digital interface
            :header-rows: 1
            :stub-columns: 1

            * - Chip pin (IC68)
              - Chip reference (IC68)
              - Schematic signal name
              - FPGA pin
              - I/O standard
            * - 41
              - DA0_P/DA1
              - LMS3_BB_ADC2_DA0_P
              - T14
              - 2.5V
            * - 40
              - DA0_M/DA0
              - LMS3_BB_ADC2_DA0_N
              - T15
              - 2.5V
            * - 43
              - DA2_P/DA3
              - LMS3_BB_ADC2_DA1_P
              - T17
              - 2.5V
            * - 42
              - DA2_M/DA2
              - LMS3_BB_ADC2_DA1_N
              - T18
              - 2.5V
            * - 45
              - DA4_P/DA5
              - LMS3_BB_ADC2_DA2_P
              - V23
              - 2.5V
            * - 44
              - DA4_M/DA4
              - LMS3_BB_ADC2_DA2_N
              - W23
              - 2.5V
            * - 47
              - DA6_P/DA7
              - LMS3_BB_ADC2_DA3_P
              - T19
              - 2.5V
            * - 46
              - DA6_M/DA6
              - LMS3_BB_ADC2_DA3_N
              - U19
              - 2.5V
            * - 51
              - DA8_P/DA13
              - LMS3_BB_ADC2_DA4_P
              - AA22
              - 2.5V
            * - 50
              - DA8_M/DA12
              - LMS3_BB_ADC2_DA4_N
              - AA23
              - 2.5V
            * - 53
              - DA10_P/DA9
              - LMS3_BB_ADC2_DA5_P
              - U25
              - 2.5V
            * - 52
              - DA10_M/DA8
              - LMS3_BB_ADC2_DA5_N
              - U26
              - 2.5V
            * - 55
              - DA12_P/DA11
              - LMS3_BB_ADC2_DA6_P
              - V26
              - 2.5V
            * - 54
              - DA12_M/DA10
              - LMS3_BB_ADC2_DA6_N
              - W26
              - 2.5V
            * - 61
              - DB0_P/DB1
              - LMS3_BB_ADC2_DB0_P
              - AB26
              - 2.5V
            * - 60
              - DB0_M/DB0
              - LMS3_BB_ADC2_DB0_N
              - AC26
              - 2.5V
            * - 63
              - DB2_P/DB3
              - LMS3_BB_ADC2_DB1_P
              - AA24
              - 2.5V
            * - 62
              - DB2_M/DB2
              - LMS3_BB_ADC2_DB1_N
              - AB25
              - 2.5V
            * - 3
              - DB4_P/DB5
              - LMS3_BB_ADC2_DB2_P
              - W20
              - 2.5V
            * - 2
              - DB4_M/DB4
              - LMS3_BB_ADC2_DB2_N
              - Y20
              - 2.5V
            * - 5
              - DB6_P/DB7
              - LMS3_BB_ADC2_DB3_P
              - AB24
              - 2.5V
            * - 4
              - DB6_M/DB6
              - LMS3_BB_ADC2_DB3_N
              - AC24
              - 2.5V
            * - 7
              - DB8_P/DB13
              - LMS3_BB_ADC2_DB4_P
              - V19
              - 2.5V
            * - 6
              - DB8_M/DB12
              - LMS3_BB_ADC2_DB4_N
              - W19
              - 2.5V
            * - 9
              - DB10_P/DB9
              - LMS3_BB_ADC2_DB5_P
              - Y25
              - 2.5V
            * - 8
              - DB10_M/DB8
              - LMS3_BB_ADC2_DB5_N
              - AA25
              - 2.5V
            * - 11
              - DB12_P/DB11
              - LMS3_BB_ADC2_DB6_P
              - W25
              - 2.5V
            * - 10
              - DB12_M/DB10
              - LMS3_BB_ADC2_DB6_N
              - Y26
              - 2.5V
            * - 35
              - CTRL1
              - LMS3_BB_ADC2_CTRL1
              - 
              - 
            * - 36
              - CTRL2
              - LMS3_BB_ADC2_CTRL2
              - 
              - 
            * - 34
              - CTRL3
              - LMS3_BB_ADC2_CTRL3
              - 
              - 
            * - 29
              - INP_A
              - LMS3_BB_ADC2_INA_P
              - 
              - 
            * - 30
              - INM_A
              - LMS3_BB_ADC2_INA_N
              - 
              - 
            * - 23
              - VCM
              - LMS3_BB_ADC2_VCM
              - 
              - 
            * - 57
              - CLKOUTP/CLKOUT
              - LMS3_BB_ADC2_CLKOUT_P
              - U22
              - 2.5V
            * - 56
              - CLKOUTM/UNUSED
              - LMS3_BB_ADC2_CLKOUT_N
              - V22
              - 2.5V
            * - 19
              - INP_B
              - LMS3_BB_ADC2_INB_P
              - 
              - 
            * - 20
              - INM_B
              - LMS3_BB_ADC2_INB_N
              - 
              - 
            * - 25
              - CLKP
              - LMS3_BB_ADC2_CLKC_P
              - 
              - 
            * - 26
              - CLKM
              - LMS3_BB_ADC2_CLKC_N
              - 
              - 
            * - 13
              - SCLK
              - FPGA_SPI1_SCLK
              - M16
              - 2.5V
            * - 14
              - SDATA
              - FPGA_SPI1_MOSI
              - M14
              - 2.5V
            * - 64
              - SDOUT
              - FPGA_SPI1_MISO_BB_ADC_LS
              - E22
              - 2.5V
            * - 15
              - SEN
              - FPGA_SPI1_LMS3_BB_ADC2_SS
              - E20
              - 2.5V
            * - 12
              - RESET
              - FPGA_LMS3_BB_ADC2_RESET
              - D20
              - 2.5V

    
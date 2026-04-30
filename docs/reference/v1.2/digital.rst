RF Transceiver Digital
######################

There are three LMS7002M field programmable RF transceiver ICs (LMS7002M #1 - IC1, LMS7002M #2 – IC3 and LMS7002M #3 – IC5), interface signals can be acknowledged by corresponding prefixes LMSx_*, where x can be 1, 2 or 3. For example LMS1_* signals belongs to IC1, LMS2_* belongs to IC3 and LMS3_* belongs to IC5. 

The `LMS7002M`_ digital interface and control signals are described below.

Digital Interface
*****************

 LMS7002M (IC1) is using data bus LMS1_DIQ1_D[11:0] and LMS1_DIQ2_D[11:0], LMS1_ENABLE_IQSEL1 and LMS1_ENABLE_IQSEL2, LMS1_FCLK1 and LMS1_FCLK2, LMS1_MCLK1 and LMS1_MCLK2 signals to transfer data to/from FPGA. Indexes 1 and 2 indicate transceiver digital data PORT-1 or PORT-2. Any of these ports can be used to transmit or receive data. By default, PORT-1 is selected as receive port and PORT-2 is selected as transmit port. The FCLK# is input clock and MCLK# is output clock for LMS7002M transceiver. TXNRX signals sets ports directions. For LMS7002M interface timing details refer to LMS7002M transceiver datasheet page 12-13 [`link <https://limemicro.com/app/uploads/2017/07/LMS7002M-Data-Sheet-v3.1r00.pdf>`__]

Control
*******

These signals are used for the following functions within the LMS7002 RFIC:

 * MSx_RXEN, LMSx_TXEN – receiver and transmitter enable/disable signals.
 * LMS_RESET – LMS7002M reset signal.
 * LMS7002M transceiver is configured via 4-wire SPI interface; FPGA_SPI0_SCLK, FPGA_SPI0_MOSI, FPGA_SPI0_LMSx_MISO, FPGA_SPI0_LMSx_SS. The SPI interface is controlled from FPGA.
 * LMS EEPROM are connected to this interface.

LMS7002M Pins
*************

.. tabs::

  .. tab:: LMS7002M#1 Pins

    .. list-table:: Table 2. RF transceiver (LMS7002M#1 IC1) digital interface pins
      :stub-columns: 1
      :header-rows: 1

      * - Chip pin (IC1)
        - Chip reference (IC1)
        - Schematic signal name
        - FPGA pin
        - FPGA I/O standard
        - Comments
      * - E5
        - xoscin_tx
        - LMS1_TxPLL_CLK
        - 
        - 
        - Connected to clock buffer
      * - AM24
        - xoscin_rx
        - LMS1_RxPLL_CLK
        - 
        - 
        - Connected to clock buffer
      * - E27
        - RESET
        - LMS1_RESET
        - V1
        - 2.5V/3.3V
        - 
      * - U29
        - TXEN
        - LMS1_TXEN
        - V6
        - 2.5V/3.3V
        - 
      * - V34
        - RXEN
        - LMS1_RXEN
        - AE3
        - 2.5V/3.3V
        - 
      * - U33
        - CORE_LDO_EN
        - LMS1_CORE_LDO_EN
        - 
        - 2.5V/3.3V
        - 
      * - AB34
        - MCLK1
        - LMS1_MCLK1
        - AA3
        - 2.5V/3.3V
        - 
      * - AA33
        - FCLK1
        - LMS1_FCLK1
        - AB2
        - 2.5V/3.3V
        - 
      * - V32
        - TXNRX1
        - LMS1_TXNRX1
        - AF4
        - 2.5V/3.3V
        - 
      * - Y32
        - ENABLE_IQSEL1
        - LMS1_EN_IQSEL1
        - AD4
        - 2.5V/3.3V
        - 
      * - AG31
        - DIQ1_D0
        - LMS1_DIQ1_D0
        - V4
        - 2.5V/3.3V
        - 
      * - AF30
        - DIQ1_D1
        - LMS1_DIQ1_D1
        - W5
        - 2.5V/3.3V
        - 
      * - AF34
        - DIQ1_D2
        - LMS1_DIQ1_D2
        - AC6
        - 2.5V/3.3V
        - 
      * - AE31
        - DIQ1_D3
        - LMS1_DIQ1_D3
        - AB6
        - 2.5V/3.3V
        - 
      * - AD30
        - DIQ1_D4
        - LMS1_DIQ1_D4
        - W4
        - 2.5V/3.3V
        - 
      * - AC29
        - DIQ1_D5
        - LMS1_DIQ1_D5
        - AA7
        - 2.5V/3.3V
        - 
      * - AE33
        - DIQ1_D6
        - LMS1_DIQ1_D6
        - AA5
        - 2.5V/3.3V
        - 
      * - AD32
        - DIQ1_D7
        - LMS1_DIQ1_D7
        - AB5
        - 2.5V/3.3V
        - 
      * - AC31
        - DIQ1_D8
        - LMS1_DIQ1_D8
        - AE5
        - 2.5V/3.3V
        - 
      * - AC33
        - DIQ1_D9
        - LMS1_DIQ1_D9
        - AD5
        - 2.5V/3.3V
        - 
      * - AB30
        - DIQ1_D10
        - LMS1_DIQ1_D10
        - AC4
        - 2.5V/3.3V
        - 
      * - AB32
        - DIQ1_D11
        - LMS1_DIQ1_D11
        - AF5
        - 2.5V/3.3V
        - 
      * - P34
        - MCLK2
        - LMS1_MCLK2
        - AA4
        - 2.5V/3.3V
        - 
      * - R29
        - FCLK2
        - LMS1_FCLK2
        - AC3
        - 2.5V/3.3V
        - 
      * - U31
        - TXNRX2
        - LMS1_TXNRX2
        - AF3
        - 2.5V/3.3V
        - 
      * - R33
        - ENABLE_IQSEL2
        - LMS1_EN_IQSEL2
        - AE2
        - 2.5V/3.3V
        - 
      * - H30
        - DIQ2_D0
        - LMS1_DIQ2_D0
        - V2
        - 2.5V/3.3V
        - 
      * - J31
        - DIQ2_D1
        - LMS1_DIQ2_D1
        - V3
        - 2.5V/3.3V
        - 
      * - K30
        - DIQ2_D2
        - LMS1_DIQ2_D2
        - W1
        - 2.5V/3.3V
        - 
      * - K32
        - DIQ2_D3
        - LMS1_DIQ2_D3
        - Y1
        - 2.5V/3.3V
        - 
      * - L31
        - DIQ2_D4
        - LMS1_DIQ2_D4
        - AF2
        - 2.5V/3.3V
        - 
      * - K34
        - DIQ2_D5
        - LMS1_DIQ2_D5
        - Y3
        - 2.5V/3.3V
        - 
      * - M30
        - DIQ2_D6
        - LMS1_DIQ2_D6
        - AB1
        - 2.5V/3.3V
        - 
      * - M32
        - DIQ2_D7
        - LMS1_DIQ2_D7
        - Y2
        - 2.5V/3.3V
        - 
      * - N31
        - DIQ2_D8
        - LMS1_DIQ2_D8
        - AC1
        - 2.5V/3.3V
        - 
      * - N33
        - DIQ2_D9
        - LMS1_DIQ2_D9
        - W3
        - 2.5V/3.3V
        - 
      * - P30
        - DIQ2_D10
        - LMS1_DIQ2_D10
        - AE1
        - 2.5V/3.3V
        - 
      * - P32
        - DIQ2_D11
        - LMS1_DIQ2_D11
        - AD1
        - 2.5V/3.3V
        - 
      * - D28
        - SEN
        - FPGA_SPI0_LMS1_SS
        - W8
        - 2.5V/3.3V
        - SPI interface
      * - C29
        - SCLK
        - FPGA_SPI0_SCLK
        - Y6
        - 2.5V/3.3V
        - SPI interface
      * - F30
        - SDIO
        - FPGA_SPI0_MOSI
        - Y5
        - 2.5V/3.3V
        - SPI interface
      * - F28
        - SDO
        - FPGA_SPI0_LMS1_MISO
        - V8
        - 2.5V/3.3V
        - SPI interface
      * - D26
        - SDA
        - LMS1_I2C_SDA
        - 
        - 2.5V/3.3V
        - Connected to EEPROM
      * - C27
        - SCL
        - LMS1_I2C_SCL
        - 
        - 2.5V/3.3V
        - Connected to EEPROM

  .. tab:: LMS7002M#2 Pins

    .. list-table:: Table 3. RF transceiver (LMS7002M#2 IC3) digital interface pins
      :stub-columns: 1
      :header-rows: 1

      * - Chip pin (IC3)
        - Chip reference (IC3)
        - Schematic signal name
        - FPGA pin
        - FPGA I/O standard
        - Comments
      * - E5
        - xoscin_tx
        - LMS2_TxPLL_CLK
        - 
        - 
        - Connected to clock buffer
      * - AM24
        - xoscin_rx
        - LMS2_RxPLL_CLK
        - 
        - 
        - Connected to clock buffer
      * - E27
        - RESET
        - LMS2_RESET
        - V7
        - 2.5V/3.3V
        - 
      * - U29
        - TXEN
        - LMS2_TXEN
        - AA8
        - 2.5V/3.3V
        - 
      * - V34
        - RXEN
        - LMS2_RXEN
        - Y8
        - 2.5V/3.3V
        - 
      * - U33
        - CORE_LDO_EN
        - LMS2_CORE_LDO_EN
        - 
        - 2.5V/3.3V
        - 
      * - D28
        - SEN
        - FPGA_SPI0_LMS2_SS
        - AA2
        - 2.5V/3.3V
        - SPI interface
      * - C29
        - SCLK
        - FPGA_SPI0_SCLK
        - Y6
        - 2.5V/3.3V
        - SPI interface
      * - F30
        - SDIO
        - FPGA_SPI0_MOSI
        - Y5
        - 2.5V/3.3V
        - SPI interface
      * - F28
        - SDO
        - FPGA_SPI0_LMS2_MISO
        - AB4
        - 2.5V/3.3V
        - SPI interface
      * - D26
        - SDA
        - LMS2_I2C_SDA
        - 
        - 2.5V/3.3V
        - Connected to EEPROM
      * - C27
        - SCL
        - LMS2_I2C_SCL
        - 
        - 2.5V/3.3V
        - Connected to EEPROM

  .. tab:: LMS7002M#3 Pins

    .. list-table:: Table 4. RF transceiver (LMS7002M#3 IC5) digital interface pins
      :stub-columns: 1
      :header-rows: 1

      * - Chip pin (IC5)
        - Chip reference (IC5)
        - Schematic signal name
        - FPGA pin
        - FPGA I/O standard
        - Comments
      * - E5
        - xoscin_tx
        - LMS3_TxPLL_CLK
        - 
        - 
        - Connected to clock buffer
      * - AM24
        - xoscin_rx
        - LMS3_RxPLL_CLK
        - 
        - 
        - Connected to clock buffer
      * - E27
        - RESET
        - LMS3_RESET
        - W6
        - 2.5V/3.3V
        - 
      * - U29
        - TXEN
        - LMS3_TXEN
        - Y7
        - 2.5V/3.3V
        - 
      * - V34
        - RXEN
        - LMS3_RXEN
        - U7
        - 2.5V/3.3V
        - 
      * - U33
        - CORE_LDO_EN
        - LMS3_CORE_LDO_EN
        - 
        - 2.5V/3.3V
        - 
      * - D28
        - SEN
        - FPGA_SPI0_LMS3_SS
        - AC2
        - 2.5V/3.3V
        - SPI interface
      * - C29
        - SCLK
        - FPGA_SPI0_SCLK
        - Y6
        - 2.5V/3.3V
        - SPI interface
      * - F30
        - SDIO
        - FPGA_SPI0_MOSI
        - Y5
        - 2.5V/3.3V
        - SPI interface
      * - F28
        - SDO
        - FPGA_SPI0_LMS3_MISO
        - AD3
        - 2.5V/3.3V
        - SPI interface
      * - D26
        - SDA
        - LMS3_I2C_SDA
        - 
        - 2.5V/3.3V
        - Connected to EEPROM
      * - C27
        - SCL
        - LMS3_I2C_SCL
        - 
        - 2.5V/3.3V
        - Connected to EEPROM

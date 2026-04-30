Board Temperature Control
#########################

LimeSDR X3 board has integrated temperature sensor which can be used to monitor board temperature through I2C interface.

Sensor has over temperature shutdown (OS) output connected to FPGA which can be used to take actions to reduce board temperature when it rises above set limits. For example, fan will be turned on if board will heat up to 45°C and FAN will be turned off if board will cool down to 35°C as shown in Figure 11. These values can be modified.

.. figure:: /images/PCIe_5GRadio_v3.0_FanHysteresis.png
  :width: 400
  
  Figure 11: FAN control temperature hysteresis

.. list-table:: Table 17. Temperature sensor and fan pin connectio
    :header-rows: 1

    * - Schematic signal name
      - FPGA pin
      - I/O standard
      - Comment
    * - FPGA_I2C_SCL
      - N16
      - 3.3V
      - Serial Clock
    * - FPGA_I2C_SDA
      - N17
      - 3.3V
      - Data
    * - LM75_OS
      - U24
      - 2.5V
      - Overtemperature shutdown output (FPGA input)
    * - FAN_CTRL
      - U4
      - 2.5V
      - Fan control output

Fan voltage can be selected between 3.3V, 5V (default) and 12V via R186, R187 and R188 respectively as shown in Figure 12. Up to three fans can be connected to connectors: J18 (FPGA), J16 (RF) and J17 (spare).

.. figure:: /images/PCIe_5GRadio_v3.0_FanControl.png
  :width: 400
  
  Figure 12: Fan control circuit and voltage selection resistors
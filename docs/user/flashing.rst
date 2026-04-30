Flashing
########

From time to time it may be necessary to reprogram the FPGA configuration FLASH memory on the LimeSDR X3 board. This may be required when upgrading to a newer gateware version, or in case of corrupted FLASH memory.

It should usually be possible to program the LimeSDR X3 board using software only, with the device connected via PCIe interface. However, in case of corrupted FLASH memory or other issues, JTAG programming may be required.

To start with download a `pre-compiled programming file`_ (.rbf). Then proceed to use the pure software programming method described below, unless it has been determined that JTAG programming is necessary.

Software Programming
********************

This section describes how to program the FPGA configuration FLASH memory on the LimeSDR X3 board using Lime software.

Software
========

The :external+suiteng:ref:`Lime Suite NG software <index:introduction>` is required for programming the FPGA configuration FLASH memory.

Programming via the GUI
=======================

The programming options can be accessed in the :code:`limeGUI` application under Modules->Programming.

To program:

#. Set Programming mode to FPGA/FLASH.
#. Select the image .bin file you wish to use by pressing Open. 
#. Initiate programming by pressing Program.

.. figure:: /images/LimeSDR-X3_Prog_CLI.png
  :width: 600

  Figure 9: Programming via the GUI

Programming via the CLI
=======================

Programming can also be achieved using the CLI application :code:`limeFLASH` that is built alongside limeGUI.

The relevant options:

* device - to choose LimeSDR X3 type :code:`X3`.
* target - to set programming mode type :code:`FPGA/FLASH` and add location to .bin file. 

..  code-block:: shell
    :caption: Programming via the CLI

    limeFLASH -d  X3 -t FPGA/FLASH <PATH_TO_FILE/flash_programming_file.bin>
 

.. note::
  :code:`<PATH_TO_FILE/flash_programming_file.bin>` should be replaced by the actual path to your chosen .bin file

.. _pre-compiled programming file: https://github.com/myriadrf/LimeSDR-X3_GW/blob/litepcie-update/bitstream/flash_programming_file.bin






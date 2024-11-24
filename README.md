# SST-6809
MC6809 Single Board Computer

![stplus](https://github.com/KenWillmott/SST-6809/assets/17345651/b1b0577b-7dc4-4cc8-a207-0306ce1a3011)


The SST is a stand alone MC6809 computer. It is inspired by the simple MC6809 SBC designed by Grant Searle:
http://searle.x10host.com/6809/Simple6809.html
and committed to a PCB design by Jeff Tranter:
http://jefftranter.blogspot.com/2019/01/a-6809-single-board-computer.html

It can be seen that what I call the Searle-Tranter design, has the following features:
- minimal ICs employed to make a useful stand alone system
- no PAL, GAL, or other programmable support logic ("glue") IC's, instead only standard 74xx MSI logic parts
- entirely through hole, DIP IC construction consistent with a vintage design. No surface mount components at all

The SST-6809 maintains the same overall approach, while adding some improvements and enhancements. Thus it is a "Super Searle Tranter" or SST. The fundamental features are:
- fairly granular address decoding, using only 4 74xx devices and one address latch for expanded memory
- full featured expansion bus, several expansion boards are already available
- separate UART and CPU clocks, allowing the MCU to run at the maximum 2.0MHz with the same 115200 baud communications
- 512kb NVRAM provides 56kb main and 456kb random access, battery backed up storage
- 32kb EEPROM jumper and software selectable in 4kb pages.
- option to use either USB adapter power, or 5V provided at screw connector terminals

The 10cm x 10cm form factor, including standard connector and mounting locations, create a "family" of boards that can interoperate in different ways. As a very minimal board, the SST does not support all of them, however its connector will support up to about 3 standard peripheral card in the M8 family, such as the M8 game board or the M8 6522/proto board. This can be accomplished using stacking connectors. The same boards may be used as vertically mounted cards on a bus - this configuration is a work in progress, however all the current cards could be used in that configuration instead (with a different connector installed).

The first PCB (V1.0) status was "assembled and testing". The EEPROM fails, a problem with the pin assignments was found.

The second and third PCB, V2.0 and V2.1, were completed. These intermediate versions do work, but V2.0 requires wire jumpers to replace a missing trace.

The current board version, V2.2, is fully operational and has some improvements such as selectable I/O memory address, and socket compatibility of 128/512k NVRAM IC's.

Detailed information can be found at:
https://exileinparadise.com/sst-6809:top

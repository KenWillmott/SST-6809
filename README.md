# SST-6809
MC6809 Single Board Computer

<img width="502" alt="stplus" src="https://github.com/KenWillmott/SST-6809/assets/17345651/c7692e27-8ab4-494b-81dc-a0a7d3487d96">


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
- full featured expansion bus, game card is already available
- separate UART and CPU clocks, allowing the MCU to run at the maximum 2.0MHz with the same 115200 baud communications
- 512kb NVRAM provides 56kb main and 456kb random access, battery backed up storage
- 32kb EEPROM jumper and software selectable in 4kb pages.
- option to use either USB adapter power, or 5V provided at screw connector terminals

The 10cm x 10cm form factor, including standard connector and mounting locations, create a "family" of boards that can interoperate in different ways. As a very minimal board, the SST does not support all of them, however its connector will support one standard peripheral card in the M8 family, such as the M8 game board.

The current PCB status is "assembled and testing". The NVRAM and extended memory address latch pass tests. The EEPROM fails, a problem with the pin assignments has been found. Investigation and fixes are ongoing. The ACIA hasn't been tested yet, but I don't expect problems there.

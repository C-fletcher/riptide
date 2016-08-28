Jumpers & Wiring
================

.. contents::
   :backlinks: top
   :local:

Wiring
------

.. Warning::
   You will DIE if you short the batteries


Backplane Assembly
~~~~~~~~~~~~~~~~~~

#. Start with backplane on flat surface.
#. insert the boards in the card edge connectors as shown below, ensuring that the tabs are lined up properly (it wont go in the other way, but if you try it can damage the edge connector)

.. figure:: http://underwaterrov.org.ohio-state.edu/img/renders/riptide_180.png

#. line up the longer 2 rod adaptors to the bottom mounting rods and slide in part ways.
#. plug in the computer power cable to the 12 v board
#. Plug in the PDB rs232 cable into the small white connector closest to the corner.
#. Plug in the large battery connectors into the PDB.  Port is the upper connector and the stbd is the lower connector.
#. plug in the kill switch cable to the small connector on the Thruster Ctrl board, and plug in the rs-232 connection to the db-9 connector.
#. take an esc board, and look at the bottom of it, there should be a number. The motor wires are grouped together with white heat shrink that lables it 1-5, find the corresponding motor wires to the board and plug them in to the esc output, matching the heat shrink colors.  the top esc connects to the port motor wires and the lower one connects to the stbd motor wire.
#. repeat for all esc boards.
#. plug in the esc boards into the backplane, in the slots above the thruster control board.
#. slide the backplane in, untill all 4 rods are in the adaptors


USB3
----

- LORD MicroStrain IMU-3DM-GX4
- PointGrey BlackFly - Left
- PointGrey BlackFly - Right
- PointGrey BlackFly - Down

.. warning::
  Should further USB ports be required it will be necessary to connect them to header pins located somewhere on the motherboard. These are not USB3 capable?!


RS-232
------

- DB-9 Connector to something...
- DB-9 Connector to something else...
- Motherboard header to this...
- Motherboard header to that...




Jumpers
-------


JCMOS1: "Normal"

PSON1: "AT MODE"

JCASE1: "" <-- No connection.

JCOMPWR1: "+12V"
JCOMPWR2: "+12V"

JMSATASW1: "M-SATA"

JPSEL1: "DC-In: 12V"


BIOS
----

Press <ESC> or <DEL> to enter.


Boot Config
-----------

sudo nano /etc/default/grub

GRUB_CMDLINE_LINUX=”"

becomes:

GRUB_CMDLINE_LINUX=”text usbcore.usbfs_memory_mb=1000”

Uncomment:

#GRUB_TERMINAL=console

sudo update-grub

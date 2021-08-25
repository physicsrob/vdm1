The VDM-2021 is a text-based video output board for the S-100 bus.  Using the VDM-2021 you can easily output text-based video straight from an Altair 8800 or other S-100 based system. 

The VDM-2021 is electrically nearly identical to the historic VDM-1 board produced by Processor Technologies starting in 1975.

# Basic Theory of Operation
This board generates sixteen 64 character lines from data stored in 1024 bytes of on-board memory.  Alphanumeric and control characters (the full 128 upper and lower case plus control ASCII character set) are displayed in a 7 x 9 dot matrix.  The board produces composite-video output through a BNC connector.  Compatible monitors include anything capable of displaying composite video: a closed circuit television monitor, a modern LCD with composite input, or a television with an RF modulator.

Because the board is electrically nearly identical to the original VDM-1 board, almost everything contained in the original VDM-1 manual is applicable.

# Software Support
Because the interface is so simple, the VDM-1 enjoyed broad software support.  [View the software page for more information](software/index.md).

# Board
The VDM-2021 is assembled from a partial kit.

The partial kit includes:

- The VDM-2021 PCB
- Character generator ROM (either MCM6574P or MCM66740)
- 8 2102 memory chips
- 1 DM8131 bus comparator
- 1 DS8836N bus receiver
- 1 93L16 binary counter

# VDM-1 History

The VDM-1 was one of the first video cards ever made for a personal computer.  It was created in 1975 by Lee Felsenstein and sold by Processor Technologies to be used in the Altair 8800 and IMSAI 8080.

Here are some links on the history of the VDM-1:
- [VDM-1 Wikipedia](https://en.wikipedia.org/wiki/VDM-1)
- [The Social History of the VDM-1](http://www.leefelsenstein.com/?page_id=53)
- [Popular Electronics VDM-1 Review](history/popular%20electronics%20Oct%2076%20review.pdf)
- [VDM-1 Manual Rev C](history/manuals/manual%20rev%20C.pdf)


# VDM-2021 Reproduction of VDM-1
In May of 2021 I reached out to Lee Felsenstein asking him for advice on reproducing the VDM-1.  He thought it was a fine idea, but strongly suggested that if I were to undertake the project I should not simply copy the layout of the original board.  Lee has always been disappointed by the poor quality of the original board layout.  I underwent the task of capturing the original schematic in KiCad (specifically revision E of the schematic), and then proceeded to product a PCB layout based on the original schematic.

The first prototype had a few problems that were easily corrected.  I expect that the next board builds should be mostly straight forward.

# Ordering
I'm selling this board for $40 plus shipping for the bare board or $90 plus shipping for a partial kit.  [Ordering Instructions](ordering.md)

# Why build a VDM-2021?
The VDM-2021 is the only board (to my knowledge) that can be built in 2021 to provide a terminal-style text output device for an S-100 system.  The VDM-1 also has some great history.

To the best of my knowledge there are two S-100 video cards that can be built today:
- This VDM-2021
- The Dazzler-II

So why might someone want to build a VDM-2021 instead of a Dazzler-II?  In short -- they're very different cards which achieve very different goals -- you might want both!  The high level is this:  the dazzler-II creates rastered graphics, the VDM-2021 creates text; the dazzler-II uses (roughly) 80s technology, the VDM-2021 uses 70s technology.

The VDM-2021 is nearly electrically identical to the original VDM-1.  You could in theory use all of the original components from a VDM-1 to construct a VDM-2021 (not that it'd be a good idea to do that to a VDM-1!) -- the only thing you might need is a few extra capacitors.  The same schematic is used for both (ignoring a couple of bugs found in the original schematic).


# How is this board different than the original VDM-1?
1. The original VDM-1 had some layout problems which resulted in a large ribon cable jumpering one side of the board to the other.

2. The original schematic did not capture the details of the IC bypass capacitors, so the capacitor numbers and values don't map exactly 1:1.

3. A few minor bug fixes were made (relative to the revision E schematic of the original):
    - The clock divisor in IC-22 was not updated in the schematic to correctly compensate for a change in the crystal oscillator frequency.
    - The blanking circuit for the scrolling functionality needs to be connected to the inverted output ofa flip-flop rather than the non-inverted output.

4. The heatsink was replaced with a modern readily available sink.

5. A footprint for an optional BNC connector has been added.

6. The original manual contains instructions to modify the VDM-1 for a vector interupt systems.  The modifications necessary to the original involve cutting a trace and jumpering some traces.  The VDM-2021 allows this configuration without cutting traces, and the jumpers are labelled and have through holes.

Comparison matrix:

|       | Original Dazzler | Dazzler-II | Original VDM-1 | VDM-2021 |
| ----- | ---------------- | ---------- | -------------- | -------- |
| Price | $215 (kit) in 1976 | $59 for partial kit | $199 (kit) in 1975 | $90 for partial kit |
| Display Type | Raster Graphics | Raster Graphics | Text | Text |
| Resolution | Up to 64x64 | Up to 64x64 | 256x512, but text | 256x512, but text |
| Memory | Host memory + DMA | Dual port onboard memory | Multiplexed onboard memory | Multiplexed onboard memory |
| Space | Two S-100 boards | One S-100 board | One S-100 board | One S-100 board |
| IC Count | 74 ICs | 22 ICs (including 4 CPLDs) | 48 ICs | 48 ICs |
| Joystick Support | No | Yes | No | No |



## Email
Contact me at physicsrob followed by ASCII 0x40 followed by the google mail domain name.



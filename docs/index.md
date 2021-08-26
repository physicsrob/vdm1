The VDM-2021 is a text-based video output board for the S-100 bus.  Using the VDM-2021 you can easily output text-based video straight from an Altair 8800 or other S-100 based system. 

The VDM-2021 is electrically nearly identical to the historic VDM-1 board produced by Processor Technologies starting in 1975.

# Basic Theory of Operation
The VDM-2021 generates a video display containing sixteen lines of 64 character each.  The characters are directly memory mapped from ASCII data stored in 1024 bytes of on-board memory.  The board produces composite-video output through a BNC connector.  Compatible monitors include anything capable of displaying composite video: a closed circuit television monitor, a modern LCD with composite input, or a television with an RF modulator.

Because the board is electrically nearly identical to the original VDM-1 board, almost everything contained in the original VDM-1 manual is applicable.

# Software Support
Because the interface is so simple, the VDM-1 enjoyed broad software support.  [View the software page for more information](software/index.md).

# Board Assembly
The VDM-2021 is assembled from a partial kit.  The recommended approach is to [order a partial kit](ordering.md) which contains the PCB as well as hard-to-obtain components, and then order the remaining components from Jameco.  A Bill of Materials (BOM) can be found [here](https://docs.google.com/spreadsheets/d/192WKFjCJ90pev5cdcXky_RTGSZf7UaUfQrNFE1YifAw/edit?usp=sharing) which includes every jameco part number.  Jameco has a "Quick Order" form under the ordering drop down which will allow for quick entry of the BOM part numbers.  At the time of writing, the total order from Jameco is $74.55 if you have none of the parts on hand.

It is recommended that you skim through the excellent board assembly directions from the [original VDM-1 manual](history/manuals/manual%20rev%20C.pdf).

There are a few major things that are different when compared to the original assembly directions:

- The bypass capacitors have different reference identifiers.
- The location of the components are entirely different.
- There is no ribbon cable.
- The address select jumper has a different order.  The VDM-1 address select is ordered "Address Select", "GND", "X", "Y", whereas the VDM-2021 address select jumper is ordered "Address Select", "X", "Y", "GND".  Just be mindful of the silkscreen and you'll be fine.

An interactive Bill of Materials can be [found here](ibom.html).  It is highly recommended to use this as a reference during assembly.  Since the component references correspond to the original VDM-1 circuit, the references are somewhat randomly placed on the board.  The interactive BOM is a quick and easy way to find where a part goes on the board.


# VDM-1 History

The VDM-1 was one of the first video cards ever made for a personal computer.  It was created in 1975 by Lee Felsenstein and sold by Processor Technologies to be used in the Altair 8800 and IMSAI 8080.  [History of the VDM-1](history.md)

# VDM-2021 Reproduction of VDM-1
In May of 2021 I reached out to Lee Felsenstein asking him for advice on reproducing the VDM-1.  He thought it was a fine idea, but strongly suggested that if I were to undertake the project I should not simply copy the layout of the original board.  Lee has always been disappointed by the poor quality of the original board layout -- as exemplified by its ribbon cable.  I underwent the task of capturing the original schematic in KiCad (specifically revision E of the schematic) and then proceeded to produce a PCB layout based on the original schematic.

# Ordering
I'm selling this board for $40 plus shipping for the bare board or $90 plus shipping for a partial kit.  [Ordering Instructions](ordering.md)

# Why build a VDM-2021?
The VDM-2021 is the only board (to my knowledge) that can be built in 2021 to provide a terminal-style text output device for an S-100 system.  The VDM-1 also has some great [history](history.md).

To the best of my knowledge there are two S-100 video cards that can be built today:
- This VDM-2021
- The Dazzler-II

So why might someone want to build a VDM-2021 instead of a Dazzler-II?  In short -- they're very different cards which achieve very different goals -- you might want both!  The high level is this:  the dazzler-II creates rastered graphics, the VDM-2021 creates text.  [Click here](dazzler_comp.md) for a comparison between the VDM-1, VDM-2021, Dazzler, and Dazzler II.


# How is it different than the original VDM-1?
The short version is that the VDM-2021 is nearly electrically identical to the VDM-1, but with an entirely different layout.  [See here](changes.md) for a detailed comparison.


## Email
Contact me at physicsrob followed by ASCII 0x40 followed by the google mail domain name.



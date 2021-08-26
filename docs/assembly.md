
# Board Assembly
The VDM-2021 is assembled from a partial kit, which includes all of the components not readily available:

    - The VDM-2021 PCB
    - Character generator ROM (either MCM6574P or MCM66740)
    - 8 2102 memory chips (equivalent to the 91L02 or 21L02 used in the original VDM-1)
    - 1 DM8131 bus comparator
    - 1 DS8836N bus receiver
    - 1 93L16 binary counter

The remaining components can be ordered from Jameco, Mouser, or Digikey.  A Bill of Materials (BOM) can be found [here](https://docs.google.com/spreadsheets/d/192WKFjCJ90pev5cdcXky_RTGSZf7UaUfQrNFE1YifAw/edit?usp=sharing) which includes every jameco part number.  Jameco has a "Quick Order" form under the ordering drop down which will allow for quick entry of the BOM part numbers.  At the time of writing, the total order from Jameco is $74.55 if you have none of the parts on hand.

## Assembly Overview
Before beginning assembly, it is highly recommended that you skim through the excellent board assembly directions from the [original VDM-1 manual](history/manuals/manual%20rev%20C.pdf).

There are a few major things that are different when compared to the original assembly directions:

- The bypass capacitors have different reference identifiers.
- The location of the components are entirely different.
- There is no ribbon cable.
- The address select jumper has a different order.  The VDM-1 address select is ordered "Address Select", "GND", "X", "Y", whereas the VDM-2021 address select jumper is ordered "Address Select", "X", "Y", "GND".  Just be mindful of the silkscreen and you'll be fine.

An interactive Bill of Materials can be [found here](ibom.html).  It is highly recommended to use this as a reference during assembly.  Since the component references correspond to the original VDM-1 circuit, the references are somewhat randomly placed on the board.  The interactive BOM is a quick and easy way to find where a part goes on the board.



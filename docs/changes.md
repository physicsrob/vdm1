# Changes relative to VDM-1 Revision E
In general there are not many difference between the VDM-1 and the VDM-2021 other than the board layout.  I'll try to include all the difference here.

1. The original VDM-1 had some layout problems which resulted in a large ribbon cable jumpering one side of the board to the other.

2. The original schematic did not capture the details of the IC bypass capacitors, so the capacitor numbers and values don't map exactly 1:1.

3. A few minor bug fixes were made (relative to the revision E schematic of the original):
    - The clock divisor in IC-22 was not updated in the schematic to correctly compensate for a change in the crystal oscillator frequency.
    - The blanking circuit for the scrolling functionality needs to be connected to the inverted output ofa flip-flop rather than the non-inverted output.

4. The heat sink was replaced with a modern readily available sink.

5. A footprint for an optional BNC connector has been added.

6. The original manual contains instructions to modify the VDM-1 for a vector interrupt systems.  The modifications necessary to the original involve cutting a trace and jumpering some traces.  The VDM-2021 allows this configuration without cutting traces, and the jumpers are labeled and have through holes.


[Return to Main Page](index.md)

**The DMA firmware based on PCileech-FPGA(https://github.com/ufrisk/pcileech-fpga) is used for** **research and learning purposes**.

you can generate fw just change the dna id in fifo.sv to yours.

## Current status

- The BAR0 emulation has been migrated from CSI2-like behavior to a minimal NVMe-controller style register model.
- PCI config shadow space now reports an NVMe class code (`01h/08h/02h`).
- Implemented MMIO registers: `CAP`, `VS`, `INTMS/INTMC`, `CC/CSTS`, `AQA`, `ASQ`, `ACQ`, and queue-0 doorbells.
- Added byte-enable aware register writes and minimal admin-queue state progression (`SQ0TDBL`/`CQ0HDBL` + interrupt-pending behavior).

### Important limitation

This is still a **minimal emulation** (controller presence + basic register interaction). It does **not** yet implement full NVMe admin/IO command DMA data-path, persistence, or true large-capacity backing storage.

Notice:

Notice:

Notice:

after flash fw, u should install driver on main pc, then main pc -> device manager ->intel csi2 host controller -> Power Management ->uncheck "Allow this computer to turn off this device to save power" in device manager.

# Anti-Cheats

The project was not aim to cheat, just use to test the anti cheat like vgk(hasn't been dtc in the past six months until purchased by some ac stuff)

# [RF Dongle](./README.md) - Learning

The purpose of this file is to document my learning journey with
this project.

Following is a brief description of what my relevant knowledge
was before starting this project, and a list of resources I found
most useful to fill missing gaps and make progress on it.

## Starting point

Going into this project, I was familiar with fundamentals of
electronics, I was somewhat comfortable reading schematics, though
certain components were still a mystery to me (e.g. capacitors
and inductors).

I have also designed a handful of simple PCBs for custom
keyboards. These PCBs had 2 layers, and mostly use through
hole components that I assembled manually, and the components
include a development board used as a module plus mechanical
switches and diodes.

During the design of these boards I never really thought about
manufacturability, nor signal integrity, and when routing traces
there was not much thought process, besides following the
schematic and trying to make the end result look aesthetically
pleasing.

## Components

- [Decoupling capacitors - Simply put](https://www.youtube.com/watch?v=BpuCv4hfYZU)

- [Inductors and capacitors in-depth](https://www.youtube.com/watch?v=r1t0ZjD9X7A)

## Signal integrity

- [How to achieve proper grouding - Rick Hartley](https://www.youtube.com/watch?v=ySuUZEjARPY)
  Current flows in fields, not in wires. This talk helped
  building an intuition for how to route trace and place
  components to minimize interference.

## PCB / Chip Antenna

- [PCB Antenna - How to design, measure and tune](https://www.youtube.com/watch?v=x1m8G8MAeUQ)
  Goes through things to keep in mind when designing a PCB
  antenna, it explains the purpose of a matching network,
  and demonstrates the measuring and tuning of the antenna
  through changing component values in the matching network.
  A lot of antenna related concepts started clicking only
  after watching this video.

- [How to correctly place a chip antenna on your PCB](https://www.youtube.com/watch?v=F6iBKXAfC5Q)
  More design considerations for antennas, but in this case it's
  specific to chip antennas (vs. PCB antennas). These
  considerations are demonstrated with simulations.

- [Why is 50 Ohm impedance used in PCB layout](https://www.youtube.com/watch?v=4OBO760u7jg)
  Interesting explanation on why the target impedance for
  circuits is usually 50 Ohms.

- [How to design a PCB with an antenna](https://www.youtube.com/watch?v=e0eY1L77A-E)
  Summarizes the process of calculating the parameters for
  a controlled impedance line to be used as a feed for
  an antenna.

## PCB Layout

- [Your BGA and you](https://www.youtube.com/watch?v=NTrP3fDrViQ)
  Design and manufacturing considerations for the fanout of a
  ball grid array (BGA) package.

- [When to use via in pad](https://www.youtube.com/watch?v=-L-0CkH3aEk)
  Design and manufacturing considerations for using via in pad
  (instead of dog bone fanout).

- [KiCad 6 STM32 PCB Design full tutorial](https://www.youtube.com/watch?v=aVUqaB0IMh4)
  Complete walkthrough of designing a board that uses an STM32
  microcontroller, with KiCad. Really useful to get an idea of
  the workflow.

## Other

- [JLC PCB capabilities](https://jlcpcb.com/capabilities/pcb-capabilities)
  Manufacturing capabilities of JLCPCB, which I chose as the
  PCB manufacturer for this project. These capabilities paired
  with trying out different options in the quote section
  (and seeing how the changes impacted price) heavily influenced
  the final design.

- [nRF52840 Reference circuit no. 1 for QIAA aQFN73](https://docs.nordicsemi.com/bundle/ps_nrf52840/page/ref_circuitry.html#ariaid-title2)
  Reference circuit for the nRF52840 in the QIAA layout, which
  was the cheaper layout to manufacture (compared to the BGA
  version). no. 1 refers to the configuration where the
  microcontroller is powered via USB. The downloadable reference
  for the PCB layout was also super useful.

- nRF52840-DK and nRF52840-Dongle: these are the development
  boards for the nRF52840. When in doubt on where to place
  something, or what kind of components were used, I checked
  these boards for answers, while crossreferencing with the
  reference circuit from the datasheet.

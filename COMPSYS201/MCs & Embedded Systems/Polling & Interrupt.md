# Polling & Interrupt

#### Polling vs Interrupt

Polling is the process of regular checking of the desired information source
- may miss information during other calculations
- checking everything takes time
- doing this requires microcontroller to not be asleep

Interrupt: stop what you are currently doing and do something else then comeback
- allows for focusing on main task
- should only be used for high priority tasks

#### Interrupt Handler (ISR: Interrupt Service Routine)

Subroutine that handles the Interrupt
Should: 
- only use voltatile variables that are global
-  be small

#### Interrupt Vectors

Each Interrupt is assigned a number
- interrupts with the lower numbers have higher priority

Interrupt vectors are addresses that inform the processor where to find the Interrupt handler

#### AVR Interrupts
Interrupts on AVR MC
- External: `INT0`, `INT1`; change
- GPIO change
- Watchdog time-out, resets microcontroller after certain time (can reset timer in program)
- ADC: notifies completed Analog to Digital Conversion 
- Serial interface: notifies important events on transmission and reception of serial data

#### External Interrupts

INT0, INT1
PCINT[0:23]
PCI0 will trigger if PCINT[7:0] changes
PCI1 will trigger if PCINT[14:8] changes
PCI2 will trigger if PCINT[23:16] changes

Bit 7 in SREG is global interrupt enable which enables the handling of interrupts

INTx changes INTFx to 1

`sei()` enables global interrupt

`PCIEx` enables `PCIx`
`PCICR` contains `PCIEx` on the xth bit
`PCIFR` contains `PCIFx` on the xth bit, this flag enables when the corresponding `PCIx` happens.

`ISR(<interrupt>_vec) {}`

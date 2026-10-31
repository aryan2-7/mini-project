# Audio Amplifier using TDA2030

**Group:** [Aryan Khatri, Pratisthit Khaniya, Shreeshant Pandit Jha, Dinanka Koirala, Shresh Khanal] | **Course:** EEEG 211 | **Instructor:** Prashant Kandel

## Idea / Background
- Audio amplifier takes a weak signal (phone, laptop, mic) and boosts it enough to drive a speaker
- Uses stuff from the course: amplification, biasing, coupling/bypass capacitors, power supply, filtering
- Practical and easy to demo (play music in the viva)

## Problem Statement
- Phone/laptop output is too weak to drive a proper speaker
- We want to build a small power amplifier ourselves that is loud and clean enough

## Objectives
- Build a working audio amplifier around the TDA2030
- Target around 12W to 15W continuous into a 4ohm speaker (8ohm can be used for lower power fallback)
- Gain of about ~33V/V (30dB) so a phone's output can drive it
- Decent frequency response (20 Hz to 20 kHz) with low distortion
- Simulate first, then build, then compare results
- Bonus: turn it into a PCB in KiCad

## Specs (rough)
- **Input:** line level from 3.5 mm jack
- **Supply:** about 28 to 30V DC, 1.2A or more
- **Output:** 4ohm speaker rated 15W or more
- **Not included:** tone control, Bluetooth, etc. (maybe later if time)

## Block Diagram
- Input jack → input coupling cap + volume pot → TDA2030 (feedback resistors set gain) → output coupling cap / Zobel network → speaker
- Power supply: transformer → rectifier → filter caps → amplifier

## Components
- TDA2030, resistors, electrolytic caps, ceramic caps, diodes, volume pot, heatsink for the IC, transformer/adapter, speaker, matrix board or breadboard
- **Software:** LTspice / Multisim for simulation, KiCad for PCB

## Simulation and Testing Plan
- Simulate gain, frequency response, and distortion
- On hardware, measure output with a function generator + oscilloscope, then do a listening test with real music
- Compare simulation and real results in the report

## Expected Outcome
- Working amplifier prototype, simulation results, report, (PCB if time)

## Timeline (rough)
Finalize idea, get approval
Simulation
Build on breadboard / matrix board
Testing and fixes
PCB (optional) and report 


## Budget
Around [Rs. ___] total

## Risks
- IC gets hot, so we need a proper heatsink around 300cm^2
- Noise/hum from the power supply, so use good filtering and short wires
- Oscillation, so add the recommended capacitors / Zobel network
- Supply too weak, so size the transformer properly

## Note on the IC
It's an IC-based design, but we build the circuit around it ourselves (feedback network, biasing, filtering, power supply).

## References
- Electromaker TDA2030 25W audio amplifier project page
- TDA2030 datasheet (ST)
- GreatScott on Youtube

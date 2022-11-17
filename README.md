# Configurable SR

This is an SR flip-flop with universal gates at each input.  
A D flip-flop is also connected to the outputs of the universal gates for additional flexibility.
The Q and Q-bar outputs of the SR and D flip-flops are all available at output pins. 

The outputs of the universal gates, as well as the intermediate signals from the 2:1 muxs feeding the xor gates are also available at the outputs.
This allows the circuit to be used as two independent universal gates, or multiplexers with both inverting and non-inverting outputs.

## Circuit Diagram

![circuit diagram](configurable-sr.drawio.svg)

## Universal Gates

The universal gates are essentially the same circuit found in the 1G99 without the tri-state output.  
This allows all the following functions to be implemented:

![input configurations](input-configurations.drawio.svg)

With the multiplexer output driven to a pin, the circuit can also implement a multiplexer with both inverting and non-inverting outputs:

![dual-out-mux](dual-out-mux.drawio.svg)


## Contact

You can find me [online here](https://greg.steiert.net/)

***

![](../../workflows/gds/badge.svg) ![](../../workflows/docs/badge.svg)

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

## Flip-Flops

The two universal gates are connected to an SR flip-flop and a D-type flip-flop as show below:

![flip-flops](flip-flops.drawio.svg)

I'm not aware of many uses for a D flip-flop connected in parallel with a SR flip-flop.  I expect only one to be connected at a time.  Let me know if you come up with a use for both flip-flops simultaneously.  

The universal gates on the flip-flop inputs allow for creating more feature rich flip-flops like this T-type flip-flop with clock enable:

![t-type flip-flop](t-type.drawio.svg)

The reason I included a SR flip-flop, and my primary purpose for this circuit is to implement the logic to drive a cyclops light from left and right tail light signals that you would find on a trailer connector.  This circuit needs to turn on when both lights are on, and stay on until both are off, so that it does not blink with a turn signal.  The cyclops configuration for the SR flip-flop is here:

![cyclops implementation](cyclops.drawio.svg)


## Contact

You can find me [online here](https://greg.steiert.net/)

***

![](../../workflows/gds/badge.svg) ![](../../workflows/docs/badge.svg)

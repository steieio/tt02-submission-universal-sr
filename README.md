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

***

![](../../workflows/gds/badge.svg) ![](../../workflows/docs/badge.svg)

# What is Tiny Tapeout?

TinyTapeout is an educational project that aims to make it easier and cheaper than ever to get your digital designs manufactured on a real chip!

Go to https://tinytapeout.com for instructions!

## How to change the Wokwi project

Edit the [info.yaml](info.yaml) and change the wokwi_id to match your project.

## How to enable the GitHub actions to build the ASIC files

Please see the instructions for:

* [Enabling GitHub Actions](https://tinytapeout.com/faq/#when-i-commit-my-change-the-gds-action-isnt-running)
* [Enabling GitHub Pages](https://tinytapeout.com/faq/#my-github-action-is-failing-on-the-pages-part)

## How does it work?

When you edit the info.yaml to choose a different ID, the [GitHub Action](.github/workflows/gds.yaml) will fetch the digital netlist of your design from Wokwi.

After that, the action uses the open source ASIC tool called [OpenLane](https://www.zerotoasiccourse.com/terminology/openlane/) to build the files needed to fabricate an ASIC.

## Resources

* [FAQ](https://tinytapeout.com/faq/)
* [Digital design lessons](https://tinytapeout.com/digital_design/)
* [Join the community](https://discord.gg/rPK2nSjxy8)

## What next?

* Share your GDS on Twitter, tag it [#tinytapeout](https://twitter.com/hashtag/tinytapeout?src=hashtag_click) and [link me](https://twitter.com/matthewvenn)!

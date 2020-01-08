# Nonlinear Circuits
These are ports of the incredible Nonlinear Circuits Eurorack modules for [VCV Rack](https://vcvrack.com/). Many of these ports were originally made for Euro Reakt for Reaktor 6, and were created by analyzing real hardware builds.

Modules by [Nonlinear Circuits](https://www.nonlinearcircuits.com/) are typically smaller modules that focus on surprises through simple interaction. They are highly recommended as starter DIY Eurorack builds.

Recommended viewing: [Interview with Nonlinear Circuits by Music Thing Modular](https://www.youtube.com/watch?v=NxVBmO7cJFA)

## Credits
- Original Design: [Andrew Fitch](https://www.nonlinearcircuits.com/)
- Code: [Michael Hetrick](https://mhetrick.com/)
- Double Neuron Panel: [Papernoise](https://www.papernoise.net/) (Hannes Pasqualini)
- Panel Porting: Jason Wehmhoener

## Modules

### Double Neuron
This is based off of a special panel designed by [Papernoise and sold by Magpie Modular](https://magpie-modular.myshopify.com/collections/all-panels/products/nonlinear-circuits-dual-neuron?variant=31017400707). It is a panel meant to house two separate Neuron/Diff-Rect modules. Why two? Well, they're easy to build and they interact in a spectacular way.

[Video intro by Modular Addict](https://www.youtube.com/watch?v=2T5mkvdE-fc)

The top-half is a "Neuron" circuit. This is a three-input mixer that runs into a half-wave rectifier and comparator. The comparator's bipolar output is summed with the rectified signal. SENSE adds a positive DC signal to the mix, while RESPONSE affects the magnitude of the comparator's output. The values of the knobs here are accurate to the original hardware, and are not bipolar like the Euro Reakt port.

The Diff-Rect (Difference Rectifier) is another creative mixer. The two "+" inputs are summed together, and the two "-" inputs are summed together. The "-" mix is then subtracted from the "+" mix. If the result is positive, it goes out the "+" output, otherwise it goes out the "-" output.

If this seems complicated, just experiment! These modules were designed for fun, not for rigorous analysis.

![Double Neuron](./neuron.png)

### Squid Axon
This is a three channel mixer connected to a shift register of sorts. Unlike most shift registers, OUT 1 holds its value until OUT 4 has received its value. There are two feedback controls. OUT 4 is normalled to IN 3, so if nothing is connected to IN 3, it is a feedback input. The other feedback control is nonlinear and always available. This feedback path runs through a diode simulator, so it behaves much differently than the other feedback control.

To use: plug any signal into the CLOCK input. Whenever this signals goes above 1V, a clock will fire. Plug any other signals into IN 1 and IN 2. Keep IN 3 unplugged if you want to use the regular FEEDBACK control.

### Coming Soon
- BOOLs
- 8-Bit Cipher
- Divine CMOS
- Numberwang
- Segue
- Let’s Splosh
- GENiE
- 1050 MixSeq
- 32:1
- Router
- Divide and Conquer
- Statues
- 4Seq
- Single Neuron/Diff-Rect
# autoeq-to-pulseeffects

I use [PulseEffects](https://github.com/wwmm/pulseeffects) to apply EQ settings from [AutoEQ](https://github.com/jaakkopasanen/AutoEq) in order to achieve a neutral sound (a "flat" frequency response). I grew tired of manually dragging all the sliders in the GUI so I created this tool to automate the process.

The shell script `import_eq` will convert an EQ text file such as [this one](https://github.com/jaakkopasanen/AutoEq/blob/master/results/innerfidelity/sbaf-serious/Superlux%20HD%20668B/Superlux%20HD%20668B%20ParametricEQ.txt) for the Superlux 668B into a PulseEffects-compatible json-formatted string. 

The output json-formatted string can then be pasted into the `equalizer` section of a PulseEffects preset at `~/config/PulseEffects/output/*.json`. 

Remember to also apply the correct preamp setting; those are not available in the text file for each headphone, they are found in the text on the "main" page for each headphone, e.g. [here](https://github.com/jaakkopasanen/AutoEq/tree/master/results/innerfidelity/sbaf-serious/Superlux%20HD%20668B) for the aforementioned Superlux 668B.

In the future I may add more tools here to further automate the process.


# autoeq-to-pulseeffects <img src="https://img.shields.io/github/license/johanengstrand/autoeq-to-pulseeffects">

>  Convert headphone EQ settings from AutoEQ to json-formatted values for PulseEffects 

I use [PulseEffects](https://github.com/wwmm/pulseeffects) to apply EQ settings from [AutoEQ](https://github.com/jaakkopasanen/AutoEq) in order to achieve a neutral sound (a "flat" frequency response). I grew tired of manually dragging all the sliders in the GUI so I created this tool to automate the process.

The very simple shell script `import_eq` will convert an EQ text file such as [this one](https://github.com/jaakkopasanen/AutoEq/blob/master/results/innerfidelity/sbaf-serious/Superlux%20HD%20668B/Superlux%20HD%20668B%20ParametricEQ.txt) for the Superlux 668B into a PulseEffects-compatible json-formatted string. 

For example, save the EQ settings for the aforementioned Superlux 668B from [here](https://github.com/jaakkopasanen/AutoEq/blob/master/results/innerfidelity/sbaf-serious/Superlux%20HD%20668B/Superlux%20HD%20668B%20ParametricEQ.txt) in a file called `668Bparameq.txt`, then

``` bash
./import_eq 668Bparameq.txt
```

The output json-formatted string can then be pasted into the `equalizer` section of a PulseEffects preset at `~/.config/PulseEffects/output/*.json`. 

Remember to also apply the correct preamp setting; those are not available in the text file for each headphone, they are found in the text on the "main" page for each headphone, e.g. [here](https://github.com/jaakkopasanen/AutoEq/tree/master/results/innerfidelity/sbaf-serious/Superlux%20HD%20668B) for the aforementioned Superlux 668B.

In the future I may add more tools here to further automate the process.


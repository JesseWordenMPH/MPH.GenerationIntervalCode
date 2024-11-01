Upon reflecting, the code explanations in the zip are kind of poor. So heres some more detail.
The following document details the function of each R document.
Heatmap.[parameters] - Generates a heatmap of deviations corresponding to iterration over the two variables included.
Plotting code - Allows plotting of GI means and iterration based on initial values or induced parameter change (interventions).

Essentially the way the code works is as follows
1) SEIR model is simulation to calculate S E I R over time
2) Incidence (i) is calculated post hoc (B*S*I)
3) GI distributions are calculated for each day for SEIR and incidence data.
4) Means for these distributions are calculated.

From here, we could plot the GIs, however, since we're iterrating, we do this instead.
Note, this is kind of a black box since we are iterating, but you can iterrogate GI distributions if you just do steps 1-4.
5a) Repeat steps 1-4 for each parameter value (E.g. beta=0.5, 0.4, 0.3. etc) then plot the GI mean curves for each (Plotting)
OR
5b) Repeat steps 1-4 for each combination of parameter values. Then store points of interest during iteration (deviations), then plot these with a heatmap (HEATMAP).

Now, for the plotting code, there is also the option to iterrate based on the linear variable change code. Where we can iterrate on. 1) Initial starting parameter, timing of an induced change, magnitude of an induced change (per timestep).

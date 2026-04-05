# HyperHDR Calibration Videos
Collection of HDR/Dolby Vision LUT calibration videos with different HDR/DV nit mastering levels (original videos & source swatches can be found at : https://github.com/awawa-dev/awawa-dev.github.io/tree/master/calibration )

Contains videos for mastering at 1000nit and 4000nit respectively to cover a wider range of HDR/DV videos than the typical HDR calibration video

- If you notice DV/HDR content is oversaturated in the video grabber window with the default video provided by the HyperHDR Author try a higher npl nits calibration video. 
- These are not "one shoe fits all" calibration videos. HDR content uses static metadata but not all movies carry the same MaxCLL & MaxFALL values so realistically you need a way to find these values and switch LUTs accordingly somehow at runtime, or manually and then disable/enable HDR within HyperHDR to reload the LUT. 
- Dolby Vision content carries dynamic metadata and unless the content is displayed around ~200 nits then you need a way to find the DV metadata at runtime realistically and hotswap while the content is playing. CPM Forks of CoreELEC allow polling of this information via the JSON-RPC API (DV l1 stats for per-shot FLL information with min/max/avg nits/CD/m^2 reporting, RPU MaxCLL & MaxFALL data is also pullable to choose mastering nits)
- Your TV/Video Grabber more than likely will also apply its own tonemapping over a certain nits value, so some of the higher valued npl videos may not be needed if say your video grabber tonemaps anything above 1500 nits to 1000. You'll have to play around and experiment.
- Mainline HyperHDR is not tooled for runtime LUT hotswapping, although it is possible to do so safely.

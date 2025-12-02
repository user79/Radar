# Radar
This is a Frequency Modulated Continuous Wave (FMCW) ground penetrating radar (GPR) project aimed toward detection of land mines for humanitarian de-mining. It is based loosely on the online resources from MIT and U.C.Davis, as well as the presentation by Ferrara/Chizh/Pietrelli 2017.
* https://ocw.mit.edu/courses/res-ll-003-build-a-small-radar-system-capable-of-sensing-range-doppler-and-synthetic-aperture-radar-imaging-january-iap-2011/
* http://gpradar.eu/onewebmedia/TU1208_GPRforeducationaluse_November2017_FerraraChizhPietrelli.pdf
* https://github.com/ucdart/UCD-EEC134/
* http://dart.ece.ucdavis.edu/education/eec134.html
* http://dart.ece.ucdavis.edu/education/files/eec134-2017-2018/Team_DiodeHard3/AN_Yharo_Torres.pdf
* http://dart.ece.ucdavis.edu/education/files/eec134-2017-2018/Team_DeepSpaceAntenna/Team_DeepSpace_Antenna_Report.pdf

Here I have posted the circuit design, Eagle CAD schematic, and board layout for revision 1.

Unfortunately, in initial testing of this board with a sawtooth voltage input to produce a standard frequency sweep (and subsequent testing with discrete DC voltage inputs), the output voltage seems to be fluctuating according to some other pattern, not related to reflectors placed at varying distances from the antennas.  My initial guess is that there is a reflection (or set of reflections) from the board itself that is causing the mixing pattern, that is overshadowing any additional reflection mixing from the receive antenna.  There may be some coupling from the traces of the PCB.  The projects above used shielded coax cable to connect the various parts, and now I can see why.

Next, in summer 2023, I did some hardware testing with a different mixer (but using the same VCO from the original board). I was able to see radar action in tracking a person walking in a hallway, as shown. However, I was hitting some fundamental limits in resolution due to sampling rate and wavelength and other issues, as described in the "GPR progress summer2023.pdf" document.


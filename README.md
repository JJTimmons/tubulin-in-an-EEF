# md

* System pdb and psf after equilibration
  * used in every run (referenced in ./md/namd.conf)
* Initial coorindates, velocities, and cell dimensions
  * based on the final frame of the equilibration run
* CHARMM36 parameter files

The [electric field parameter](http://www.ks.uiuc.edu/Research/namd/2.10b1/ug/node42.html) was turned on using eFieldOn and eField

```tcl
set inputname       last_runs_name
set outputname      this_runs_name

# for the 10ns run during which the an EEF was applied
eFieldOn			yes
# for a 750 kV/cm EEF in the positive transverse direction
eField		        0.035826345822314 0.026219852770675 0.16659974853940
```

# analysis

Representative scripts for the analyses performed on the 50 ns trajectory files. The types of analyses, and the range of frames that were studied, are below:

* rmsd (full 50ns)
* rmsf (10 to 20ns)
* dipole (full 50ns)
* secondary_structure (10 to 20ns)
* dimer_curvature (10 to 20ns)
* dimer_stretch (10 to 20ns)
* h1_b2_loop (5 to 10ns) (using the last 5ns of 10ns runs over several magnitudes)
* deviation (last frame of EEF exposure)

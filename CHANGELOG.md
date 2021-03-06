## 1.2.0  – 2019-06-18

### General

- Added `--version` argument for `cobaya-run`
- Many bug-fixes for corner-cases

### Post-processing (still **BETA**: fixing conventions)

- Importance re-weighting, adding derived parameters, etc.

### Collections

- Now picklable!
- Support for skip and thin

### Samplers

#### Evaluate

- Multiple evaluations with new `N` option.

#### PolyChord

- Updated to version 1.16
- Handles speed-blocking optimally, including oversampling (manual blocking also possible).

### Likelihoods

- Reworked input/output parameters assignment (documented in DEVEL.rst)
- Removed deprecated `gaussian`

### Cosmo theories:

- Capitalization for observables now enforced! (fixed `H=H(z)` vs `h` ambiguity)
- CAMB and CLASS: fixed call without observables (just derived parameters)


## 1.1.3 – 2019-05-31

### Bugfixes (thanks Andreas Finke!)

### I/O

- Fuzzy-matching suggestions for options of blocks.


## 1.1.2 – 2019-05-02

### Bugfixes (thanks Vivian Miranda!)


## 1.1.1 – 2019-04-26

### I/O

- More liberal treatment of external Python objects, since we cannot check if they are the same between runs. So `force_reproducible` not needed any more! (deprecation notice left)


## 1.1.0 – 2019-04-12

### Python 3 compatibility – lots of fixes

### Cosmological likelihoods

#### Planck

- clik code updated for compatibility with Python 3 and modern gcc versions

### Cosmological theory codes

#### camb

- Updated to 1.0 (installing from master branch, considered stable)

#### classy

- Updated to ...
- Added P(k) interpolator

### Samplers

#### MCMC

- Manual parameter speed-blocking.

#### PolyChord

- Now installable with `cobaya-install polychord --modules [/path]`

### Cosmology input generator

- Added "citation" tab.


## 1.0.4 – 2019-04-11

### Many bugfixes -- special thanks to Guadalupe Cañas-Herrera and Vivian Miranda!

### I/O

- More permisive resuming.

### Parameterization and priors

- Made possible to fix a parameter whose only role is being an argument of a dynamically defined one.
- Likelihoods can be used in dynamical derived parameters as `chi2__[name]` (cosmological application: added automatic consolidated CMB and BAO likelihoods).

### Samplers

#### General

- Seeded runs for `evaluate`, `mcmc` and `polychord`.

#### MCMC

- Small improvements to callback functions.

#### PolyChord

- Updated to PolyChord 1.15 and using the [official GitHub repo](https://github.com/PolyChord/PolyChordLite).
- Fixed output: now -logposterior is actually that (was chi squared of posterior).
- Interfaced callback functions.

### Likelihoods

#### Created `gaussian_mixture` and added deprecation notice to `gaussian`

### Cosmological theory codes

#### General

- Added P(k) interpolator as an observable (was already available for CAMB, but not documented)

#### classy

- Updated to 2.7.1
- Added P(k) interpolator

### Cosmological likelihoods

#### DES

- Added Y1 release likelihoods [(arXiv:1708.01530)](https://arxiv.org/abs/1708.01530)

#### BICEP-Keck

- Updated to 2015 data [(arXiv:1810.05216)](https://arxiv.org/abs/1810.05216) and renamed to `bicep_keck_2015`.

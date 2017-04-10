FLUID_PLASMA
==============

[![DOI](https://zenodo.org/badge/84864291.svg)](https://zenodo.org/badge/latestdoi/84864291)

A simple Matlab class for a fluid charged species with convenience methods. 
Useful for plasma fluid models.

## Installation

Installation requires simply that you 
[download FLUID_PLASMA](https://github.com/mariomerinomartinez/fluid_plasma/archive/master.zip) 
and add the base directory (the one that contains the `+fluid_plasma` 
directory) to your Matlab path.

### Dependencies

A recent version of Matlab is needed to run the code. 
The code has been developed in Matlab 2016a Academic version. 

FLUID_PLASMA 
depends on other Matlab packages that you can download from my GitHub
account:
[utilities](https://github.com/mariomerinomartinez/utilities)
and
[constants_and_units](https://github.com/mariomerinomartinez/constants_and_units).
These packages must be installed and added to your Matlab path beforehand.

## Usage
 
The `fluid_plasma` package contains two Matlab classes:

* The `species` class models a simple plasma fluid species (can be ions or
electrons). It basically has mass, charge, and defines the thermodynamics of
the species.
* The `plasma` class stores one ion species and N electron species (to allow 
for more flexible electron models), and adds a method to compute the sonic 
velocity in the plasma.

There are three thermodynamic models implemented so far (20121026):

* cold
* isothermal
* polytropic

Usage is straight forward. Start by creating a plasma object and setting its parameters, then call one of its methods:

```Matlab
p = fluid_plasma.plasma; % Create the default plasma object
p.electrons{1}.T(1); % query the temperature of the first electron species for electron density n=1
```

### Testing

Unit tests are found in the `/test` subdirectory. After adding the package to
your Matlab path, you can run all tests by executing `runtests` from this 
subdirectory.

## Contributing

If you have any comments for improvement or 
are interested in contributing to the continued 
development of this or any of my other codes, you can contact me 
through my [personal website](http://mariomerino.uc3m.es/).
  
## License

Copyright (c) 2017 Mario Merino. The software is released as open 
source with the [MIT License](LICENSE.md).
# Batch Connect - OSC Abaqus/CAE

![GitHub Release](https://img.shields.io/github/release/osc/bc_osc_abaqus.svg)
![GitHub License](https://img.shields.io/github/license/osc/bc_osc_abaqus.svg)

A VNCSim app designed for OSC OnDemand that launches Abaqus within an Oakley
batch job.

## Prerequisites

This app requires the following software be installed on the nodes that the
batch job is intended to run on:

- [Abaqus/CAE](https://www.3ds.com/products-services/simulia/products/abaqus/abaquscae/) 6.14+
- [Lmod](https://www.tacc.utexas.edu/research-development/tacc-projects/lmod) 6.0.1+
- [Fluxbox](http://fluxbox.org/) 1.1.1+

For hardware rendering support:

- [X server](https://www.x.org/)
- [VirtualGL](http://www.virtualgl.org/) 2.3+

For VNC server support:

- [TurboVNC](http://www.turbovnc.org/) 2.1+
- [noVNC](https://github.com/novnc/noVNC) 0.6.2+

## Install

Use git to clone this app and checkout the desired branch/version you want to
use:

```sh
git clone <repo>
cd <dir>
git checkout <tag/branch>
```

You will not need to do anything beyond this as all necessary assets are
installed. You will also not need to restart this app as it isn't a Passenger
app.

To update the app you would:

```sh
cd <dir>
git fetch
git checkout <tag/branch>
```

Again, you do not need to restart the app as it isn't a Passenger app.

## Specification

### ROOT

All assets in this package look for dependencies in the specified `$ROOT`
directory. This should be set to correspond to the included `template/`
directory.

An example running the `xstartup` script included in this package:

```sh
# Path where you installed this project
BC_OSC_ABAQUS_DIR="/path/to/bc_osc_abaqus/template"

# Run the `xstartup` script with proper `$ROOT` set
ROOT="${BC_OSC_ABAQUS_DIR}" ${BC_OSC_ABAQUS_DIR}/xstartup
```

### ABAQUS_MODULE

This environment variable describes the specific Abaqus version to load. This
also assumes module support through the
[Lmod](https://www.tacc.utexas.edu/research-development/tacc-projects/lmod)
package manager is installed on the running compute node as well as the
requested module in `$ABAQUS_MODULE`.

### GPU_OFF

*Optional*

If this environment variables is set, then it will run the Abaqus GUI in
software rendering mode.

If this is unset (default), then it will use
[VirtualGL](http://www.virtualgl.org/) giving the Abaqus GUI full 3D hardware
acceleration support inside the VNC session. Note that an `Xorg` server must be
running on the compute node with a GPU for this to be supported.

## Contributing

1. Fork it ( https://github.com/OSC/bc_osc_abaqus/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request

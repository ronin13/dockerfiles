This Dockerfile builds an image with tools from linux kernel's tools/ directory.

For now, 

    * It builds the vm/ tools since others are mostly available as packages.
    * Builds and installs perf.

```
Usage:

Standard, except share the PID namespace in docker run (and mount one too if required).
```

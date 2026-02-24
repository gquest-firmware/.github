Welcome to the GQuEST firmware repository! Here you will find code related to feedback control and data acquisition for the GQuEST interferometer, in particular related to the LLCOOLJ FPGA system.

```mermaid
graph TD
    P(Filter realization) --> S[HLS]
    S --> F[Filter VHDL]
    R[Harness VHDL] --> V[Vivado project]
    F --> V
    P --> R
    V --> B[Bitfile]
    B --> H[Hardware]
    C(Coefficients) --> D[Filter driver]
    D --> H
    P --> D
```

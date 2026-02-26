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

```mermaid
graph TD
T(Continuous time filter)--gen_coefficents.py-->C(coefficients)
C--csim-->CR(C simulation results)
C--pysim-->PR(Python simulation results)
CR--verify-->V[verification]
PR--verify-->V
V--synthesis-->R(Results)
```

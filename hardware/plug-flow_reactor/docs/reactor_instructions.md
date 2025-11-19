# 🧪 Plug-flow reactor instructions

Renders of the exterior and the internal structure are available below :

[pfr_exterior.png](https://github.com/PhormsFactory/Phorms/blob/main/hardware/plug-flow_reactor/docs/pfr_render.png)

[pfr_interior.png](https://github.com/PhormsFactory/Phorms/blob/main/hardware/plug-flow_reactor/docs/pfr_interior.png)

## 📖 Description

The proposed plug-flow reactor integrates a simple S-shaped design, see the associated PNG images.
It has few parameters to consider :
- Number of channels (straight pipes per layer) : $N$
- Length of each channels : $L$
- Number of layers : $M$
- Pipe diameter : $D$
- Overall spacing between layers and channels : $S$

There are 2 layouts : reactor and heat exchanger.
Each layer $M$ has $N$ channels, all the channels per layer are connected in a linear way via 'U-turns'. 

The heat exchanger starts from the bottom layer $1$ and skips all even numbers of layers.
The top layer $L$ must be also a layer of heat exchanger, meaning that the number of layers $L$ is always an uneven number.
This way the reactor layers are always surrounded by layers of heat exchanger for better heat transfer and is represented by all even number of layers.

It is optimal to operate a continuous heat transfer with two countercurrent fluids compared with co-current fluids. Consequently, the reactor fluid enters at layer $L-1$ and exits at layer $2$ while the heat exchanger fluid enters at layer $1$ and exits at layer $L$. One could use each streams differently, the proposed layout is in accordance with good engineering practices.

Additionally, the layers are arranged in quincunx pattern, which increases the heat transfer performance and reduces the overall height of the model.

The pipe diameter $D$ and overall spacing $S$ parameters can be adjusted but cannot be too small for printing accuracy reasons.

## 🔌 Flow connectors

The reactor has 4 connectors, the symbols on top of the reactor allow to identify the correct connectors :
- Reactor inlet : &#9679;<b>(X)</b>
- Reactor outlet : <b>(X)</b>&#9679;&#9679;
- Heat exchange inlet : &#9679;<b>(Z)</b>
- Heat exchange outlet : <b>(Z)</b>&#9679;&#9679;

The connectors are based on standard M5 BSP OD threads and are 4mm deep.
For instance, one could use pneumatic PL4-M5 fittings for fluid transfer.

## 🖨️ Printing parameters

## ✏️ CAD files
The user can adjust the following variables in the model ('Varset' in FreeCAD) :

| Variable name | Symbol | Minimum recommended value |
| ------------- | ------ | ------------------------- |
| Number of channels | $N$ | 8 |
| Channel length | $L$ | 50.0 mm |
| Number of layers | $M$ | 5 |
| Reactor diameter | $D_1$ | 1.0 mm |
| Heat exchanger diameter | $D_2$ | 1.0 mm |
| Spacing | $S$ | 3.0 mm |

Reactor and heat exchanger volumes are estimated in a dedicated spreadsheet in the CAD file. The average residence time $\tau$ can be estimated knowing the global flowrate $\dot{V}$ as : $\tau = \frac{V}{\dot{V}}$.

## 🧩 STL Download (GitHub Releases)

The model contains a lot of vertices and is heavy. It is available for download on GitHub Releases, link below :

| Link | Version | Size | Status |
| ---- | ------- | ---- | ------ |
| [plug-flow_reactor.stl](https://github.com/PhormsFactory/Phorms/releases/download/v0.1.0-alpha/plug-flow_reactor.stl) | 0.1.0-alpha | 138Mb | Print OK, watertightness tests ongoing |

### Notes
Feedback from early prints to avoid leaks :
- Avoid low nozzle temperatures : 
    - Poor layer adhesion will lead to leaking units and poor pressure resistance
    - Natural finishes become less transparent and interior less visible
- Infill : print with 100% infill to improve structural resistance
- Apply teflon tape on fitting threads
- Avoid low spacing between channels and layers
- Print without pause

### Happy downloading ☀️ ! 
### Contributions and suggestions are always welcome 💬🤝.
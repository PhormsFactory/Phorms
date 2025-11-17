# Phorms
Open-source 3D printable modules for pharmaceutical applications.

##  📖 Description
Phorms project aims to provide open-source 3D printable modules for pharmaceutical or fine chemistry applications.
Converting batch processes to continuous processes or directly adapting new processes to continuous is widely supported by all regulation agencies worldwide, however investing in such expensive equipments can be a limitation for smaller laboratories.
For now, Phorms' modules are prototypes to support laboratories for quick-testing continuous processes concepts with limited costs and community-driven.
All modules can be connected to each other to build multi-steps processes.

For now, Phorms focuses on unit of operations for producing small molecules such as :
- Small tank modules for reactants and solvents
- Continuous reaction modules
- Continuous liquid/liquid extraction modules
- Continuous crystallization modules
- Continuous cyclonic separators

Avoiding non-3D-printable equipments like pumps, filtration media or valves is important for better accessibility and to limit any extra investments.
For instance, compressed gases like air or nitrogen can be used as driving force for all fluids in the process.
All modules are designed to be as analogic as possible and do not require the user to use any electronic systems for flow regulation or any other purposes.

Each module has an associated documentation which gives printing tips and setups.

## 🛠️ Choice of printing material

Ideally the selected polymer must :
- Resist to acids and bases
- Resist to solvents (organic and aqueous)
- Resist to heat
- Resist to pressure
- Be 3D-printable, preferably FDM
- Not be too expensive

PTFE is the best candidate regarding these constraints, unfortunately it cannot be 3D-printed.
The next one is PVDF, but it required very high printing temperatures that are not supported by many 3D printers. 
Also, it can potentially produce fluor-based gases which could be harmful for inexperienced users.

The most widely used polymers for FDM printing are PLA, ABS or Nylon.
They are not suitable for such applications because of their low melting point and solvent resistance.

In the end, the list could be reduced to 3 candidates : PETG, Polypropylene (PP), and Polycarbonate (PC).
Polypropylene is the polymer used for all the prototypes developed here, it can be hard to print (warping) but manageable with dedicated solutions.
Polypropylene has many advantages like good elasticity and transparency, which could be helpful for some modules.
PETG is easier to print but shows a high hardness and tends to break.
PC is also harder than Polypropylene and very difficult to print, however among those 3 polymers, it has the best resistance to all criteria listed above.

## 🖨️ Printing setup

- Printer : Prusa MK3
- Enclosure : None
- Nozzle : E3D V6 Nozzle X
- Printing sheet : Prusa PP steel sheet (mandatory to avoid warping)
- Slicer : PrusaSlicer
- Filament : FormFutura Centaur PP Natural ⌀1.75mm

While printing, Polypropylene behaves like Nylon and tends to jam the extruder.
It is advised to loosen the extruder as much as possible to avoid any issue.
The detailed printing parameters are specified for each module separately.

## 📁 Files
For each module, the following documents are provided :
- STL file
- STEP file
- FCStd file
- Instructions
- PNG renders

All 3D models are developed with FreeCAD 1.0.0, it is recommended to use ThreadProfile addon for designing fasteners.

## ✅ Available modules (Nov. 2025)
### 🧪 Plug-flow reactor
A plug-flow reactor with integrated heat exchanger without supports.

Status : 🔴 prototype under development

### 📦 Plug-flow reactor kit
A plug-flow reactor linked with 2 tanks, printable in one block without support.
Each tank flow can be regulated with a 'pinch-valve', the heat exchanger goes through all parts of the kit.

Status : 🔴 prototype under development
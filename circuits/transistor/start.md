# Transistor

## Definition

A **transistor** is a small semi-conductor that controls the flow of electricity in a circuit.

`It can let electricity pass, block it, or change how much flows, depending on the signals it receives.`


## What is a semi-conductor?

A **semiconductor** is a material that can sometimes **conduct electricity** and sometimes **block** it.

### Silicon:
<div style="display: flex; gap: 10px; width: 100%;">
  <img src="si.jpg" alt="Silicon crystal" style="width: 500px; object-fit: contain;"/>
  <img src="silicon.jpg" alt="Silicon sample" style="width: 500px; object-fit: contain;"/>
</div>

`It does not let electricity flow as easily as a metal, but it is not as resistant as an insulator.`

###### Example: **[Silicon](https://periodic-table.rsc.org/element/14/silicon)** is the most common semiconductor material used.
<!-- silicon bond image -->

## Conductivity Boosting

To increase the conductivity of semiconductors (like silicon), small amounts of other atoms are added. This process is called **doping**.

###### Result: the conductivity of semi-conductor increases.

Depending on the type of atom added, the semiconductor becomes either:

1. **n-type**: Doped with atoms that have extra electrons (such as phosphorus). These extra electrons are free to move, making the material better at conducting electricity.
2. **p-type**: Doped with atoms that have fewer electrons (such as boron). This creates "holes" (spaces where an electron could go), and these holes help carry electricity through the material.

## n-type

In n-type semiconductors, the added atoms provide extra electrons, which are the main charge carriers.

<img src="n_type.jpg" alt="Silicon crystal" style="width: 500px; object-fit: contain;"/>

## p-type

In p-type semiconductors, the added atoms create holes, and these holes act as the main charge carriers.

<img src="p_type.jpg" alt="Silicon crystal" style="width: 500px; object-fit: contain;"/>

### What actually lets the electricity flow?

In a semiconductor, electricity is carried by two things:
- **Electrons** (negatively charged particles)
- **Holes** (empty spaces where an electron could be, acting like positive charges)

In **n-type** material, electrons are the main carriers.  
In **p-type** material, holes are the main carriers.

When a voltage is applied, electrons move towards the positive side, and holes move towards the negative side, allowing current to flow through the material.

---

## Structure
What happens when we put one type of semiconductor between two others of the same type? (e.g. n-p-n or p-n-p)

If you arrange the layers as n-p-n or p-n-p, you create a structure where the middle layer is different from the outer layers.  

- In **p-n-p**, a thin n-type layer is sandwiched between two p-type layers.
- In **n-p-n**, a thin p-type layer is sandwiched between two n-type layers.

##### Example Image:
![](formation.jpg)

## Flow
There is an electrical contact at both outer layer for electricity to flow between them.

![](pathway.jpg)

This arrangement forms the basic structure of a **transistor**. The middle layer (called the **base**) controls whether electricity can flow between the outer layers (called the **emitter** and **collector**).

`electricity is meant to flow between 'source' and 'drain'.`

## Gate
Instead of an mechanical switch there is a third electrical Contact called gate.
- this gate is insulated from the semiconductor by an '**Oxide Layer**'.

![](gate.jpg)

##### In this image:
- Blue color -> Gate [ the electrical contact that works the gate ]
- Gray color -> Oxide insulator layer

## Depletion Layer:

when these are layed as shown in the pattern, they don't stay as they were. 

![](depletion_layer.jpg)

The excess electrons from n-type semi-conductors moves toward the excess holes of p-type creating a depletion layer.

`This depletion layer block the flow of electricity between **'source'** and **'drain'**`

- excess electron in n-type: which behave as a carrier of electricity in n-type
- excess holes in p-type: which behave as a carrier of electricity in p-type


---
###### **Dear curious readers, you may wonder: we made the material conductive by doping, but now we are making a pattern to stop or control the flow. Read further to know why!**
---

## Twist: Making the Layers Togglable for Electricity Conduction

The special thing about this layered structure is that the middle layer acts like a gate or switch.  
- By applying a small voltage or current to the base (middle layer), the **'Depletion Layer'** is shrinked by taking out the filled holes. this creates a pathway through pnp or npn layers.
`in this example n-p-n`

![](gate_on.jpg)

This is the key principle behind how transistors work:  
**A small signal at the base can control a large flow of electricity between the emitter and collector.**

---

`This is how transistors are made`

---

## Components
Transistors typically have three terminals:
- **Emitter** (or Source for FETs)
- **Base** (or Gate for FETs)
- **Collector** (or Drain for FETs)

Transistors can function as:
- Amplifiers (increasing signal strength)
- **Switches** (turning current on/off)

Their invention revolutionized electronics, enabling the development of smaller, faster, and more reliable devices.


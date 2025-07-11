# Logic Gates: The Brains of Digital Circuits

Welcome! In the previous section, we learned that a transistor can act as a simple electronic switch. Now, we'll see how combining these switches allows us to perform logical operations, which are the foundation of all computation.

## From Transistors to Logic Gates

By arranging transistors in specific configurations, we can create circuits that make decisions based on electrical inputs. These decision-making circuits are called **logic gates**. Each gate takes one or more binary inputs (a '1' for ON/high voltage, or a '0' for OFF/low voltage) and produces a single binary output.

---

## Fundamental Logic Gates
These are the most basic building blocks of digital logic.

- AND Gate
- OR Gate
- NOT Gate (Inverter)

## Integrated Circuits (ICs)

While you can build gates from individual transistors, it's not practical for complex devices. Instead, millions or even billions of these gates are manufactured on a single piece of silicon. This tiny, pre-packaged collection of gates is called an **Integrated Circuit (IC)**, or simply a "chip".

![A simple logic gate IC](https://upload.wikimedia.org/wikipedia/commons/thumb/5/52/74LS00.jpg/320px-74LS00.jpg)
*An example of a simple IC, the 7400, which contains four NAND gates.*

## Complex Logic Gates
These gates are combinations of the fundamental gates and are extremely common in circuit design.
- NAND Gate (NOT-AND)
- NOR Gate (NOT-OR)
- XOR Gate (Exclusive-OR)
- XNOR Gate (Exclusive-NOR)
## Universal Gates
Some gates are considered "universal" because you can create any other logic gate (AND, OR, NOT, etc.) by combining only that one type of gate. This is a very powerful concept in digital design.
- NAND Gate
- NOR Gate

### Proofing gates with Universal Gates
- NOT Gate
- OR Gate
- AND Gate
- so the others as well......

This property makes them incredibly efficient for manufacturing, as a factory can produce vast quantities of a single gate type to build any kind of complex chip.

---




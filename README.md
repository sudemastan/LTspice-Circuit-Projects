# LTspice-Circuit-Projects

# Supernode Circuit Analysis

This project provides the step-by-step mathematical solution and nodal analysis for a DC circuit containing a supernode, based on Kirchhoff's Current Law (KCL) and Kirchhoff's Voltage Law (KVL).

---

## Circuit Components

- Independent Voltage Source (V1): 14 V
- Independent Voltage Source (Vs): 6 V (between Node A and Node B)
- Resistor R1: 4 Ohm (between 14V source and Node A)
- Resistor R2: 3 Ohm (between Node A and Ground)
- Resistor R3: 2 Ohm (between Node B and Ground)
- Resistor R4: 6 Ohm (between Node B and Ground)
- Reference Node (Ground): 0 V

---

## Step-by-Step Analysis

### 1. Constraint Equation (KVL)
The 6V independent voltage source connects directly between Node A and Node B, forming a supernode:

VB - VA = 6
VB = VA + 6  --- [Equation 1]

### 2. Supernode Equation (KCL)
Sum of all currents leaving the supernode equals zero:

(VA - 14) / 4 + VA / 3 + VB / 2 + VB / 6 = 0

Multiply the entire equation by 12 to eliminate fractions:

3 * (VA - 14) + 4 * VA + 6 * VB + 2 * VB = 0
3*VA - 42 + 4*VA + 8*VB = 0
7*VA + 8*VB = 42  --- [Equation 2]

### 3. Solving the System
Substitute [Equation 1] into [Equation 2]:

7*VA + 8*(VA + 6) = 42
7*VA + 8*VA + 48 = 42
15*VA = -6
VA = -6 / 15 = -0.4 V

Calculate VB:

VB = VA + 6 = -0.4 + 6 = 5.6 V

---

## Output Values

- Voltage across the 3 Ohm resistor (v):
  v = VA = -0.4 V

- Current through the 2 Ohm resistor (i):
  i = VB / 2 = 5.6 / 2 = 2.8 A

---

## Summary of Results

- Node Voltage A (VA): -0.4 V
- Node Voltage B (VB): 5.6 V
- Branch Voltage (v across 3 Ohm): -0.4 V
- Branch Current (i through 2 Ohm): 2.8 A

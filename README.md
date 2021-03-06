# Computer Basics

## Index

1. [Basic logic gates (`AND`, `NOT`)](#section_1)
2. [Compound logic gates (`NAND`, `OR`, `XOR`)](#section_2)
3. [Binary addition](#section_3)

In this project I go through the basics of computer operations.

<a name="section_1"></a>

### 1. Basic logic gates (`AND`, `NOT`)

The `AND` and `NOT` logic gates, which can be easily created with simple circuits, are the basis for the rest of the elements addressed in this project.

`AND`

<div align="left">
  <img src="img/and_circuit.png" alt="and_circuit" height="200" width="300"/>
  <img src="img/and_truth_table.png" alt="and_truth_table" height="200" width="200"/>
</div>

`NOT`

<div align="left">
  <img src="img/not_circuit.png" alt="not_circuit" height="200" width="300"/>
  <img src="img/not_truth_table.png" alt="not_truth_table" height="200" width="200"/>
</div>

<a name="section_2"></a>

### 2. Compound logic gates (`NAND`, `OR`, `XOR`)

- `NAND` -> consists of an `AND` gate followed by a `NOT` gate.
- `OR` -> each input is passed through a `NOT` gate, and then both of them enter a `NAND` gate.
- `XOR` -> an `OR` gate and a `NAND` gate both receive both inputs in parallel. The output of these two gates enter an `AND` gate.

`NAND`

<div align="left">
  <img src="img/nand_gate.png" alt="nand_gate" height="200" width="600"/>
  <img src="img/nand_truth_table.png" alt="nand_truth_table" height="200" width="200"/>
</div>

`OR`

<div align="left">
  <img src="img/or_gate.png" alt="or_gate" height="200" width="600"/>
  <img src="img/or_truth_table.png" alt="or_truth_table" height="200" width="200"/>
</div>

`XOR`

<div align="left">
  <img src="img/xor_gate.png" alt="xor_gate" height="200" width="600"/>
  <img src="img/xor_truth_table.png" alt="xor_truth_table" height="200" width="200"/>
</div>

<a name="section_3"></a>

### 3. Binary addition

<p><strong>Addition of 1-bit numbers</strong></p>

The following diagram represents the binary sum of 2 bits (A and B). It is clear that the carry column matches perfectly the `AND` gate, and the sum column matches the `XOR` gate.

<div align="left">
  <img src="img/adder.png" alt="adder" height="200" width="600"/>
  <img src="img/adder_truth_table.png" alt="adder_truth_table" height="200" width="200"/>
</div>

However, we have to add a third input to the addition in order to take into account the carry bit and construct our adder.

<div align="left">
  <img src="img/adder_with_carry.png" alt="adder_with_carry" height="250" width="600"/>
  <img src="img/adder_with_carry_truth_table.png" alt="adder_with_carry_truth_table" height="250" width="200"/>
</div>

<small>
  <br>
</small>

<p><strong>Addition of 4-bit numbers</strong></p>

With the adder we previously created, we can easily generate a 4-bit numbers adder. This adder overflows when the sum is greater than 4 bits, and this is indicated by the carry output.

<div align="left">
  <img src="img/4_bits_addition.png" alt="4_bits_addition" height="350" width="800"/>
</div>

<small>
  <br>
</small>

<p><strong>General addition</strong></p>

We can also create a general adder for any two numbers using just the 1-bit numbers adder, as done in the `general_adder` function in `binary_addition.py`.

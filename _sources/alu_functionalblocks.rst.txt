Functional Blocks
=================

The ALU consists of four major blocks.

Shared Adder
------------

The shared adder performs:

* Addition
* Subtraction
* Signed comparisons
* Unsigned comparisons

Instead of using separate hardware for addition and subtraction,
the ALU uses a single adder.

Subtraction is performed using two's complement arithmetic:

::

   A - B = A + (~B + 1)

Shifter
--------

The shifter performs:

* Logical Left Shift (SLL)
* Logical Right Shift (SRL)
* Arithmetic Right Shift (SRA)

For left shifts, operand bits are first reversed and then shifted.

Comparator
----------

The comparator supports:

Equality Operations

* ALU_EQ
* ALU_NE

Unsigned Comparisons

* ALU_GTU
* ALU_GEU
* ALU_LTU
* ALU_LEU

Signed Comparisons

* ALU_GTS
* ALU_GES
* ALU_LTS
* ALU_LES

Result Multiplexer
------------------

The final output is selected according to operator_i.

Supported operations include:

* ADD
* SUB
* AND
* OR
* XOR
* SLL
* SRL
* SRA
* EQ
* NE
* GT
* GE
* LT
* LE
* SLT
* SLE
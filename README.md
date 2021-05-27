# RTLDesignusingVerilogwithSKY130Technology

<b>RTL design using Verilog with SKY130 Technology</b>

This is an 5-Day online workshop conducted by VLSI System Design, Banglore from 26th-30th May 2021.

Learn basics of digital design using verilog language, various RTL coding styles, typical synthesis problems faced by industry and how to solve them in Verilog

<p align="justify">Workshop intends to teach the verilog coding guidelines that results in predictable logic in Silicon. it is important to note that every verilog code is not synthesizable and even if it is , it may result in different logic depending on the coding styles used. The course details all these aspects of the Verilog HDL with theory and backed with lot of practical examples. Workshop introduces to the digital logic design using Verilog HDL . Validating the functionality of the design using Functional Simulation. Writing Test Benches to validate the functionality of the RTL design . Logic synthesis of the Functional RTL Code. Gate Level Simulation of the Synthesized Netlist.</p>

<h1>Workshop Day wise Content :</h1>
<details>

  [<h2>Day 1 - Introduction to Verilog RTL design and Synthesis</h2>](https://github.com/mdzakirhussain/RTLDesignusingVerilogwithSKY130Technology/blob/main/README.md#day-1---introduction-to-verilog-rtl-design-and-synthesis-1)
<ul>
  <li>Introduction to open-source simulator iverilog</li>
  
  <li>Labs using iverilog and <a href="http://gtkwave.sourceforge.net" onclick="window.open('http://gtkwave.sourceforge.net', '_self');">gtkwave</a></li>
<li>Introduction to Yosys and Logic synthesis</li>
<li>Labs using Yosys and Sky130 PDKs</li>
</ul>

<h2>Day 2 - Timing libs, hierarchical vs flat synthesis and efficient flop coding styles</h2>

<ul>
<li>Introduction to timing .libs</li>
<li>Hierarchical vs Flat Synthesis</li>
<li>Various Flop Coding Styles and optimization</li>
</ul>

<h2>Day 3 - Combinational and sequential optmizations</h2>

<ul>
<li>Introduction to optimizations</li>
<li>Combinational logic optimizations</li>
<li>Sequential logic optimizations</li>
<li>Sequential optimzations for unused outputs</li>
</ul>

<h2>Day 4 - GLS, blocking vs non-blocking and Synthesis-Simulation mismatch</h2>

<ul>
<li>GLS, Synthesis-Simulation mismatch and Blocking/Non-blocking statements</li>
<li>Labs on GLS and Synthesis-Simulation Mismatch</li>
<li>Labs on synth-sim mismatch for blocking statement</li>
</ul>

<h2>Day 5 - Optimization in synthesis</h2>

<ul>
<li>If Case constructs</li>
<li>Labs on "Incomplete If Case"</li>
<li>Labs on "Incomplete overlapping Case"</li>
<li>for loop and for generate</li>
<li>Labs on "for loop" and "for generate"</li>
</ul>
</details>

<h1>Day 1 - Introduction to Verilog RTL design and Synthesis</h1>

<ul>
  <li>Introduction to open-source simulator iverilog</li>
  <li>Labs using iverilog and 
 <a href="http://gtkwave.sourceforge.net" onclick="window.open('http://gtkwave.sourceforge.net', '_self');">gtkwave</a></li>
<li>Introduction to Yosys and Logic synthesis</li>
<li>Labs using Yosys and Sky130 PDKs</li>
</ul>
<h3><li>Introduction to open-source simulator iverilog</li></h3>
<p align="justify">Icarus Verilog is a Verilog simulation and synthesis tool. It operates as a compiler, compiling source code written in Verilog (IEEE-1364) into some target format. For batch simulation, the compiler can generate an intermediate form called vvp assembly. This intermediate form is executed by the ``vvp'' command. For synthesis, the compiler generates netlists in the desired format.</p>

[For more Info.](http://iverilog.icarus.com)

<h3><li>Labs using iverilog and <a href="http://gtkwave.sourceforge.net" onclick="window.open('http://gtkwave.sourceforge.net', '_blank');">gtkwave</a></li></h3>

<p align="justify">The following are the commands to simulate the design written in the verilog code. Before going to simulation let us understand some terminology, Any design for example let us consider MUX 4x1 is been described in the Verilog HDL such a described file is called design file. Now, the description of the design is correct or not we need to confirm it, that is done through testbench, testbench is also a verilog code only but that consists of majorly two things 
  <ol>
  <li> Instantiation of the design</li>
  <li> Test Vectors</li>
    </ol>

<h3><li>Introduction to <a href="http://www.clifford.at/yosys/" onclick="window.open('http://www.clifford.at/yosys/', '_blank');">Yosys</a> and Logic synthesis</li></h3>
<p align="justify">Yosys is a framework for Verilog RTL synthesis. It currently has extensive Verilog-2005 support and provides a basic set of synthesis algorithms for various application domains. Selected features and typical applications:</p>

<ol>
  <li>Process almost any synthesizable Verilog-2005 design</li>
<li>Converting Verilog to BLIF / EDIF/ BTOR / SMT-LIB / simple RTL Verilog / etc.</li>
  <li>Built-in formal methods for checking properties and equivalence</li>
  <li>Mapping to ASIC standard cell libraries (in Liberty File Format)</li>
<li>Mapping to Xilinx 7-Series and Lattice iCE40 FPGAs</li>
  <li>Foundation and/or front-end for custom flows</li>
</ol>

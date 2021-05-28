# RTLDesignusingVerilogwithSKY130Technology

<b>RTL design using Verilog with SKY130 Technology</b>

This is an 5-Day online workshop conducted by VLSI System Design, Banglore from 26th-30th May 2021.

Learn basics of digital design using verilog language, various RTL coding styles, typical synthesis problems faced by industry and how to solve them in Verilog

<p align="justify">Workshop intends to teach the verilog coding guidelines that results in predictable logic in Silicon. it is important to note that every verilog code is not synthesizable and even if it is , it may result in different logic depending on the coding styles used. The course details all these aspects of the Verilog HDL with theory and backed with lot of practical examples. Workshop introduces to the digital logic design using Verilog HDL . Validating the functionality of the design using Functional Simulation. Writing Test Benches to validate the functionality of the RTL design . Logic synthesis of the Functional RTL Code. Gate Level Simulation of the Synthesized Netlist.</p>

<h1>Workshop Day wise Content :</h1>
<details>

  [<h2>Day 1 - Introduction to Verilog RTL design and Synthesis</h2>](https://github.com/mdzakirhussain/RTLDesignusingVerilogwithSKY130Technology/blob/main/README.md#day-1---introduction-to-verilog-rtl-design-and-synthesis-1)
<ul>
  <li><a href="https://github.com/mdzakirhussain/RTLDesignusingVerilogwithSKY130Technology/blob/main/README.md#introduction-to-open-source-simulator-iverilog">Introduction to open-source simulator iverilog</a></li>
  
  <li><a href="https://github.com/mdzakirhussain/RTLDesignusingVerilogwithSKY130Technology/blob/main/README.md#labs-using-iverilog-and-gtkwave">Labs using iverilog and <a href="http://gtkwave.sourceforge.net">gtkwave</a></a></li>
<li><a href="https://github.com/mdzakirhussain/RTLDesignusingVerilogwithSKY130Technology/blob/main/README.md#introduction-to-yosys-and-logic-synthesis">Introduction to Yosys and Logic synthesis</a></li>
<li><a href="https://github.com/mdzakirhussain/RTLDesignusingVerilogwithSKY130Technology/blob/main/README.md#labs-using-yosys-and-sky130-pdks">Labs using Yosys and Sky130 PDKs</a></li>
</ul>

<h2><a href="https://github.com/mdzakirhussain/RTLDesignusingVerilogwithSKY130Technology/blob/main/README.md#day-2---timing-libs-hierarchical-vs-flat-synthesis-and-efficient-flop-coding-styles-1">Day 2 - Timing libs, hierarchical vs flat synthesis and efficient flop coding styles</a></h2>

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

<p align="justify">The following are the commands to simulate the design written in the verilog code. Before going to simulation let us understand some terminology, Any design for example let us consider MUX 4x1 is been described in the Verilog HDL such a described file is called design file. Now, the description of the design is correct or not we need to confirm it, that is done through testbench, testbench is also a verilog code only but that consists of majorly two things</p>
  <ol>
  <li> Instantiation of the design</li>
  <li> Test Vectors</li>
    </ol>
    
 <p>We did the following simulation for Day-1</p>
  <ol><li>Mux 2x1</li></ol>
    <p>The following commands are used for performing the simulation using iverilog simulator</p>
    <ol>
<li>For compiling the design file(s) and testbench file<br /><b>iverilog design_file_name.v testbench_file_name.v</b></li>
  <li>After comiling a file with the name and extension  <b>a.out</b> will be generated. And this file is executed using the command<br /><b>vvp a.out</b><br />This will generate a file with the extension .vcd, for this file name can be given by the user in the testbench.</li>
  <li>And finally to see the waveform we use gtkwave using the coomand<br /><b>gtkwave filename.vcd</b></li>
  
</ol>
    
   <li><b>Mux 2x1 Simulation results</b></li> 
    
  <img src="day1 simulation/1 mux/2 mux_compile.png">
   
   <b>Fig.1 Command to compile design file and testbench file is "iverilog good_mux.v tb_good_mux.v"</b>
  
  <img  src="day1 simulation/1 mux/3 mux_execute.png">
  
  <b>Fig.2 Command to execute is "./a.out"</b>
  <img src="day1 simulation/1 mux/4 mux_vcd file generated.png">
  <b>Fig.3 shows vcd(value change dump) file been generated successfully</b>
  <img src="day1 simulation/1 mux/5 gtkwave command.png">
  <b>Fig.4 shows the command to invoke gtkwave using vcd file</b>
  <img src="day1 simulation/1 mux/6 gtkwave output.png">
  <b>Fig.5 Finally simulation result</b>
  <br />
  <br /><li><b>DFF with Asynchronous reset Simulation results</b></li>
  
  <img src="day1 simulation/2 dff asyncres/1 dff asyncres compile.png">
  <b>Fig.1 compile design file and testbench file</b>
     <img src="day1 simulation/2 dff asyncres/2 dff asyncres exec.png">
      <b>Fig.2 execute  "./a.out"</b>
       <img src="day1 simulation/2 dff asyncres/3 dff asyncres after exec vcd file.png">
         <b>Fig.3 shows vcd(value change dump) file been generated successfully</b>
         <img src="day1 simulation/2 dff asyncres/4 dff asyncres gtkwave command.png">
        <b>Fig.4 shows the command to invoke gtkwave using vcd file</b>
           <img src="day1 simulation/2 dff asyncres/5 dff asyncres gtkwave output.png">
         <b>Fig.5 Finally simulation result</b><br />  
   <br /><li><u><b>DFF with Asynchronous set Simulation results</b></u></li><br />
    <br /><img src="day1 simulation/3 dff async set/1 dff async set compile.png">
    <b>Fig.1 compile design file and testbench file</b>
     <img src="day1 simulation/3 dff async set/2 dff asyn set exec.png">
      <b>Fig.2 execute  "./a.out"</b>
      <img src="day1 simulation/3 dff async set/3 dff async set gtkwave command.png">
       <b>Fig.3 shows the command to invoke gtkwave using vcd file</b>
       <img src="day1 simulation/3 dff async set/4 dff async set gtkwave output.png">
       <b>Fig.4 Finally simulation result</b><br />
       <br /><li><b>DFF with synchronous reset Simulation results</b></li> 
   <img src="day1 simulation/4 dff syncres/1 dff syncres compile.png">
   <b>Fig.1 compile design file and testbench file</b>
    <img src="day1 simulation/4 dff syncres/2 dff syncres exec.png">
       <b>Fig.2 execute  "./a.out"</b>
     <img src="day1 simulation/4 dff syncres/3 dff syncres gtkwave command.png">
     <b>Fig.3 shows the command to invoke gtkwave using vcd file</b>
      <img src="day1 simulation/4 dff syncres/4 dff syncres gtkwave output.png">
      <b>Fig.4 Finally simulation result</b>
   
   
   
   
   
   
   

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
<b><li>What is Logic Synthesis?</li></b>
<p align="justify">Logic synthesis is a process of converting HDL code to gate level information, which is technically called gate-level netlist. To do logic synthesis we use software tool called synthesizer, in our case we are using open-source synthesizer tool called yosys.</p>

<h3><li>Labs using Yosys and Sky130 PDKs</li></h3>
<p>We did the synthesis for the following design on Day-1</p>
  <ol><li>Mux 2x1</li></ol>
    <p>The following commands and steps are followed for performing the synthesis using yosys synthesizer</p>
   <li><b>First step</b> we have to read standard cells library into the yosys using the command</li><br />
  <b><li>read_liberty -lib sky130_fd_sc_hd__tt_025C_1v80.lib</li></b><br />
    <li>Here sky130_fd_sc_hd__tt_025C_1v80.lib is standard cell library which is from <a href="https://www.skywatertechnology.com">skywatertechnology<a/></li><br />
  
<li><b>Second step</b> is to read verilog files into the yosys using the command</li><br />
  <b><li>read_verilog filename.v</li></b><br />
  
  <li><b>Thrird step</b> is to perform synthesis using the command</li><br />
  <b><li>synth -top module_name</li></b><br />
  
  <li><b>Fourth step</b> is to map to standard cells using the following command</li><br />
<b><li>abc -liberty sky130_fd_sc_hd__tt_025C_1v80.lib</li></b><br />

  <li><b>Fifth step</b> is to write out the netlist file using the command</li><br />
  <b><li>write_verilog your_file_name.v</li></b>
  
  <h3><li>Mux 2x1 Synthesis results</li></h3>
  
  <img src="day1 synthesis/1 mux/1 command to invoke yosys.png">
  <b>Fig.1 Invoking yosys</b>
  
  <img src="day1 synthesis/1 mux/2 yosys terminal.png">
  <b>Fig.2 Yosys terminal</b>
  
  <img src="day1 synthesis/1 mux/3 read liberty file.png">
  <b>Fig.3 Read liberty file</b>
  
  <img src="day1 synthesis/1 mux/4 read verilog file.png">
  <b>Fig.4 Read verilog file</b>
  
  <img src="day1 synthesis/1 mux/5 synth command.png">
  <b>Fig.5 Run synthesis</b>
  
  <img src="day1 synthesis/1 mux/6 after synth.png">
  <b>Fig.6 After synthesis</b>
  
  <img src="day1 synthesis/1 mux/7 abc command to generate netlist.png">
  <b>Fig.7 Stabdard cell netlist generation command</b>
  
  <img src="day1 synthesis/1 mux/8 after netlist.png">
  <b>Fig.8 After stabdard cell netlist</b>
  
  <img src="day1 synthesis/1 mux/9 write netlist.png">
  <b>Fig.9 Writing out standard cell netlist to a file</b>
  
  <img src="day1 synthesis/1 mux/10 show command.png">
  <b>Fig.10 Show command to view the diagram of cells</b>
  
  <img src="day1 synthesis/1 mux/11 after show command.png">
  <b>Fig.11 View in Diagram</b>
  
  
<h2>Day 2 - Timing libs, hierarchical vs flat synthesis and efficient flop coding styles</h2>

<ul>
<li>Introduction to timing .libs</li>
<li>Hierarchical vs Flat Synthesis</li>
<li>Various Flop Coding Styles and optimization</li>
</ul>  
  
  <p align="justify">In the Day 2 of the workshop, we have been given Introduction to what standard cells library means and what it contains. And also about types of synthesis such as differences between hierarchical vs flat synthesis. And, finally we also been given insights on optimization and different coding styles.</p>
  
   <p>We did the simulation on Day-2 for following list </p>
  <ol><li>DFF with Asynchronous reset</li>
    <li>DFF with synchronous set</li>
    <li>DFF with synchronous reset</li>
    </ol><br />
    <p>We did the synthesis for the following list of designs on Day-2</p>
  <ol>
  <li>Multi module synthesis using hierarchical and flat approaches</li>
    <li>DFF with Asynchronous reset</li>
    <li>DFF with synchronous set</li>
    <li>DFF with synchronous reset</li>
    </ol>
<h3><li>Introduction to timing .libs</li></h3>

<p>Sample of .lib that is liberty file</p>

<img src="lib file/1 lib file sample.png">
<img src="lib file/2 lib file sample.png">

<h3><li>Hierarchical vs Flat Synthesis</li></h3>

<p>The following are the images of synthesis showing differences between hierarchical and flat synthesis </p>

<img src="hier vs flat/1 invoke yosys.png">
<b>Fig.1 Invoke yosys</b>

<img src="hier vs flat/2 yosys terminal.png">
<b>Fig.2 Yosys terminal</b>

<img src="hier vs flat/3 read liberty.png">
<b>Fig.3 Read liberty</b>

<img src="hier vs flat/4 read verilog.png">
<b>Fig.4 Read verilog</b>

<img src="hier vs flat/5 after read.png">
<b>Fig.5 After verilog read</b>

<img src="hier vs flat/6 synth -top hier.png">
<b>Fig.6 Synth -top for netlist</b>

<img src="hier vs flat/7 after synth command.png">
<b>Fig.7 After synth command</b>

<img src="hier vs flat/8 abc command.png">
<b>Fig.8 abc command to map to standard cells</b>

<img src="hier vs flat/10 show op.png">
<b>Fig.9 Result of hierarchical synthesis </b>

<img src="hier vs flat/11 flatten.png">
<b>Fig.10 Command for Flatten synthesis</b>

<img src="hier vs flat/12 show command for flatten.png">
<b>Fig.11 Result of flatten synthesis</b>


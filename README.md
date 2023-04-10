### cpu_soft_cores
## An Inventory of Soft Core Processors

## Introduction  
The included files are PDF versions of spreadsheet pages covering OpenCores and other available source code for FPGA based soft core processors. Criteria for inclusion here is that there be source code and documentation. For those cores considered as interesting, the core needs to be “usable”. That is: the core has been compiled, placed and routed into an FPGA chip and that it is mostly correct and mostly complete.

Have added columns for: Vendor CPR results (AILX col W), SOC designs (Y/N, col Z) and address modes (col AK). Column X is moved to column O, gives DFF count.

The PDF spreadsheets are available through the Downloads window.  
Have recently added the Excel spreadsheet as cut and paste from the PDF version no longer works.  

The latest updates include web-links (col D and AQ) and author (col G) where available, old designs in particular have dead web-links.
Current process is to compile, place & route into Xilinx Zynq Ultrascale+ or Altera-Intel Arria-2. Am making a modest amount of effort editing each design to get a successful CPR.  Am at this time not attempting to CPR designs that are other than VHDL, Verilog or System Verilog.

## Cautions  
Am developing a metric for comparison across the wide variety of data and instruction sizes, architecture types, instruction set “completeness” and FPGA families. The current metric is 1000 times Fmax times MIPS/clk divided by LUT-ALUT count and clks/inst. MIPS/clk is adjusted to reflect data size and instruction set usefulness. Have generally used as the top module the module with simple memory ports and no SOC features. Have refrained from making any source code changes other than syntax corrections and replacement of vendor specific IP with generic inferred IP (RAM, clock generation, ...).   Bare cores without memory do not include the access time delay of block RAM.  

The PDF spreadsheets contain full information. Cut & paste a link or set of blocks into a text editor to see the clipped text.
Several categories of designs are not yet included in the PDF files: Paper designs where there is a published paper but source code is not openly available. Planning designs where there is an OpenCores project name and possibly an ISA description but no source code. Incomplete designs. And designs that are probably simulation only.

## Intent  
Goal is to classify the ~500 unique processor cores as to data and instruction sizes, architecture types, instruction set “completeness”, register set size, etc. And to find those cores that exhibit outstanding performance. For about 440 processor designs have obtained LUT-ALUT counts and an Fmax for atleast one FPGA family.

For well maintained designs with full tools and validation see  
https://en.wikipedia.org/wiki/Soft_microprocessor  
https://web.archive.org/web/20091026171102/http://1-core.com/library/digital/soft-cpu-cores/  

## Call for Help  
Those that wish to contribute corrections or compile, place, route and timing data are welcome to do so. Please provide entries for each spreadsheet column including your name, tool version and top module name.  A project archive is the most useful and smallest file size that lets one reproduce results.  

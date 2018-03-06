# Formal Verification VLSI

<!-- TOC -->

- [Formal Verification VLSI](#formal-verification-vlsi)
    - [Formal Verification Category](#formal-verification-category)
        - [Equivalce Checking](#equivalce-checking)
            - [C-to-RTL](#c-to-rtl)
            - [RTL-to-RTL](#rtl-to-rtl)
        - [Formal Assertion Based Verification](#formal-assertion-based-verification)
        - [Formal Apps](#formal-apps)
    - [Formal Verification Tool](#formal-verification-tool)
    - [Vendor: Cadence](#vendor-cadence)
    - [Vendor: Mentor](#vendor-mentor)
    - [Vendor: OneSpin](#vendor-onespin)
    - [Vendor: Synopsys](#vendor-synopsys)
    - [Vendor: ATEC](#vendor-atec)
    - [Vendor: RealIntent](#vendor-real-intent)
    - [Vendor: Averant](#vendor-averant)
    - [Consulting: Oski Tech](#consulting-oski-tech)
    - [Disclaimer](#disclaimer)
    - [Reference](#reference)

<!-- /TOC -->

## Formal Verification Category

### Equivalce Checking

#### C-to-RTL

Checking your SystemC/C/C++ code against your RTL code following high level synthesis (HLS) to see if your design intent is upheld.

Tools: Mentor (Calypto) `SLEC`; Synopsys `Hector`; ATEC `ATEC`.

#### RTL-to-RTL

Comparing different RTL code or gate level code of the same design to make sure they have the same functionality.

Tools: Mentor `SLEC`; OneSpin `EC-RTL`; Cadence `JasperGold`; Synopsys `Hector`; ATEC `ATEC`.

### Formal Assertion Based Verification

F-ABV verifies that the properties of your design source code functionality match those described in your spec. 

Tools: Cadence `JasperGold`,`IFV`; Mentor `Questa FV`, `Calypto`; OneSpin `Verify`; Synopsys `VC Formal`; ATEC `ATEC`.

### Formal Apps

Formal apps which, for specific situations, automatically create assertions.

     1. Register Checking App
     2. Connectivity Checking App
     3. Structural Property (or Assertion Synthesis) App
     4. Activation Checks and Code Unreachability App
     5. Scoreboarding App
     6. Safety Fault Analysis App
     7. Security Verification App
     8. Clock Domain Crossing (CDC) App
     9. Power Domain Management App
    10. X-Propagation Checking App
    11. Abstract Assertion Authoring App
    12. Sim-Trace Property Synthesis App
    13. Protocol Compliance Apps
    14. Sequential Verilog/VHDL RTL Equivalency Checking App
    15. Arithmetic Precision Analysis App
    16. And the 3rd Party App Marketplace
Vendor: Cadence; Mentor; OneSpin; Synopsys; Real intent.



## Formal Verification Tool

|                                                 | Cadence                                                      | Mentor                                                       | OneSpin                                                      | Synopsys                                                   | ATEC                                                         |
| ----------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ---------------------------------------------------------- | ------------------------------------------------------------ |
| **Formal Verification Tool**                    | JasperGold, IFV.                                             | Questa FV, Calypto                                           | Verify                                                       | VC Formal                                                  | ATEC                                                         |
| **Performance/ Capacity/ Convergence Estimate** | 21 formal engines. Manual + automatic selection. Optimized Formal model. Mature autoprove strategies | ~10 formal engines, Manual + automatic selection. Basic Formal Model. | 15-20 formal engines, Manual + automatic selection. Optimized Formal model. | ~4-5 formal engines. Manual selection. Basic Formal model. | 8 formal engines. Manual selection. Basic  Formal model.     |
| **Debug**                                       | Graphical debugger w/ formal based root cause, and what-if analysis. Trace generation. HDL test generation. | Graphical debugger w/ root cause analysis. Trace generation. | Graphical debugger w/ root cause analysis. Trace generation. HDL Test Generation | Graphical debugger w/ root cause analysis.                 | Trace generation. HDL Test Generation. Scripts to launch simulator and waveform. |
| **Setup and Control**                           | Assertion templates. Ctrl signal recognition. TCL.           | Some signal recognition. TCL.                                | Assertion templates. Ctrl Signal recognition. TCL.           | TCL. Ask vendor.                                           | Ctrl Signal recognition. TCL.                                |
| **Property types**                              | Safety, Activation, Liveness, Coverage, Structural.          | Safety, Activation, Structural                               | Safety, Activation, Liveness, Coverage, Structural.          | Safety, Activation.                                        | Safety, Activation, Liveness, Coverage.                      |
| **Standard Language Support Assertions**        | SVA, PSL, VHDL                                               | SVA, PSL                                                     | SVA, PSL, VHDL, C                                            | SVA                                                        | Simple SVA. Verilog 2005, C++14.                             |
| **Coverage mechanisms**                         | Assertion coverage. COI-based constraint and property analysis. Proof Core (accurate engine-level) coverage. | Assertion coverage.                                          | Assertion coverage. Observation coverage.                    | Mutation analysis.                                         | Assertion coverage.                                          |
| **Formal-Stimulation Interoperability**         | Closed db read/write for an intelligent CDNS formal-simulation coverage and unified analysis. UCIS write. | Open db. UCIS read/write.                                    | Open db. UCIS read/write.                                    | Closed db read/write.                                      | Log only.                                                    |
| **Engine Access**                               | Parallel engine. (>1000 engines on server farm; flexible ProofGrid control) Standard license. | Standard license.                                            | Parallel engine. Cloud support. Standard and token licensing. | Standard licence.                                          | Parallel engine. Floating license.                           |
| **Access to Formal Expert AE Support**          | Large focused group of corporate AEs, large group of formal specialist FAEs, even larger group of formal-knowledgeable verification FAEs. | Small number of specialized AEs                              | Focused group of Field and Corporate AEs                     | Some experts recently hired                                | Small number of specialized AEs.                             |
| **Price**                                       |                                                              |                                                              |                                                              |                                                            | affordable (As low as 50,000$)                               |



## Vendor: Cadence

Cadence: Acquired Bell Labs Design Automation formal technology in 1996, and Verplex in 2003.  Both are used as a basis for their Incisive Formal  Verification (IFV) internal development.  CDNS acquired Jasper in 2014.

JasperGold Formal Verification Platform (Apps)  https://www.cadence.com/content/cadence-www/global/en_US/home/tools/system-design-and-verification/formal-and-static-verification/jasper-gold-verification-platform.html

Incisive Formal Verification Platform https://www.cadence.com/content/cadence-www/global/en_US/home/tools/system-design-and-verification/formal-and-static-verification/incisive-formal-verification-platform.html

Conformal Equivalence Checker - Cadence https://www.cadence.com/content/cadence-www/global/en_US/home/tools/digital-design-and-signoff/equivalence-checking/conformal-equivalence-checker.html



## Vendor: Mentor

Mentor: Acquired 0-In in 2004, used as the technology basis of their Questa Formal Verification.  Acquired Calypto in 2015.

Questa Formal Verification Apps https://www.mentor.com/products/fv/questa-formal-verification-apps

Questa SLEC (0-In) https://www.mentor.com/products/fv/questa-slec



## Vendor: OneSpin

OneSpin: Spun-out of Siemens/Infineon formal verification group in 2005.  Since that time, they've extended their core formal platform and expanded their offering.

360 DV-Verify https://www.onespin.com/products/360-dv-verify/

360 EC-RTL https://www.onespin.com/products/360-ec-rtl/



## Vendor: Synopsys

Synopsys: Acquired the Chrysalis formal technology through their 2001 Avanti merger.  Also picked up Hector through their 2012 SpringSoft acquisition.  SNPS had internally written their Magellan formal tool.  They have a new tool listed on their website as "VC Formal" and they recently acquired Atrenta.

VC Formal https://www.synopsys.com/verification/static-and-formal-verification/vc-formal.html

Hector (now part of VC Formal) https://www.synopsys.com/jp2/Tools/Verification/FunctionalVerification/Pages/HECTOR.aspx

Formality and Formality Ultra https://www.synopsys.com/implementation-and-signoff/signoff/formality-and-formality-ultra.html



## Vendor: ATEC

ATEC: ATEC Technologies, Inc. is a startup technology company that specializes in Formal Verification. ATEC was founded in 2011 in Santa Clara. Currently, ATEC have technology support team in USA and China. The founders came out of NVIDIA 7 years ago.

ATEC: A Tool for Equivalence Checking http://tukarla.com/



## Vendor: RealIntent

Real Intent: The founders came out of Sun Microsystems 15 years ago.  Originally they developed a formal verification platform, then focused on specific apps.

Verix CDC http://www.realintent.com/real-intent-products/verix-cdc/



## Vendor: Averant

Solidify model checker http://www.averant.com/products-solidify.html



## Consulting: Oski Tech

Oski http://www.oskitechnology.com/



## Disclaimer

I am an employee of ATEC. To be neutral, the statics in this document directly cames from ATEC and the following references. 



## Reference

[DeepChip: Jim Hogan on how "this is not your father's formal verification"](http://www.deepchip.com/items/0558-01.html) how dramatically formal verification has grown over the last 20 years. 

[DeepChip: Where Formal ABV whomps HDL simulation for chip verification](http://www.deepchip.com/items/0558-02.html)

[DeepChip: 9 major and 23 minor Formal ABV tool metrics - plus their gotchas](http://www.deepchip.com/items/0558-03.html)

[DeepChip: 16 Formal Apps that make Formal easy for us non-Formal engineers](http://www.deepchip.com/items/0558-04.html)

[DeepChip: Hogan on Cadence, Mentor, OneSpin, Real Intent, Synopsys formal](http://www.deepchip.com/items/0558-05.html)

[DeepChip: OneSpin CEO cites 8 "insufficiencies" in Jim Hogan's Formal Guide](http://www.deepchip.com/items/0558-06.html)


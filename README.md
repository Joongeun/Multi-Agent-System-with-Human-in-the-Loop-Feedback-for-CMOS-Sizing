# Multi-Agent-System-with-Human-in-the-Loop-Feedback-for-CMOS-Sizing
I developed a "Human-in-the-Loop" (HITL) multi-agent system using the Google Agent Development Kit (ADK) to automate the complex process of transistor sizing in circuit design.

**The Problem**

Manually sizing transistors to meet specific performance targets (like speed and voltage symmetry) is a tedious, iterative process.

**The Solution**

I built a specialized AI workforce where each agent handles a specific part of the design cycle:

* Theoretical Analysis: A "CircuitExplainer" agent determines how transistor widths will impact performance.

* Automated Simulation: Agents autonomously write and run ngspice scripts to test the circuit after each iteration of parameter modification.

* Intelligent Optimization: A "Sizer" agent analyzes simulation data and proposes adjustments.

* Human-in-the-Loop: To speed up convergence to a solution, the system pauses to request expert feedback (e.g., "Double the size") before proceeding, combining AI speed with human oversight.

**The Result**

The agentic workflow successfully optimized a CMOS inverter from a failing state (900ps delay) to meeting all strict design specifications (< 50ps delay) within just a few automated iterations.

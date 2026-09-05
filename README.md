# Hash Power & Democratic Blockchain Review

This directory contains a comprehensive critical review and presentation evaluating the research paper **"Performance Evaluation for the Hash Generation Phase of a Democratic Blockchain"** by Luis Lugo and César Pedraza (2020).

## Overview

The reviewed study analyzes how various parallel computing techniques affect execution time and energy consumption during the hash generation phase of a "democratic blockchain" protocol (proposed by Paul, Sarkar, & Mukherjee, 2014). This critical review evaluates the paper's technical contributions, benchmark methodologies, energy estimation model, and systemic implications for network consensus, security, and economic sustainability compared to Bitcoin's Proof-of-Work (PoW).

## Authors of the Review

- **Andrés Arias**
- **Catalina Jaramillo**
- **Rafael Marulanda**

*Pontificia Universidad Javeriana*

---

## Directory Contents

| File | Description |
| :--- | :--- |
| [`resena_lugo_hash_power.tex`](file:///d:/repos/master-tesis-economy/Bitcoin-economics/05_hash-power/resena_lugo_hash_power.tex) | Full academic critical review article in LaTeX format. |
| [`resena_lugo_hash_power.pdf`](file:///d:/repos/master-tesis-economy/Bitcoin-economics/05_hash-power/resena_lugo_hash_power.pdf) | Compiled PDF of the academic critical review. |
| [`critica_lugo_pedraza_beamer.tex`](file:///d:/repos/master-tesis-economy/Bitcoin-economics/05_hash-power/critica_lugo_pedraza_beamer.tex) | 10-slide Beamer presentation in LaTeX format. |
| [`critica_lugo_pedraza_beamer.pdf`](file:///d:/repos/master-tesis-economy/Bitcoin-economics/05_hash-power/critica_lugo_pedraza_beamer.pdf) | Compiled PDF of the Beamer presentation slides. |
| [`Lugo_2020.pdf`](file:///d:/repos/master-tesis-economy/Bitcoin-economics/05_hash-power/Lugo_2020.pdf) | Original paper by Luis Lugo & César Pedraza (2020). |

---

## Key Synthesis & Findings

1. **Hardware Parallelization**:
   - **CPU (POSIX / OpenMP)**: Execution time ~1,351 s; limited scaling beyond physical cores.
   - **Cluster (Open MPI)**: Virtualization overhead and network latency limit throughput gains.
   - **GPU (CUDA / OpenCL)**: Achieves maximum speedup (~10–12× acceleration), reducing execution time to 106–120 s.

2. **Energy Efficiency**:
   - CUDA demonstrates the lowest estimated energy consumption (**4.66 Wh**), compared to **~21 Wh** on CPU and **100.20 Wh** on Open MPI. High-power parallel hardware can lower total energy consumption by significantly shortening execution time.

3. **Systemic & Methodological Critique**:
   - **Scope Boundary**: Lugo & Pedraza measure only the local hash generation subroutine, excluding network propagation, hash broadcasting, and validation phases.
   - **Consensus & Security Trade-offs**: Democratic min-hash selection reduces PoW hashing competition but introduces significant communication complexity and message flooding risks.
   - **ASIC & Thermal Recovery**: The study omits ASIC hardware benchmarks and thermal waste-heat recovery models, which alter the net energy balance in industrial mining operations.

---

## Compilation Instructions

To recompile the document files locally, use `latexmk` or `pdflatex`:

```bash
# Compile the review paper
latexmk -pdf resena_lugo_hash_power.tex

# Compile the presentation slides
latexmk -pdf critica_lugo_pedraza_beamer.tex
```

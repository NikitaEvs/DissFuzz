# DissFuzz

Decentralized fuzzing based on untrustworthy nodes.

**Presentation**: [Google Slides](https://docs.google.com/presentation/d/1bytUYZyYBLtQCxYB2k0tFoIBmTncc_5h7DeJc_Ia4Sw/edit?usp=sharing) or [PDF](docs/final_presentation.pdf).

## Authors
- [Milana Maric](https://github.com/milanammaric)
- [Qifan Pan](https://github.com/civp)
- [Nikita Evsiukov](https://github.com/NikitaEvs)
- [Vladimir Hanin](https://github.com/VladimirHaninEPFL)
- [Chau Ying Kot](https://github.com/KurohanaJuri)
- [Derya Cögendez](https://github.com/deryacog)

## Demo
![Demo](media/demo.gif)

## Overview
Fuzzing is a technique employed to identify vulnerabilities
in a program by automatically generating and testing diverse inputs. Running
a fuzzer locally on a single machine can be time-consuming, so it can be distributed across different machine cores.

Our project, DissFuzz, is ***the first work*** to support **distributed
and decentralised fuzzing based on untrusted nodes**:
- The system incorporates different actors that use the blockchain
for synchronisation, ensuring the security of our system.
- To encourage user participation in the system,
we introduce a **digital currency**. 
- To maintain the integrity
and security of our system, we implement a **Proof of Work
(PoW)** mechanism.

The objective of the project is to extend the
distributed fuzzing further by **eliminating the single point of
trust**. This is achieved through the implementation of **permissionless consensus** and **zero-knowledge Proof-of-Fuzzing-Work** implemented using [**Execution Hash**](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=9791228) of programs under fuzzing.

## Disclaimer
Since the project is based on the course's homeworks, the repository doesn't contain any code. Our work is an extension of the paper D. Jang, A. Askar, I. Yun, S. Tong, Y. Cai, and T. Kim, “Fuzzing@home:
Distributed fuzzing on untrusted heterogeneous clients".

Majority of the codebase is written in Go. Some parts related to cryptography and LLVM generation are implemented in C++.

## Content

- [Main project report](docs/final_report.pdf)
- [Main project presentation](docs/final_presentation.pdf)
- [Individual report](docs/individual_report.pdf)
- Modified llvm-17 [source tree](https://github.com/NikitaEvs/fuzzcoin_llvm) for execution hash generation
- [Probability analysis](docs/probability_analysis.pdf) of the decentralized fuzzing coverage 
- [Core idea design](docs/decentralized_design.pdf)
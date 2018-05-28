# awesome-mpc [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

The list format was inspired from [awesome list](https://github.com/sindresorhus/awesome) and after a fruitful lunch discussion at [TPMPC](http://www.multipartycomputation.com/). It is designed to have a central place where everyone can find open-source software designed for MPC as well as introductory material to this topic.

Moreover, the list is given alphabetically and divided into categories of libraries which are actively maintained or recently developed.

Please feel free to do a pull request with any MPC software or resource you know and it is not on the list. The current classification might not be most suitable one and I am open to any suggestions.

## Contents

- [Theory](#theory)
	- [Books](#books)
	- [Courses](#courses)
	- [Tutorials](#tutorials)
- [Misc](#misc)
- [Software](#software)
	- [Frameworks](#frameworks)
	- [Primitives](#primitives)
 	- [Protocols](#protocols)
	- [Tools](#tools)

## Theory

### Books

- [Applications of Secure Multiparty Computation](http://ebooks.iospress.nl/volume/applications-of-secure-multiparty-computation) - Collection of MPC protocols for several real-world tasks such as statistics.
- [Secure Multiparty Computation and Secret Sharing](http://www.cambridge.org/dk/academic/subjects/computer-science/cryptography-cryptology-and-coding/secure-multiparty-computation-and-secret-sharing?format=HB) - Comprehensive treatment of unconditionally secure techniques for multiparty computation (MPC) and secret sharing.

### Courses

- [FHE-MPC Advanced Grad Course](https://www.cs.bris.ac.uk/home/nigel/FHE-MPC/) - `informal grad course' in FHE and MPC.
- [Secure Computation](http://drona.csa.iisc.ernet.in/%7Earpita/SecureComputation15.html) - Secure Computation course offered by Indian Institute of Science covering secret sharing schemes, oblivious transfer to impossiblity results and zero-knowledge proofs.
- [Secure Multi-Party Computation at Scale](https://piazza.com/bu/fall2017/cs591v1/home) - Boston University course that covers mathematical and algorithmic foundations of MPC, with an additional focus on deployment of state-of-the-art MPC technologies.

### Tutorials

- [How To Simulate It](https://eprint.iacr.org/2016/046) - A Tutorial on the Simulation Proof Technique.
- [OSU Bibliography](https://web.engr.oregonstate.edu/~rosulekm/scbib/index.php?n=Main.GettingStarted) - An Annotated Bibliography of Practical Secure Computation.
- [The 1st BIU Winter School](http://cyber.biu.ac.il/event/the-1st-biu-winter-school/) - Introductory lectures for basic secure computation constructions.
- [The 5th BIU Winter School](http://cyber.biu.ac.il/event/the-5th-biu-winter-school/) - Tutorials and recent advances in secure computation delivered in video format.

## Misc

- [ePrint papers](https://guutboy.github.io) - Frequently updated list of secure computation papers appearing on IACR eprint.

## Software

Here I tried to reference the most recent article found on specific software since enumerating all changes including the original paper is too cumbersome.

## Frameworks

- [ABY](https://github.com/encryptogroup/ABY) - 2PC with secret sharing and garbled circuits; secure against semi-honest adversaries | [NDSS'15](http://encrypto.de/papers/DSZ15.pdf).
- [batchDualEx](https://github.com/osu-crypto/batchDualEx) - 2PC with garbled circuits; secure against malicious adversaries | eprint: [2016/632](https://eprint.iacr.org/2016/632).
- [Duplo](https://github.com/AarhusCrypto/DUPLO) - 2PC with garbled circuits; secure against malicious adversaries.
- [EMP-toolkit](https://github.com/emp-toolkit) - 2PC and MPC with garbled circuits; secure against semi-honest adversaries (emp-sh2pc). There are also ones resistant against malicious parties (emp-[ag2pc|m2pc|agmpc]). | eprint: [2017/189](https://eprint.iacr.org/2017/189), [2016/762](https://eprint.iacr.org/2016/762), [2017/030](https://eprint.iacr.org/2017/030)
- [FRESCO](http://fresco.readthedocs.io/en/latest/) - MPC supporting TinyTables or SPDZ protocols; secure against semi-honest or malicious adversaries | [Practice'15](http://practice-project.eu/downloads/publications/D22.1-State-of-the-art-analysis-PU-V1.1.pdf).
- [Obliv-C](http://oblivc.org/) - 2PC with garbled circuits; secure against semi-honest adversaries | eprint: [2015/1153](http://eprint.iacr.org/2015/1153).
- [Sharemind](https://sharemind.cyber.ee/) - 2PC or 3PC with secret sharing; secure against semi-honest adversaries | [Cyber'13](https://cyber.ee/uploads/2013/04/Jagomagis_msc.pdf).
- [SPDZ](https://www.cs.bris.ac.uk/Research/CryptographySecurity/SPDZ/) - General MPC with secret sharing; secure against malicious adversaries | eprint: [2017/1230](https://eprint.iacr.org/2017/1230).
- [TinyLEGO](https://github.com/AarhusCrypto/TinyLEGO) - 2PC with garbled circuits; secure against malicious adversaries | eprint: [2015/309](http://eprint.iacr.org/2015/309).

## Primitives
- [APRICOT](https://github.com/bristolcrypto/apricot) - OT Extension secure against malicious adversaries | [2015/546](http://eprint.iacr.org/2015/546).
- [libOTe](https://github.com/osu-crypto/libOTe) - Library with various OT Extensions.
- [OT Extension](https://github.com/encryptogroup/OTExtension) - OT Extension secure against malicious adversaries | [2015/061](https://eprint.iacr.org/2015/061).
- [SCAPI](https://github.com/cryptobiu/libscapi) - Various secure computation API's carefully documented with a clean code design in mind | [2012/629](http://eprint.iacr.org/2012/629).
- [SplitCommit](https://github.com/AarhusCrypto/SplitCommit) - Additively homomorphic commitment scheme | [2015/694](http://eprint.iacr.org/2015/694).
- [TSS](https://github.com/snipsco/rust-threshold-secret-sharing) - A pure-Rust implementation of various threshold secret sharing schemes.


## Protocols
- [BaRK-OPRF](https://github.com/osu-crypto/BaRK-OPRF) - Private Set Intersection | [2016/799](https://eprint.iacr.org/2016/799).
- [Linreg](https://github.com/schoppmp/linreg-mpc/) - Privacy preserving linear regression | [2016/892](https://eprint.iacr.org/2016/892).
- [Geppetri](https://github.com/meilof/geppetri) - Verifiable 3PC | [2017/013](https://eprint.iacr.org/2017/013).
- [ORAM (Obliv-C)](http://oblivc.org/sqoram/) - Oblivous RAM | [S&P'16](http://oblivc.org/docs/sqoram.pdf).
- [PSI](https://github.com/encryptogroup/PSI) - Private Set Intersection | [2014/447](https://eprint.iacr.org/2014/447).

## Tools
- [CBMC-GC](http://www.seceng.informatik.tu-darmstadt.de/index.php/research/software/cbmc-gc/) - Creates Boolean circuits from ANSI-C code optimized for secure computation | [ShallowCC](http://www.seceng.informatik.tu-darmstadt.de/assets/buescher/ShallowCC16.pdf).
- [UC Compiler](https://github.com/encryptogroup/UC) - Valiant's Universal Circuit Compiler | [2016/093](https://eprint.iacr.org/2016/093).


## Contribute

Contributions welcome! Read the [contribution guidelines](contributing.md) first.


## License

[![CC0](http://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](http://creativecommons.org/publicdomain/zero/1.0)

To the extent possible under law, Dragoș Rotaru has waived all copyright and
related or neighboring rights to this work.

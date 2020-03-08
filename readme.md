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
	- [Retired software](#retired-software)
- [Workshops](#workshops)

## Theory

### Books

- [A Pragmatic Introduction to Secure Multi-Party Computation](https://securecomputation.org) - A broad introduction to the field of secure multi-party computation, covering both the fundamental constructions and many of the recent improvements. The book emphazises the intuition and ideas behind the protocols rather than rigorous proofs.
- [Applications of Secure Multiparty Computation](http://ebooks.iospress.nl/volume/applications-of-secure-multiparty-computation) - Collection of MPC protocols for several real-world tasks such as statistics.
- [Efficient Secure Two-Party Protocols](https://www.springer.com/us/book/9783642143021) - Comprehensive study of efficient protocols and techniques for secure two-party computation – both general constructions that can be used to securely compute any functionality, and protocols for specific problems of interest.
- [Secure Multiparty Computation and Secret Sharing](http://www.cambridge.org/dk/academic/subjects/computer-science/cryptography-cryptology-and-coding/secure-multiparty-computation-and-secret-sharing?format=HB) - Comprehensive treatment of unconditionally secure techniques for multiparty computation (MPC) and secret sharing.

### Courses

- [Cryptographic Computing Course](http://orlandi.dk/crycom) - Course on MPC, Homomorphic Encryption and related topics given by Claudio Orlandi at Aarhus University.
- [FHE-MPC Advanced Grad Course](https://homes.esat.kuleuven.be/~nsmart/FHE-MPC/) - 'Informal grad course' in FHE and MPC.
- [Secure Computation](http://drona.csa.iisc.ernet.in/%7Earpita/SecureComputation15.html) - Secure Computation course offered by Indian Institute of Science covering secret sharing schemes, oblivious transfer to impossiblity results and zero-knowledge proofs.
- [Secure Multi-Party Computation at Scale](https://piazza.com/bu/fall2017/cs591v1/home) - Boston University course that covers mathematical and algorithmic foundations of MPC, with an additional focus on deployment of state-of-the-art MPC technologies.

### Tutorials

- [Getting Started with MPC](http://u.cs.biu.ac.il/~lindell/MPC-resources.html) - Light compilation of basic resources for getting started in MPC study and research.
- [How To Simulate It](https://eprint.iacr.org/2016/046) - A Tutorial on the Simulation Proof Technique.
- [OSU Bibliography](https://web.engr.oregonstate.edu/~rosulekm/scbib/index.php?n=Main.GettingStarted) - An Annotated Bibliography of Practical Secure Computation.
- [UC Security](https://www.youtube.com/playlist?list=PLqc9MPlwib9nSuyH4oUIwPsyDiZ4bwuEE) - Video lectures on UC security delivered by Ran Canetti.

## Misc

- [ePrint papers](https://guutboy.github.io) - Frequently updated list of secure computation papers appearing on IACR eprint.

## Software

Here I tried to reference the most recent article found on specific software since enumerating all changes including the original paper is too cumbersome.

### Frameworks

- [ABY](https://github.com/encryptogroup/ABY) - 2PC with secret sharing and garbled circuits; secure against semi-honest adversaries. | [NDSS'15](http://encrypto.de/papers/DSZ15.pdf).
- [ABY3](https://github.com/ladnir/aby3) - 3PC with secret sharing for privacy preserving machine learning and database joins (PSI, Union, etc.); secure against semi-honest adversaries. | [CCS'18](https://eprint.iacr.org/2018/403.pdf), [2019/518](https://eprint.iacr.org/2019/518.pdf).
- [BatchDualEx](https://github.com/osu-crypto/batchDualEx) - 2PC with garbled circuits; secure against malicious adversaries. | eprint: [2016/632](https://eprint.iacr.org/2016/632).
- [CrypTen](https://github.com/facebookresearch/CrypTen) - MPC with secret sharing; secure against semi-honest adversary; focused on building PyTorch applications. | documentation: [link](https://crypten.ai/)
- [EMP-toolkit](https://github.com/emp-toolkit) - 2PC and MPC with garbled circuits; secure against semi-honest adversaries (emp-sh2pc). There are also ones resistant against malicious parties (emp-[ag2pc|m2pc|agmpc]) | eprint: [2017/189](https://eprint.iacr.org/2017/189), [2016/762](https://eprint.iacr.org/2016/762), [2017/030](https://eprint.iacr.org/2017/030).
- [Fancy-Garbling](https://github.com/spaceships/fancy-garbling) - 2PC with arithmetic garbled circuits; secure against semi-honest adversaries. | eprint: [2016/969](https://eprint.iacr.org/2016/969).
- [FRESCO](http://fresco.readthedocs.io/en/latest/) - MPC supporting TinyTables or SPDZ protocols; secure against semi-honest or malicious adversaries. | [Practice'15](http://practice-project.eu/downloads/publications/D22.1-State-of-the-art-analysis-PU-V1.1.pdf).
- [HoneyBadgerMPC](https://github.com/initc3/HoneyBadgerMPC) - Robust MPC-based confidentiality layer for blockchains with guaranteed output delivery; secure against up to t < n/3 malicious parties.
- [JIFF](https://github.com/multiparty/jiff/) - JavaScript client and server libraries for building web-based applications that employ general purpose MPC; secure against semi-honest adversaries. | documentation: [link](https://multiparty.org/jiff/).
- [MP-SPDZ](https://github.com/data61/MP-SPDZ) - MPC with garbled circuits or secret sharing; secure against malicious or semi-honest adversaries with dishonest or honest majority. | [documentation](https://mp-spdz.readthedocs.io/en/latest/)
- [MPyC](https://www.win.tue.nl/%7Eberry/mpyc/) - BGW honest majority multi-party protocol; secure against semi-honest adversaries. | [TPMPC'18](https://www.win.tue.nl/~berry/mpyc/TPMPC2018.pdf).
- [Obliv-C](http://oblivc.org/) - 2PC with garbled circuits; secure against semi-honest adversaries. | eprint: [2015/1153](http://eprint.iacr.org/2015/1153).
- [SCALE-MAMBA](https://homes.esat.kuleuven.be/~nsmart/SCALE/) - General MPC with secret sharing; secure against various adversaries including malicious with a dishonest majority. Software closer to a production system. | documentation: [link](https://homes.esat.kuleuven.be/~nsmart/SCALE/Documentation.pdf).
- [Sharemind](https://sharemind.cyber.ee/) - 2PC or 3PC with secret sharing; secure against semi-honest adversaries. | [Cyber'13](https://cyber.ee/research/theses/roman_jagomagis_msc.pdf).
- [swanky](https://github.com/GaloisInc/swanky) - A suite of rust libraries for secure multi-party computation (currently includes oblivious transfer, garbled circuits, and private set intersection).
- [Tf-encrypted](https://github.com/mortendahl/tf-encrypted/) - 3PC with secret sharing; secure against semi-honest adversaries; focused on TensorFlow-based applications.

### Primitives

- [APRICOT](https://github.com/bristolcrypto/apricot) - OT Extension secure against malicious adversaries. | [2015/546](http://eprint.iacr.org/2015/546).
- [Distributed Vector-OLE](https://github.com/schoppmp/distributed-vector-ole) - A two-party generator for Vector-OLE correlations. [CCS'19](https://eprint.iacr.org/2019/1084.pdf).
- [LibOTe](https://github.com/osu-crypto/libOTe) - Library with various OT Extensions.
- [OT Extension](https://github.com/encryptogroup/OTExtension) - OT Extension secure against malicious adversaries. | [2015/061](https://eprint.iacr.org/2015/061).
- [SCAPI](https://github.com/cryptobiu/libscapi) - Various secure computation API's carefully documented with a clean code design in mind. | [2012/629](http://eprint.iacr.org/2012/629).
- [SplitCommit](https://github.com/AarhusCrypto/SplitCommit) - Additively homomorphic commitment scheme. | [2015/694](http://eprint.iacr.org/2015/694).
- [TSS](https://github.com/snipsco/rust-threshold-secret-sharing) - A pure-Rust implementation of various threshold secret sharing schemes.


### Protocols

- [BaRK-OPRF](https://github.com/osu-crypto/BaRK-OPRF) - Private Set Intersection. | [2016/799](https://eprint.iacr.org/2016/799).
- [Blockchain-Crypto-MPC](https://github.com/unbound-tech/blockchain-crypto-mpc) - Multiparty ECDSA signing in the cryptocurrency setting, includes an optimized GC library, OT, and more. | [CCS'18](https://eprint.iacr.org/2018/987).
- [LibPSI](https://github.com/osu-crypto/libPSI) - Various protocols for performing private set intersection.
- [Linreg](https://github.com/schoppmp/linreg-mpc/) - Privacy preserving linear regression. | [2016/892](https://eprint.iacr.org/2016/892).
- [Geppetri](https://github.com/meilof/geppetri) - Verifiable 3PC. | [2017/013](https://eprint.iacr.org/2017/013).
- [MPECDSA](https://gitlab.com/neucrypt/mpecdsa) - Threshold multiparty ECDSA from ECDSA assumptions. | [S&P'19](https://eprint.iacr.org/2019/523.pdf).
- [ORAM (Obliv-C)](http://oblivc.org/sqoram/) - Oblivous RAM. | [S&P'16](http://oblivc.org/docs/sqoram.pdf).
- [PSI](https://github.com/encryptogroup/PSI) - Private Set Intersection. | [2014/447](https://eprint.iacr.org/2014/447).
- [ROOM](https://github.com/schoppmp/room-framework) - Read-Only Oblivious Maps and applications to secure machine learning on sparse data. | [CCS'19](https://eprint.iacr.org/2019/281.pdf).

### Tools
- [CBMC-GC](https://gitlab.com/securityengineering/CBMC-GC-2) - Creates Boolean circuits from ANSI-C code optimized for secure computation. | [ShallowCC](http://www.seceng.informatik.tu-darmstadt.de/assets/buescher/ShallowCC16.pdf).
- [Conclave](https://github.com/multiparty/conclave) - Big Data query compiler that combines cleartext processing with Spark and MPC protocols. | [EuroSys19](https://arxiv.org/abs/1902.06288).
- [HyCC](https://gitlab.com/securityengineering/HyCC) - Optimizes circuits for hybrid MPC from ANSI-C. | [CCS'18](https://thomaschneider.de/papers/BDKKS18.pdf).
- [MPC-SoK](https://github.com/MPC-SoK/frameworks) - Build environments for many MPC frameworks using Docker containers. | [S&P19](https://marsella.github.io/static/mpcsok.pdf).
- [Tiny-Garble](https://github.com/esonghori/TinyGarble) -  Logic Synthesis and Sequential Descriptions for Yao's Garbled Circuits. | [S&P'15](http://aceslab.org/sites/default/files/TinyGarble.pdf).
- [UC Compiler](https://github.com/encryptogroup/UC) - Valiant's Universal Circuit Compiler. | [2016/093](https://eprint.iacr.org/2016/093).

### Retired software

- [Duplo](https://github.com/AarhusCrypto/DUPLO) - 2PC with garbled circuits; secure against malicious adversaries.
- [FairPlayMP](https://github.com/FaiplayMP/FairplayMP) - GMW based multi-party protocol secure against semi-honest adversaries | [CCS'08](http://www.cs.huji.ac.il/project/Fairplay/FairplayMP/FairplayMP.pdf).
- [Frigate](https://bitbucket.org/bmood/frigaterelease) - C-style compiler for optimizing boolean circuits.  | [Euro S&P'16](https://www.cise.ufl.edu/~traynor/papers/mood-eurosp16.pdf).
- [Myst](https://github.com/OpenCryptoProject/Myst) - Secure Multiparty Key Generation, Signature and Decryption JavaCard applet and host application | [CCS'17](https://acmccs.github.io/papers/p1583-mavroudisA.pdf).
- [SDA](https://github.com/snipsco/sda) - Secure distributed aggregation of high-dimensional vectors | [2017/643](https://eprint.iacr.org/2017/643).
- [SPDZ](https://www.cs.bris.ac.uk/Research/CryptographySecurity/SPDZ/) - General MPC with secret sharing; secure against malicious adversaries | eprint: [2017/1230](https://eprint.iacr.org/2017/1230).
- [SPDZ-Yao](https://github.com/mkskeller/SPDZ-Yao) - 2PC with garbled circuits; high-level language similar to SPDZ; secure against semi-honest adversaries.
- [Semi-honest BMR](https://github.com/cryptobiu/Semi-Honest-BMR) - BMR protocol secure against semi-honest adversaries | [2016/1066](https://eprint.iacr.org/2016/1066).
- [Tasty](https://github.com/encryptogroup/tasty) - 2PC with garbled circuits and homomorphic encryption | [2010/365](https://eprint.iacr.org/2010/365).
- [TinyLEGO](https://github.com/AarhusCrypto/TinyLEGO) - 2PC with garbled circuits; secure against malicious adversaries | eprint: [2015/309](http://eprint.iacr.org/2015/309).
- [VIFF](http://viff.dk/) - 3+PC with secret sharing; secure against semi-honest adveraries.
- [Wysteria](https://bitbucket.org/aseemr/wysteria/wiki/Home) - Multparty computation with GMW, written in a functional PL; secure against semi-honest adversaries | [S&P'14](http://www.cs.umd.edu/~aseem/wysteria.pdf).


## Workshops

- [IIT Bombay MPC school](https://www.cse.iitb.ac.in/%7Emp/crypto/mpc2017/) - Covers basic and advanced topics related to the theory of MPC aimed at CS students and researchers interested in cryptography.
- [Securing Computation](https://simons.berkeley.edu/workshops/crypto2015-1) - Conducted at Simons institute for Theory of Computing.
- [The 1st BIU Winter School](http://cyber.biu.ac.il/event/the-1st-biu-winter-school/) - Introductory lectures for basic secure computation constructions.
- [The 5th BIU Winter School](http://cyber.biu.ac.il/event/the-5th-biu-winter-school/) - Tutorials and recent advances in secure computation delivered in video format.
- [TPMPC](http://www.multipartycomputation.com/) - Yearly workshop that started in Aarhus 2012. It has now become one of the biggest workshops for MPC people.

## Contribute

Contributions welcome! Read the [contribution guidelines](contributing.md) first.


## License

[![CC0](http://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](http://creativecommons.org/publicdomain/zero/1.0)

To the extent possible under law, Dragoș Rotaru has waived all copyright and related or neighboring rights to this work.

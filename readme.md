# awesome-mpc [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

Multiparty computation (MPC) allows several parties to jointly compute on secrets without revealing them. This list is designed to be a central place where everyone can find open-source software designed for MPC as well as introductory material to this topic.
The list format is inspired from [awesome list](https://github.com/sindresorhus/awesome) and after a fruitful lunch discussion at [TPMPC](http://www.multipartycomputation.com/) back in 2017 in Bristol.

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
- [FHE-MPC Advanced Grad Course](https://nigelsmart.github.io/FHE-MPC/) - 'Informal grad course' in FHE and MPC.
- [Secure Computation](https://www.csa.iisc.ac.in/~arpita/SecureComputation15.html) - Secure Computation course offered by Indian Institute of Science covering secret sharing schemes, oblivious transfer to impossiblity results and zero-knowledge proofs.
- [Secure Multi-Party Computation at Scale](https://piazza.com/bu/fall2017/cs591v1/info) - Boston University course that covers mathematical and algorithmic foundations of MPC, with an additional focus on deployment of state-of-the-art MPC technologies.

### Tutorials

- [Getting Started with MPC](https://yehudalindell.com/resources-for-getting-started-with-mpc/) - Light compilation of basic resources for getting started in MPC study and research.
- [How To Simulate It](https://eprint.iacr.org/2016/046) - A Tutorial on the Simulation Proof Technique.
- [OSU Bibliography](https://web.engr.oregonstate.edu/~rosulekm/scbib/index.php?n=Main.GettingStarted) - An Annotated Bibliography of Practical Secure Computation.
- [TinySMPC (tutorial)](https://github.com/kennysong/tinysmpc) – A tiny, educational, Pythonic library for SMPC. The tutorial notebook runs in your browser.
- [UC Security](https://www.youtube.com/playlist?list=PLqc9MPlwib9nSuyH4oUIwPsyDiZ4bwuEE) - Video lectures on UC security delivered by Ran Canetti.

## Misc

- [ePrint papers](https://guutboy.github.io) - Frequently updated list of secure computation papers appearing on IACR eprint.
- [MPC deployments](https://mpc.cs.berkeley.edu) - A hub for real-world MPC deployments maintained by UC
Berkeley EECS Security Group.

## Software

Here I tried to reference the most recent article found on specific software since enumerating all changes including the original paper is too cumbersome.

### Apps

- [2PC is for Lovers](https://voltrevo.github.io/2pc-is-for-lovers/) - Allows two people to find out if they are secretly in love with each other using malicious secure 2PC of a single AND gate.
- [MPC Hello](https://voltrevo.github.io/mpc-hello/) - Malicious secure 2PC calculating the larger of two numbers. Also a [template repository](https://github.com/voltrevo/mpc-hello) for building malicious secure 2PC web apps for any circuit.
- [TLS Notary](https://tlsnotary.org/) - Uses MPC to blindly sign TLS data, allowing users to make proofs about the content of data served to them over https.

### Frameworks

- [ABY](https://github.com/encryptogroup/ABY) - 2PC with secret sharing and garbled circuits; secure against semi-honest adversaries. | [NDSS'15](http://encrypto.de/papers/DSZ15.pdf).
- [ABY3](https://github.com/ladnir/aby3) - 3PC with secret sharing for privacy preserving machine learning and database joins (PSI, Union, etc.); secure against semi-honest adversaries. | [CCS'18](https://eprint.iacr.org/2018/403.pdf), [2019/518](https://eprint.iacr.org/2019/518.pdf).
- [BatchDualEx](https://github.com/osu-crypto/batchDualEx) - 2PC with garbled circuits; secure against malicious adversaries. | eprint: [2016/632](https://eprint.iacr.org/2016/632).
- [Carbyne Stack](https://carbynestack.io) - MPC cloud platform that combines state-of-the-art MPC with cloud-native technology like Kubernetes, Istio, and Knative to enable MPC deployments at scale.
- [CrypTen](https://github.com/facebookresearch/CrypTen) - MPC with secret sharing; secure against semi-honest adversary; focused on building PyTorch applications. | documentation: [link](https://crypten.ai/)
- [EMP-toolkit](https://github.com/emp-toolkit) - 2PC and MPC with garbled circuits; secure against semi-honest adversaries (emp-sh2pc). There are also ones resistant against malicious parties (emp-[ag2pc|m2pc|agmpc]) | eprint: [2017/189](https://eprint.iacr.org/2017/189), [2016/762](https://eprint.iacr.org/2016/762), [2017/030](https://eprint.iacr.org/2017/030).
- [EzPC](https://github.com/mpc-msri/EzPC) - Offers a suite of tools for secure machine learning using semi-honest MPC protocols. It includes a language for secure machine learning, compilers for TensorFlow/Onnx to various MPC protocols, and frameworks for training and inference on deep neural networks. It provides an end-to-end solution for secure machine learning. | documentation: [link](https://github.com/mpc-msri/EzPC). End-to-End Platform: [link](https://github.com/microsoft/private-benchmarking)
- [Fancy-Garbling](https://github.com/spaceships/fancy-garbling) - 2PC with arithmetic garbled circuits; secure against semi-honest adversaries. | eprint: [2016/969](https://eprint.iacr.org/2016/969).
- [FRESCO](http://fresco.readthedocs.io/en/latest/) - MPC supporting TinyTables or SPDZ protocols; secure against semi-honest or malicious adversaries. | [Practice'15](http://practice-project.eu/downloads/publications/D22.1-State-of-the-art-analysis-PU-V1.1.pdf).
- [HoneyBadgerMPC](https://github.com/initc3/HoneyBadgerMPC) - Robust MPC-based confidentiality layer for blockchains with guaranteed output delivery; secure against up to t < n/3 malicious parties.
- [HPMPC](https://github.com/chart21/hpmpc/) - HPMPC implements multiple MPC protocols and provides a high-level C++ interface to define functions and use cases. Out of the box, the framework supports computation in the boolean and arithmetic domain, mixed circuits, and fixed point arithmetic. Neural network models can be imported from PyTorch as part of [PIGEON](https://eprint.iacr.org/2024/1371.pdf).
- [JIFF](https://github.com/multiparty/jiff/) - JavaScript client and server libraries for building web-based applications that employ general purpose MPC; secure against semi-honest adversaries. | documentation: [link](https://multiparty.org/jiff/).
- [libTMCG](https://github.com/HeikoStamer/libtmcg) - C++ framework with various primitives and tools for implementing multiparty games; secure against semi-honest adversaries. | documentation: [link](https://www.nongnu.org/libtmcg/libTMCG.html/index.html)
- [Moose](https://github.com/tf-encrypted/moose) - 3PC with secret sharing; secure against semi-honest adversaries; focused on data processing and machine learning.
- [MOTION](https://github.com/encryptogroup/MOTION) - Mixed-Protocol MPC framework supporting full-threshold boolean and arithmetic GMW and BMR; secure against semi-honest adversaries. | eprint: [2020/1137](https://eprint.iacr.org/2020/1137).
- [MP-SPDZ](https://github.com/data61/MP-SPDZ) - MPC with garbled circuits or secret sharing; secure against malicious or semi-honest adversaries with dishonest or honest majority. | [documentation](https://mp-spdz.readthedocs.io/en/latest/) | eprint: [2020/512](https://eprint.iacr.org/2020/521)
- [MPC Framework](https://github.com/voltrevo/mpc-framework) - TypeScript framework for doing MPC with multiple techniques for generating circuits and MPC backends. In particular, it supports [summon](https://github.com/voltrevo/summon) circuits and [emp-wasm-backend](https://github.com/voltrevo/emp-wasm-backend) for malicious secure 2PC.
- [MPZ](https://github.com/privacy-scaling-explorations/mpz) - A collection of multi-party computation libraries written in Rust 🦀. Strives to provide safe, performant, modular and portable MPC software with a focus on usability.
- [MPyC](https://www.win.tue.nl/%7Eberry/mpyc/) - BGW honest majority multi-party protocol; secure against semi-honest adversaries. | [TPMPC'18](https://www.win.tue.nl/~berry/mpyc/TPMPC2018.pdf).
- [Obliv-C](http://oblivc.org/) - 2PC with garbled circuits; secure against semi-honest adversaries. | eprint: [2015/1153](http://eprint.iacr.org/2015/1153).
- [Obliv-Java](https://github.com/Calctopia-OpenSource/jdk10u) - Faithful reimplementation of Java using Obliv-C. | eprint: [2017/878](https://eprint.iacr.org/2017/878)
- [Rosetta](https://github.com/LatticeX-Foundation/Rosetta/) - 3PC with secret sharing; secure against semi-honest adversaries; focused on reusing the APIs of TensorFlow and allowing to transfer traditional TensorFlow codes into a privacy-preserving manner with minimal changes.
- [SecretFlow-SPU](https://github.com/secretflow/spu) - A domain-specific compiler and runtime suite, that aims to provide a secure computation service with provable security. SPU compiler uses XLA as its front-end Intermediate Representation (IR) and SPU runtime implements various MPC protocols. | [USENIX ATC'23](https://www.usenix.org/system/files/atc23-ma.pdf).
- [Sharemind](https://sharemind.cyber.ee/) - 2PC or 3PC with secret sharing; secure against semi-honest adversaries. | [Cyber'13](https://cyber.ee/research/theses/roman_jagomagis_msc.pdf).
- [swanky](https://github.com/GaloisInc/swanky) - A suite of rust libraries for secure multi-party computation (currently includes oblivious transfer, garbled circuits, and private set intersection).
- [Tandem](https://github.com/sine-fdn/tandem) - 2PC with garbled circuits written in Rust; secure against malicious adversaries.
- [TF Encrypted](https://github.com/mortendahl/tf-encrypted/) - 3PC with secret sharing; secure against semi-honest adversaries; focused on TensorFlow-based applications.
- [TNO-MPC](https://github.com/TNO-MPC/) - Collection of MPC generic software components, procedures, functionalities, and solutions based on secret sharing and (partially) homomorphic encryption developed in Python and Go. | Blogs and principles: [TNO MPC Lab](https://mpc.tno.nl/).

### Primitives

- [aes-prng](https://github.com/tf-encrypted/aes-prng) - Rust pseudo-random number generator based on AES.
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
- [Fireblocks MPC](https://github.com/fireblocks/mpc-lib/) - Multiparty ECDSA and EdDSA | eprint [2020/492](https://eprint.iacr.org/2020/492).
- [LibPSI](https://github.com/osu-crypto/libPSI) - Various protocols for performing private set intersection.
- [Linreg](https://github.com/schoppmp/linreg-mpc/) - Privacy preserving linear regression. | [2016/892](https://eprint.iacr.org/2016/892).
- [Geppetri](https://github.com/meilof/geppetri) - Verifiable 3PC. | [2017/013](https://eprint.iacr.org/2017/013).
- [MPECDSA](https://gitlab.com/neucrypt/mpecdsa) - Threshold multiparty ECDSA from ECDSA assumptions. | [S&P'19](https://eprint.iacr.org/2019/523.pdf).
- [ORAM (Obliv-C)](http://oblivc.org/sqoram/) - Oblivous RAM. | [S&P'16](http://oblivc.org/docs/sqoram.pdf).
- [Prio](https://github.com/mozilla/libprio) - Private aggregation with SNIPs (secret-shared non-interactive proofs). | [NSDI'17](https://crypto.stanford.edu/prio/paper.pdf).
- [PSI](https://github.com/encryptogroup/PSI) - Private Set Intersection. | [2014/447](https://eprint.iacr.org/2014/447).
- [ROOM](https://github.com/schoppmp/room-framework) - Read-Only Oblivious Maps and applications to secure machine learning on sparse data. | [CCS'19](https://eprint.iacr.org/2019/281.pdf).

### Tools
- [CBMC-GC](https://gitlab.com/securityengineering/CBMC-GC-2) - Creates Boolean circuits from ANSI-C code optimized for secure computation. | [ShallowCC](https://web.archive.org/web/20180205110742/http://www.seceng.informatik.tu-darmstadt.de/assets/buescher/ShallowCC16.pdf).
- [CipherCompute](https://github.com/Cosmian/CipherCompute) - Create generic MPC programs using [Rust](https://www.rust-lang.org/). Works on top of the [SCALE](https://github.com/KULeuven-COSIC/SCALE-MAMBA) engine. Enterprise software that provides UIs for participants handshaking, computations approval, datasources connections, auditing etc...
- [Circom 2 Arithc](https://github.com/namnc/circom-2-arithc/) - Compiles bristol circuits for MPC from circom code.
- [Conclave](https://github.com/multiparty/conclave) - Big Data query compiler that combines cleartext processing with Spark and MPC protocols. | [EuroSys19](https://arxiv.org/abs/1902.06288).
- [Garble-Lang](https://github.com/sine-fdn/garble-lang) - Programming language for MPC with Garbled Circuits. Garble is statically typed, low-level, purely functional and uses a syntax heavily inspired by Rust.
- [HyCC](https://gitlab.com/securityengineering/HyCC) - Optimizes circuits for hybrid MPC from ANSI-C. | [CCS'18](https://thomaschneider.de/papers/BDKKS18.pdf).
- [MPC-SoK](https://github.com/MPC-SoK/frameworks) - Build environments for many MPC frameworks using Docker containers. | [S&P19](https://marsella.github.io/static/mpcsok.pdf).
- [Private Benchmarking](https://github.com/microsoft/private-benchmarking) - Provides an End to End platform to perform Private Benchmarking using MPC and GPU-based Confidential Computing on LLMs/CNNs/Vision Models using [EzPC](https://github.com/mpc-msri/EzPC) framework. | [eprint](https://arxiv.org/abs/2403.00393).
- [Summon](https://github.com/voltrevo/summon) - A TypeScript-like language for compiling bristol circuits for MPC. Also available as an [npm module](https://www.npmjs.com/package/summon-ts).
- [Tiny-Garble](https://github.com/esonghori/TinyGarble) -  Logic Synthesis and Sequential Descriptions for Yao's Garbled Circuits. | [S&P'15](http://aceslab.org/sites/default/files/TinyGarble.pdf).
- [UC Compiler](https://github.com/encryptogroup/UC) - Valiant's Universal Circuit Compiler. | [2016/093](https://eprint.iacr.org/2016/093).

### Retired software

- [Duplo](https://github.com/AarhusCrypto/DUPLO) - 2PC with garbled circuits; secure against malicious adversaries.
- [FairPlayMP](https://github.com/FaiplayMP/FairplayMP) - GMW based multi-party protocol secure against semi-honest adversaries | [CCS'08](http://www.cs.huji.ac.il/project/Fairplay/FairplayMP/FairplayMP.pdf).
- [Frigate](https://bitbucket.org/bmood/frigaterelease) - C-style compiler for optimizing boolean circuits.  | [Euro S&P'16](https://www.cise.ufl.edu/~traynor/papers/mood-eurosp16.pdf).
- [Myst](https://github.com/OpenCryptoProject/Myst) - Secure Multiparty Key Generation, Signature and Decryption JavaCard applet and host application | [CCS'17](https://acmccs.github.io/papers/p1583-mavroudisA.pdf).
- [SCALE-MAMBA](https://nigelsmart.github.io/SCALE/) - General MPC with secret sharing; secure against various adversaries including malicious with a dishonest majority. Software closer to a production system. | documentation: [link](https://nigelsmart.github.io/SCALE/Documentation.pdf).
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
- [The 1st BIU Winter School](https://web.archive.org/web/20230604031948/http://cyber.biu.ac.il/event/the-1st-biu-winter-school/) - Introductory lectures for basic secure computation constructions.
- [The 5th BIU Winter School](https://web.archive.org/web/20230601080023/https://cyber.biu.ac.il/event/the-5th-biu-winter-school/) - Tutorials and recent advances in secure computation delivered in video format.
- [TPMPC](http://www.multipartycomputation.com/) - Yearly workshop that started in Aarhus 2012. It has now become one of the biggest workshops for MPC people.

## Contribute

Contributions welcome! Read the [contribution guidelines](contributing.md) first.


## License

[![CC0](http://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](http://creativecommons.org/publicdomain/zero/1.0)

To the extent possible under law, Dragoș Rotaru has waived all copyright and related or neighboring rights to this work.

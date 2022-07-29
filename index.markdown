---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

# The 9th Workshop on Formal Reasoning in Distributed Algorithms

Date: August 11th 2022

The workshop is organized as part of [FLoC 2022](https://www.floc2022.org/workshops).

*Walk-in registration* is still possible: [https://www.floc2022.org/registration](https://www.floc2022.org/registration)

## News

* July 29: titles and abstracts are complete!
* July 21: added tentative program
* July 7: added more speakers
* June 13th: added first two speakers and registration link
* May 23rd: website created!

## Program

Tentative program:
* 9:00-9:45: Hagit Attiya, Technion
    <details>
    <summary>Preserving Hyperproperties when Using Concurrent Objects (click to expand the abstract)</summary>
      <br>
      <p>
        Linearizability, a consistency condition for concurrent objects, is known to preserve trace properties.
        This suffices for modular usage of concurrent objects in applications, deriving their safety properties from the abstract object they implement.
        However, other desirable properties, like average complexity and information leakage, are not trace properties.
        These *hyperproperties* are not preserved by linearizable concurrent objects, especially when randomization is used.
        This talk will discuss formal ways to specify concurrent objects that preserve hyperproperties and their relation with verification methods like forward /           backward simulation.
        We will show that certain concurrent objects cannot satisfy such specifications, and describe ways to mitigate these limitations. 
      </p>
    </details>
* 9:45-10:30: Yoram Moses, Technion
    <details>
    <summary>On Direct and Indirect Information in Distributed Protocols (click to expand the abstract)</summary>
      <br>
      <p>
        I will discuss the role and uses of direct and indirect information in distributed protocols. In particular, I will describe a protocol based on indirect information whose formal verification is offered as an interesting challenge. 
      </p>
    </details>
* --Coffee Break--
* 11:00-11:45: Constantin Enea, Ecole Polytechnique, LIX
    <details>
    <summary>Quorum Tree Abstractions of Consensus Protocols (click to expand the abstract)</summary>
      <br>
      <p>
        Distributed algorithms solving agreement problems like consensus or state machine replication are essential components of modern fault-tolerant distributed services. They are also notoriously hard to understand and reason about. Their complexity stems from the different assumptions on the environment they operate with, i.e., process or network link failures, Byzantine failures etc. In this talk, I will describe a novel abstract representation of the dynamics of such protocols which focuses on quorums of responses (votes) to a request (proposal) that form during a run of the protocol. We show that focusing on such quorums, a run of a protocol can be viewed as working over a tree structure where different branches represent different possible outcomes of the protocol, the goal being to stabilize on the choice of a fixed branch. This abstraction resembles the description of recent protocols used in Blockchain infrastructures, e.g., the protocol supporting Bitcoin or Hotstuff. We show that this abstraction supports reasoning about the safety of various algorithms, e.g., Paxos, PBFT, Raft, and HotStuff, in a uniform way. In general, it provides a novel induction based argument for proving that such protocols are safe. This is joint work with Berk Cirisci and Suha Orhun Mutluergil. 
      </p>
    </details>
* 11:45-12:30: Ori Lahav, Tel Aviv University
    <details>
    <summary>What's Decidable about Causally Consistent Shared Memory? (click to expand the abstract)</summary>
      <br>
      <p>
        While causal consistency is one of the most fundamental consistency models weaker than sequential consistency, the decidability of safety verification for (finite-state) concurrent programs running under causally consistent shared-memories is still unclear. We establish the decidability of this problem for two standard and well-studied variants of causal consistency. To do so, for each of the variants, we develop an equivalent "lossy" operational semantics, and show that it constitutes a well-structured transition system, which enables decidable verification. The two novel semantics are based on similar key observations, which, we believe, may also be of independent use in the investigation of weakly consistent shared memory models and their verification. Interestingly, our results are in contrast to the undecidability of this problem under the Release/Acquire fragment of the C/C++11 memory model, which forms another variant of a causally consistent memory that, in terms of allowed outcomes, lies strictly between the two models we study. Nevertheless, all these variants coincide for write/write-race-free programs, which implies the decidability of verification for such programs under Release/Acquire.
(Joint work with Udi Boker, partly presented at PLDI'20)
      </p>
    </details>
* --Lunch Break--
* 14:00-14:45: Bernhard Kragl, AWS
    <details>
    <summary>Using Lightweight Formal Methods to Validate a Key-Value Storage Node in Amazon S3 (click to expand the abstract)</summary>
      <br>
      <p>
        This talk reports our experience applying lightweight formal methods to validate the correctness of ShardStore, a new key-value storage node implementation for the Amazon S3 cloud object storage service. By "lightweight formal methods" we mean a pragmatic approach to verifying the correctness of a production storage node that is under ongoing feature development by a full-time engineering team. We do not aim to achieve full formal verification, but instead emphasize automation, usability, and the ability to continually ensure correctness as both software and its specification evolve over time. Our approach decomposes correctness into independent properties, each checked by the most appropriate tool, and develops executable reference models as specifications to be checked against the implementation. Our work has prevented 16 issues from reaching production, including subtle crash consistency and concurrency problems, and has been extended by non-formal-methods experts to check new features and properties as ShardStore has evolved.
      </p>
* 14:45-15:30: Ilina Stoilkovska, Amazon
    <details>
    <summary>Eliminating Message Counters in Threshold Automata (click to expand the abstract)</summary>
      <br>
      <p>
        Threshold automata were introduced to give a formal semantics to distributed algorithms in a way that supports automated verification. While transitions in threshold automata are guarded by conditions over the number of globally sent messages, conditions in the pseudocode descriptions of distributed algorithms are usually formulated over the number of locally received messages. In this talk, we present an automated method to close the gap between these two representations. We propose threshold automata with guards over the number of received messages and present abstractions into guards over the number of sent messages, by eliminating the receive message counters. Our approach allows us for the first time to fully automatically verify models of both synchronous, asynchronous, and randomized distributed algorithms that are in one-to-one correspondence with their pseudocode. 
      </p>
    </details>

## Summary of the workshop

Distributed algorithms is an active research field; their applications range
from Internet applications over cloud computing to safety-critical control
systems. Whereas many applications are of critical importance, the correctness
of distributed algorithms is usually based on very subtle mathematical
arguments. Consequently, one easily can make mistakes with hand-written proofs,
which reduces the trust in the correctness of these systems.

In the last decades, formal methods were proven to be useful for the
verification of many hardware and software systems. For distributed algorithms,
the application of formal methods was limited: formal methods have been used
for finding bugs in distributed algorithms, and to a much smaller extent formal
methods were used in computer-aided verification of simple distributed
algorithms. However, to verify more involved distributed algorithms, one cannot
easily apply existing verification tools. To be eventually able to do this, an
interdisciplinary effort from the concerned fields of formal methods, logic in
computer science, and distributed algorithm theory is required.

The topics of interest for the FRIDA workshop include the following topics, as
they apply to distributed algorithms and systems:

* formal modeling
* model checking
* interactive theorem proving
* parameterized model checking
* integration of different verification techniques
* benchmarking
* synthesis
* run-time verification
* testing
* invariant inference


## Organizers

### Main organizers
* [Marijana Lazić](https://www7.in.tum.de/~lazic/) [(email)](mailto:lazic@in.tum.de)
* [Swen Jacobs](https://cispa.de/en/people/swen.jacobs)
### With support of
* Igor Konnov
* [Giuliano Losa](https://www.losa.fr/) [(email)](mailto:giuliano@losa.fr)
* Stephan Merz
* Joseph Widder

## Previous editions

Starting a productive dialogue between distributed algorithms and verification
communities was the goal of a successful [Dagstuhl Seminar “Formal Verification
of Distributed Algorithms”](https://www.dagstuhl.de/en/program/calendar/semhp/?semnr=13141)
which was held in April 2013. During this seminar,
the participants agreed that a series of workshops should be held in order to
strengthen the community that does research on these issues.

The [1st workshop on Formal Reasoning in Distributed
Algorithms](https://easychair.org/smart-program/VSL2014/FRIDA-index.html) took
place in Vienna as part of the Vienna Summer of Logic’14 and Federated Logic
Conference’14. The [2nd FRIDA
workshop](http://discotec2015.inria.fr/workshops/frida-2015/) took place in
Grenoble as part of FORTE’15. The [3rd FRIDA
workshop](https://forsyte.at/events/frida2016/) was organized in Marrakech as
part of NETYS’16. The [4th FRIDA
workshop](https://forsyte.at/events/frida2017/) took place in Vienna as part of
DISC 2017. The [5th FRIDA workshop](https://forsyte.at/events/frida2018/) was
co-located with CAV 2018, which was held as part of the Federated Logic
Conference (FLoC). The [6th
workshop](https://team.inria.fr/veridis/events/frida2019/) was co-located with
DISC 2019 in Budapest, Hungary. Finally, [FRIDA 2020](https://frida2020.galois.com/) and [FRIDA 2021](frida-2021.github.io) took place as an online workshops at QONFEST 2020 and DISC 2021, respectively.

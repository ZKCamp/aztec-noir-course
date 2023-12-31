# ZKCamp's Aztec Noir Course

## About Aztec
Aztec is a first-of-its-kind hybrid zkRollup supporting both public and private smart contract execution.  It will allow developers to build fully programable, privacy preserving smart contracts, with composable call semantics using our ZK-Snark programming language, Noir.

## About ZKCamp
[ZKCamp](www.zkcamp.xyz) is a ZK education company. ZKCamp's primary offering is a live cohort-based course that teaches ZKPs and their underlying mathematical and cryptographic principles using hands-on examples and engaging assessments. The course is tailored for engineers who do not have a math or cryptography background but are eager to learn it. Through a structured curriculum and live sessions with instructors, participants will have the opportunity to learn and engage with the material in a collaborative environment. Upon completion of the course, participants will have the knowledge and skills necessary to build decentralized applications based on ZKPs.


## What is this course about?

Zero-knowledge proofs (ZKP) have been gaining tremendous traction in the blockchain space, came up first as a privacy solution and increasingly as a scaling solution.

Noir, Aztec's language for programming zero knowledge circuits, offers a unique, easy approach to building applications that leverage zero knowledge proofs. Most ZK frameworks require advanced cryptography expertise, but Noir abstracts away much of the complexity to open up zkApp development to the broader pool of web 3.0 developers.

The shift from traditional development to building ZKP applications with Noir introduces a new set of concepts and tools that may seem overwhelming at first. Aztec collaborated with ZKCamp.xyz to launch the first live cohort to teach Noir to a set of 30 developers durind Aug 13-18, 2023. 

 The course, led by the instructors at ZKCamp and sponsored by Aztec, is tailored for engineers who do not have a math or cryptography background but are eager to learn it. Through a structured curriculum and live sessions with instructors, participants had the opportunity to learn and engage with the material in a collaborative environment. 

## Prerequisites

1. Read this [blog](https://www.zkcamp.xyz/blog/what-is-a-zkp-anyway) to make sure you have a basic understanding of what zero-knowledge proofs are all about.
2. Zero-knowledge proofs are based on certain mathematical primitives. Read the blogs below to get a basic understanding of the underlying mathematics

    * [Polynomials](https://www.zkcamp.xyz/blog/you-cant-understand-zkps-without-understanding-polynomials)

    * [Modular Math](https://www.zkcamp.xyz/blog/why-we-use-modular-math-for-zero-knowledge-proofs)

3. Read this [blog](https://www.zkcamp.xyz/blog/information-theory) to get an introduction to Information Theory.

4. To build applications with Noir, you need to know basics of solidity. Learn the basics of Solidity, if you aren’t familiar with it already, through this short [course](https://cryptozombies.io/en/solidity).

5. [Set up the Noir development environment](https://noir-lang.org/getting_started/nargo_installation/#option-1-noirup).

## Lectures & course materials
Lectures are of 90 min each. Each of the items below has the lecture recording, slides, quizzes and assignments associated with the lecture

<details>
<summary><b>&nbsp;Lecture 1 - Cohort Introduction & ZKP Fundamentals</b></summary>
<br/>
The first lecture reviews the curriculum and covers some of the Zero-Knowledge Proofs fundamentals that will be useful for future lectures. The lecture ends with a meet and greet session amongst the ZKCampers in the cohort.

<br/>
<li><a href = "https://youtu.be/3tuQP3Su1r4">Recording</a></li>
<li><a href = "https://docs.google.com/presentation/d/e/2PACX-1vR7nYLpmDcvo61PXX1t_uDdHjAFpAyJRAHYVSY0Ogzt6K6_eZgVZQAXRxIAQI4znf2gba2IE59trzCv/pub?start=false&loop=false&delayms=3000">Slides</a></li>
</details>

<details>
<summary><b>&nbsp;Lecture 2 - Introduction to Aztec Ecosystem</b></summary>
<br/>
In this lecture, Josh, from developer relations at Aztec, provides an introduction to Aztec. The lecture touches upon the history of Aztec, its differentiation from other L1/L2 protocols, Aztec's architecture, Noir's place within the Aztec ecosystem, and the future roadmap for Aztec.

<br/>
<li><a href = "https://youtu.be/w8blpTC4O9Y">Recording</a></li>
<li><a href = "https://docs.google.com/presentation/d/13ZYuCStLETBojSshZ1NIorDFa3dqirvJKCE2yjoqCMY/preview?usp=embed_googleplus">Slides</a></li>
</details>

<details>
<summary><b>&nbsp;Lecture 3 - Noir Basics</b></summary>
<br/>
This lectures explores the foundational concepts of the Noir language by examining a series of Noir programs. The lecture discusses topics such as Primitive and Compound Data Types, Constraints, and writing tests.

<br/>
<li><a href = "https://youtu.be/fKH3r8cDD_Y">Recording</a></li>
<li><a href = "https://docs.google.com/presentation/d/e/2PACX-1vTRpVg9MbqNSwzHXsgJzWopxmbfPO3Lc-ZAeqA73hlrsj_B7LptI1_dDWXOwCNhjmRS48zHkTEpb4dY/pub?start=false&loop=false&delayms=3000">Slides</a></li>
<li><a href="./quiz/noir-basics.md">Quiz - Noir Basics</a></li>
<li><a href="./quiz/noir-basics-solutions.md">Quiz Solutions - Noir Basics</a></li>
<li><a href="https://github.com/ZKCamp/noir-toy-hashing-assignment">Assignment - Toy hashing alogrithm in Noir</a></li>
</details>

<details>
<summary><b>&nbsp;Lecture 4 - Building a Noir Application - Part 1</b></summary>
<br/>
Just knowing the Noir programming language is not enough. To build private and decentralized applications, one needs to learn how to setup a project, use Noir CLI, generate a verifier contract, and also integrate it with the frontend. 
In the first part of a two part lecture series, students learn how to build a private DAO app in Noir from scratch. Students are also introduced to couple of ZK primitives - Identity Commitment and Merkle Trees.
<br/>
<li><a href = "https://youtu.be/DsuhSVXSB5w">Recording</a></li>
<li><a href = "https://docs.google.com/presentation/d/e/2PACX-1vRZXMqGfC627bK0zVODX6URgiZAhurbhxULWIgLzSigvuRmUJ4YmAP4Sv09fJ96lf-CPAG2uFPrweoY/pub?start=false&loop=false&delayms=3000">Slides</a></li>
<li> 
    Reading Material - Refer to the following branches of <a href="https://github.com/ZKCamp/noir-voting">this</a> repo
    <ul>
        <li><a href = "https://github.com/ZKCamp/noir-voting/tree/1-identity-commitments">1-identity-commitments</a></li>
        <li><a href = "https://github.com/ZKCamp/noir-voting/tree/2-merkle-trees">2-merkle-trees</a></li>
    </ul>

</li> 
</details>

<details>
<summary><b>&nbsp;Lecture 5 - Building a Noir Application - Part 2</b></summary>
<br/>
Part 2 of Building a Noir Application introduces the steps to generate, compose and test a Solidity Smart contract to manage the Private Voting for the DAO. Students are also introduced to the ZK primitive - Nullifers. Finally, students learn how to use Noir in the browser.

<br/>
<li><a href = "https://youtu.be/UZiUfh5eO7I">Recording</a></li>
<li><a href = "https://docs.google.com/presentation/d/e/2PACX-1vQ-L6f9yc-zoCPrkVuOPphsZC1H6HOU--N03AxR3lmDyE83mYCaB4gnA-BSuYOvBiHX6E_KXg-UpSjN/pub?start=false&loop=false&delayms=3000">Slides</a></li>
<li><a href = "https://github.com/ZKCamp/stealthdrop-assignment">Assignment - StealthDrop in Noir</a></li>
<li> 
    Reading Material - Refer to the following branches of <a href="https://github.com/ZKCamp/noir-voting">this</a> repo
    <ul>
        <li><a href = "https://github.com/ZKCamp/noir-voting/tree/3-smart-contracts">3-smart-contracts</a></li>
        <li><a href = "https://github.com/ZKCamp/noir-voting/tree/4-nullifier">4-nullifier</a></li>
        <li><a href = "https://github.com/ZKCamp/noir-voting/tree/5-integration-tests">5-integration-tests</a></li>
    </ul>

</li> 
</details>

<details>
<summary><b>&nbsp;Lecture 6 - Advanced Noir</b></summary>
<br/>
The first part of this lecture does a deep dive into topics such as Noir's novel intermediate representation (ACIR), constraints optimizations, and security. During the second half, Josh from Aztec covers topic like Recursion, Storage Proofs in Ethereum. He then sheds light on how students can actively participate in Noir through Aztec's grant initiatives.

<br/>
<li><a href = "https://youtu.be/jghEF5WQ5G8">Recording</a></li>
<li><a href = "https://docs.google.com/presentation/d/e/2PACX-1vSamWI7cXmA8LxkBqMrHG983saaThhLsuc5h45dhbOvGeG2n5-MuR7lBcLqpBjIqQHFp2t2uL50HNIz/pub?start=false&loop=false&delayms=3000">Slides (Rajesh)</a></li>
<li><a href = "https://docs.google.com/presentation/d/1FTiDRAAGBvs7UiQMQTcqeS6uO4ko2CbhRfU4c80k9LM/edit#slide=id.g23d1b8ba2aa_0_199">Slides (Josh)</a></li>
<li> 
    Reading Material - Refer to the following branches of <a href="https://github.com/ZKCamp/noir-voting">this</a> repo
    <ul>
        <li><a href = "https://github.com/ZKCamp/noir-voting/tree/6-security">6-security</a></li>
    </ul>

</li> 
</details>
<br/>

---
title: Nonperturbative Aspects of Quantum Field Theory in Curved Spacetime
description: >
    My master's thesis focused on using the functional renormalization group to understand the nonperturbative behavior of a particle detector model. Here's an overview. 
type: thesis
date: 2023-04-28
last_modified_at: 2026-01-19
tags: 
    - QFTCS 
    - AQFT 
    - FRG
post_type: paper-note
related_publications:
    - "2305.17453"
---
One of the hardest problems in fundamental physics is to understand the quantum nature of gravity. On the road to doing so, it has been useful to consider how quantum mechanics effects occur in the presence of strong gravitational fields. A good framework for this is that of quantum field theory in curved spacetime (QFTCS). In this framework, one considers the behavior of quantum fields—the building blocks of the standard model of particle physics, for example—on top of a classical background spacetime. It therefore consists of an approximation in which gravity behaves classically, but matter is quantized. 

One interesting application of QFTCS is to the field of relativistic quantum information (RQI). One may ask oneself how quantum mechanics can be used to convey information between two observers, and in particular how the structure of spacetime affects the possibilities of communication. These questions are addressed by RQI. Within this paradigm, {% include ref.html key='landulfo2016Nonperturbative' text='Landulfo (2016)' %} has described a communication protocol in which two experimentalists couple a two-level quantum system (a qubit) to a quantum field and communicate by performing measurements on the qubits. Some important features of this model are the following.
1. It can be solved exactly (something extremely rare in quantum field theory) due to the particular choice of coupling;
2. the results obtained hold for a large class of spacetimes;
3. it is not necessary to choose an arbitrary notion of "particles" in formulating the model;
4. the quantum state of the field can belong to a large class of "vacuum-like" states;
5. both sender and receiver are allowed to have arbitrary trajectories through spacetime;
6. both sender and receiver interact with the quantum field within bounded regions of spacetime;
7. the protocol allows the transmission of classical information (bits with 0 or 1 values);
8. the protocol explicitly forbids faster-than-light communication.

All of these are great advantages, but the model still has a couple of drawbacks. For instance, one cannot transmit quantum information (qubit states) without the aid of extra entanglement between the parts and one cannot harvest entanglement from the quantum fields. Moreover, one cannot use the qubits as particle detectors. This is inconvenient because particle detector models are very useful in studying both QFTCS and RQI and even date back to the original derivation of the Unruh effect {% include ref.html key='unruh1976Notes' text='(Unruh 1976)' %}.

To improve on these aspects, one needs to change the coupling of the model to introduce a "gap" in the qubit. Namely, Landulfo's original model assumes a two-level system in which both levels have the same energy. This leads to all of the good features of the model (in particular the fact that it is exactly solvable), but it also leads to the drawbacks. Adding an energy gap (so that the two levels have different energies) improves the drawbacks but at the cost of the exact solution.

Most work in RQI is perturbative, so it would be interesting to obtain nonperturbative information about this behavior. One possible way of doing this is to study the model perturbatively, but account for nonperturbative corrections by exploiting the functional renormalization group running of the theory. While this is still an approximate solution, it allows one to obtain nonperturbative information, hence allowing the investigation of a regime often overlooked. 

## Quantum Field Theory in Curved Spacetime

The first step in this journey is then to understand QFTCS. While quantum field theory in flat spacetime is often formulated in terms of canonical quantization or the path integral approach, these methods seem too arbitrary to allow a satisfactory formulation in general spacetimes. A more general approach is then the algebraic approach. 

The algebraic approach focuses on describing the observables in the theory and then considering the possible states. An observable is anything that can be measured through an experiment, and a state gives you the (probabilistic) outputs of any possible experiment for a given preparation of the system. One can argue that the space of observables must have an algebraic structure (at least a *-algebra, typically), allowing one to get a powerful mathematical machinery to study quantum field theory.

A sociological disadvantage of the algebraic approach is the fact it involves a lot of functional analysis, which not all physicists are familiar with. In my thesis, I present the main ideas of the algebraic approach without assuming previous knowledge of functional analysis. While this naturally leads to limitations because less mathematical machinery is available, one can still get a good grasp of what a quantum field theory is. This clarifies concepts such as what are particles and how they are a subjective concept, or how the notion of a Hilbert space is not truly the fundamental defining feature of a quantum theory. 

As an example of prediction of QFTCS, one can then consider the Unruh effect, which is central for this work: a simple application of the generalization of Landulfo's model would be to study communication between an inertial and an accelerated particle detector, the latter being subject to the Unruh thermal bath. In my thesis, I discuss four different derivations of the Unruh effect: the algebraic derivation based on the notion of KMS states, the canonical approach based on Bogoliubov transformations, the path integral approach, and the particle detector approach. These different techniques showcase different aspects of the effect and work under different assumptions, hence giving a more complete view of what the Unruh effect is. 

In the remainder of the thesis, most of the techniques employed are focused on Euclidean path integral methods, which are essential in the traditional formulation of the FRG (but {% include ref.html key="dangelo2024AlgebraicQFTApproach" text="D'angelo _et al_. (2024)" %} have recently presented an algebraic version of the FRG in Lorentzian spacetimes). I therefore discuss the basic ideas behind Euclidean path integrals and when it is possible to employ a Euclidean path integral in curved spacetimes. 

With these discussions accounted for, it is possible to go further and discuss the FRG. 

## Functional Renormalization Group

The functional renormalization group is a nonperturbative realization of the renormalization group. While it has many different incarnations, the one I worked with is focused on the so-called Wetterich equation. This is a functional differential equation describing how the effective average action (a quantum version of the classical action) changes as one changes the scales being considered. 

This technique is quite general in quantum field theory and can be applied to many different systems. Nevertheless, most pedagogical approaches to the FRG derive the Wetterich equation in the particular case of a bosonic field content. Nevertheless, it turns out that for our applications we need a formulation that also admits fermions. This form is already known in the literature, but it is difficult to find a pedagogical derivation of it, so I included it in my thesis. 

Once one has the main equation at hand, there are a few steps necessary to compute a nonperturbative renormalization group flow. They are as follows. 
1. One must choose an action to describe the theory. The actual exact theory has an infinitely complicated action, so the typical approach is to choose a truncation, i.e., a simplified action that ideally captures most of the physics we are interested in.
2. One must choose a regulator, which is a function responsible for screening out the modes that should not contribute at each scale we are analyzing. There are many possible choices given in the literature, but the choice of regulator must be specific to the theory at hand to avoid problems.
3. One needs to compute the difficult functional traces involved in the Wetterich equation. This can often be done by exploiting heat kernel techniques (reviewed in the thesis). 

The main questions are then the following. 
1. How can we formulate the generalized Landulfo model in terms of an action (since the original formulation uses a canonical approach)?
2. What would be an adequate regulator for this model?
3. How do we compute the necessary functional traces?

## Nonperturbative Renormalization Group Flow for a Particle Detector

To keep the calculations feasible (in particular the functional traces), we assume the detector is undergoing inertial motion in Minkowski spacetime. 

The formulation of a particle detector through a path integral formalism was addressed by {% include ref.html key="burbano2021PathIntegralFormulation" text="Burbano, Perche, and Torres (2021)" %}. One can write the detector variables in terms of Grassmann variables (anticommuting variables) on the detector's worldline. While some attention must be paid to the interaction between the detector and field to the properly described, the construction is straightforward.

Next, there is the issue of the regulator. In standard quantum field theories, the regulator is similar to a mass term, since masses suppress modes with very low energies. In a particle detector, the gap term plays the role of a gap term, so the chosen regulator was a gap-like term. 

The computation of the functional traces is tricky but manageable. Due to the occurrence of derivatives in the denominator of the function inside the functional trace, it is necessary to perform a Taylor-like expansion, compute each term using standard heat kernel techniques, and then resum the series. The results are complicated functions expressed in terms of integrals of hypergeometric functions.

After all these steps, one arrives at the expressions for the nonperturbative renormalization group flow for the system. Unfortunately, the results diverge in the gapless limit, which would be the case in which Landulfo's original results should be recovered. This indicates a problem in the calculation. 

As sanity checks, the one-loop calculation and a different technique for the evaluation of some functional traces were considered. The one-loop calculation did not present any issues, while the alternative evaluation of functional traces yielded the same results as the heat kernel techniques.

## Conclusions

At the time of publication of this thesis, the reasons for the failure of the nonperturbative calculation were still unknown, but since then they have been resolved and will be addressed in future publications. 

The thesis also presents important pedagogical contributions through the presentations of the algebraic approach to QFTCS and of the FRG for generic field content. 
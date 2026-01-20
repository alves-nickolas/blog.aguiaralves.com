---
title: Killing horizons naturally define asymptotic symmetries
description: >
    This may be an interesting path for new forms of holography in fundamental physics. Interestingly, it also suggests new asymptotic symmetries at null infinity, which in turn could hint at a theory of modified gravity. 
date: 2025-09-22
last_modified_at: 2026-01-19
tags: 
    - IRStructure 
    - GR 
    - QFTCS
post_type: paper-note
related_publications:
    - "2504.12514"
---
Symmetry is a guiding principle throughout physics. In a sense, one could say the study of physics is the pursuit of what the underlying symmetries of the universe are. Recently, a lot of attention has been given to the so-called asymptotic symmetries—the symmetries that emerge in spacetime as one asymptotically approaches a limiting surface. 

Of particular notice are the Bondi–Metzner–Sachs ({% include ref.html key="bondi1962GravitationalWavesVII" text="Bondi, van der Burg, and Metzner 1962"%}; {% include ref.html key="sachs1962AsymptoticSymmetries" text="Sachs 1962"%}; {% include ref.html key="sachs1962GravitationalWavesVIII" text="Sachs 1962"%}) and Dappiaggi–Moretti–Pinamonti ({% include ref.html key="dappiaggi2009CosmologicalHorizons" text="2009" %}) groups (see my {% include ref.html key="aguiaralves2026LecturesBondiMetzner" text="recent pedagogical review"%} for an introduction). These groups characterize the asymptotic symmetries at null infinity in asymptotically flat spacetimes and the cosmological horizon in expanding universes ("asymptotically de Sitter spacetimes"), respectively. 

However, it is curious that the two groups are very similar, but also very different. We would like to understand why. If we have success in extending the groups to larger versions that encompass both at the same time, then we will be able to employ techniques that are common in one setup to the other.

## Methods
Our main mathematical tool will be the notion of a Carollian structure, introduced by Duval *et al.* ({% include ref.html key="duval2014CarrollVersusNewton" text="Duval, Gibbons, Horvathy, and Zhang 2014"%}; {% include ref.html key="duval2014ConformalCarrollBMS" text="Duval, Gibbons, and Horvathy 2014"%}; {% include ref.html key="duval2014ConformalCarrollGroups" text="Duval, Gibbons, and Horvathy 2014"%}). This is a generalization of the idea of a pseudo-Riemannian manifold to the case in which the metric has a degenerate direction. Instead of asking for a pair $(M,g_{ab})$, we instead ask for a triple $(N,h_{ab},n^a)$, where $n^a$ is a vector along the degenerate (null) direction.

Instead of working with arbitrary null hypersurfaces, we prefer to define the notion of asymptotic (conformal) Killing horizons. These are null hypersurfaces tangent to a vector field that asymptotically satisfies the (conformal) Killing equation in the limit as one approaches the surface. These surfaces are meant to inherit properties of genuine Killing horizons, but without restricting the ambient spacetime. 

A(C)KHs are special when considered as a type of null hypersurface. For instance, all their spatial cross-sections are confomorphic (for ACKHs) or isometric (for AKHs). This considerably constrains their geometry.

## Results
After studying the conformal Carroll groups naturally induced by the A(C)KH structure, we find the groups 

$$G_{\text{ACKH}} = \text{Conf}(\Sigma) \ltimes \left(\mathcal{C}^{\infty}(\Sigma) \ltimes \mathcal{C}^{\infty}(\Sigma) \right)$$

and 

$$G_{\text{AKH}} = \text{Isom}(\Sigma) \ltimes \left(\mathcal{C}^{\infty}(\Sigma) \ltimes \mathcal{C}^{\infty}(\Sigma) \right),$$

where $\text{Isom}(\Sigma)$ is the isometry group for $\Sigma$, while $\text{Conf}(\Sigma)$ is the associated conformal group. In both cases, $\Sigma$ stands for the spatial cross section of the horizon. 


For $\Sigma = \mathbb{S}^2$, as one usually considers in four-dimensional applications, we get 

$$G_{\text{ACKH}} = \text{SO}^+(3,1) \ltimes \left(\mathcal{C}^{\infty}(\mathbb{S}^2) \ltimes \mathcal{C}^{\infty}(\mathbb{S}^2) \right)$$

and 

$$G_{\text{AKH}} = \text{SO}(3) \ltimes \left(\mathcal{C}^{\infty}(\mathbb{S}^2) \ltimes \mathcal{C}^{\infty}(\mathbb{S}^2) \right),$$

$G_{\text{AKH}}$ is then merely the DMP group, but $G_{\text{ACKH}}$ extends the BMS group by an infinite family of "superdilations".

## Conclusions
Viewing the sky as a Killing horizon can lead to interesting new perspectives. For example, superdilations arising at the symmetry group at infinity may hint at memory effects hidden in modified theories of gravity. One could use symmetries to search for these theories, and then test the subsequent predictions with gravitational wave observatories. 

Other possible outlooks are the investigations of bifurcate horizons, which could appear at lightcones and at spacetimes that are asymptotically flat at spatial infinity. Lastly, our analysis disfavors the possibility of exploiting superrotations as a path to a dS/CFT correspondence in the cosmological horizon.
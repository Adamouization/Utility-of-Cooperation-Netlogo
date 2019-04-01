# Altruistic Strategies For Colony Growth

## Utility of Cooperation using NetLogo

The present coursework explores the utility of cooperation, which is core to many cognitive strategies. The NetLogo code can be found in the [src](https://github.com/Adamouization/ICCS-2/tree/master/src) folder.

## 1 Introduction

The tested hypothesis is the beneﬁt of altruistic strategies for colony growth. The inspiration comes from Wilkinson (1984), who revealed how Vampire Bats demonstrate altruistic behaviour towards other members of the same species who are not strictly related to them. The goal of this research is to prove that some altruistic strategies are selected by speciﬁc environments. While it is acknowledged that the simulation environment used in this report is diﬀerent from the corresponding real world example, the aim of the experiment is to extract variables which aﬀect colony growth in the context of altruism.

Dawkins (1976) provides an interesting metaphor for altruistic and selfish behaving entities within a population; the former are called “suckers” , the latter “cheats”. In the chapter “You scratch my back, I’ll ride on yours”_ (Dawkins, 1976, p. 165), he is explained how “cheats” can take advantage of “suckers” by simply not returning favours. The ultimate consequence of this scenario is the extinction of altruistic behaviour (or its recurring shrinking and expansion).

The current project shows how altruistic behaviours, like the one described by Wilkinson (1984), apply when resources are scarce, while“cheats”, described by Dawkins (1976), emerge and take over when there are less threats to survival.

## 2 Approach

While Smaldino et al. (2013) demonstrate that, for certain conditions, cooperative behaviour is worse in harsh environments and better in safe ones, the opposite is argued in this report. As stated by Caˇˇce and Bryson (2007, p. 312), simulations are strictly theoretical and can in no case simulate any kind of realistic real-world situation. Therefore, changing a single heuristic can flip the simulation outcomes, which is what was done in this report.

A rational rule-base was constructed with respect to simulation of real-world behaviour. An additional rule introduced to Smaldino et al.’s simulation will be referred to as “altruistic suicide”. This suicidal heuristic is inspired by Wilkinson (1984) and the Vampire Bat’s altruistic behaviour. It is intended to be a simplification of altruistic behaviours observed in nature. The assumption behind it is that any altruistic act, clarified by Smaldino et al. (2013, p. 451), has the risk of bringing the entity committing the act closer to its death. This altruistic suicide strategy requires part of the population to die and share its resources (its corpse) with the remaining entities in the form of energy.

Additional changes made to Smaldino et al. (2013)’s original simulation rules include the removal of the prisoner’s dilemma paradigm. The new rules make it so that any interaction between agents generate +2 energy units for each communication. The other modification to the code is a pre-defined probability of triggering an altruistic suicide at each tick.

In the simulation, the population of agents is split between defectors, who do not commit altruistic suicide , and cooperators, who do commit altruistic suicide. The resources resulting from an altruistic suicide are only shared with other cooperative, suicidal entities, not with the selfish part of the population.

The experiment consists in testing the speed at which the maximum population is reached, measured in terms of ticks. Throughout the experiment, two variables are tested: the cost of living and the suicide rate. The initial population consists of 100 agents, with a 50% split of cooperators and defectors. The world limit is naturally bounded by the 70x70 world size. The tick value is recorded and plotted when the population size reachesN= 4900.

The simulation is conducted in NetLogo 6.0. using a modified version of Smaldino et al. (2013)’s code. Nine runs are carried out using varying costs of living and suicide rates. The suicide rate is used as an indicator of how altruistic the cooperators are (1 being the most and 0 being the least altruistic).


## 3 Results

The results of the nine simulation runs are plotted in a 3D histogram (see Figure 1), where the height of the bars is the number of ticks needed to reach a population ofN= 4900.

<img src="https://github.com/Adamouization/ICCS-2/blob/master/report/figures/3d_histogram.png" alt="results histogram" width="40%"/>


The 3D histogram clearly demonstrates that the higher the suicide rate, the quicker the population reaches the maximum threshold, meaning a population that cooperates evolves more quickly than a selfish one. Similarly, the lower the cost of living, the quicker the population evolves, meaning harsh environment conditions hinder a population’s growth. The results of the experiment show that altruism (higher suicide rate) helps countering the environment’s harsh conditions, allowing the population to grow more quickly. The histogram also betrays a second correlation between the changes in cost of living for lower ranges (from 0 to 0.5), showing a boosting effect for population growth caused by higher suicide rates.

## 4 Discussion

There is a limit to how much "altruistic suicide" contributes to growth. However, this is not reflected by this simulation for high suicide rates due to the intrinsic to the logic of the simulation rules.

Focusing on the results from Section 3, it can be observed that the maximum population is mostly reached thanks to the altruist half. The following factors may play a role in this observation:

* birth energy threshold
* net-positive neighbour benefit
* "altruistic suicide" energy income

This means that a slight energy-wise advantage favours birth rates from the start. This generates early localised clusters of “cooperators” which generate more energy than smaller clusters (because of the modified prisoner’s dilemma), thus more children, more suicides and, consequently, more localisation again. This virtuous cycle maximises growth. Therefore, maximum population is reached fairly quickly thanks to cooperators. Once total world coverage occurs, a stable condition is reached where energy procurement is not a problem, thanks to the updated prisoner’s dilemma paradigm. The main take on this is that population growth is maximised in safe environments where populations are more altruistic.

Once world coverage is first reached, population growth is no longer required. As cooperators still commit altruistic suicide, cells are freed up on the grid and can then be replaced by both defectors or cooperators. As this effect keeps occurring, the altruist population will slowly shrink and eventually be fully replaced by defectors before going extinct, similarly to Dawkins (1976) explanations. But this is just yet another side effect of the experiment which is not considered in the hypothesis.

## 5 Conclusion

We tested the effectiveness of population growth with different rule-bases and different gradations of altruistic behaviour across different environments. We found that altruistic wealth redistribution among cooperators is beneficial to population growth.

## References

Dawkins, C. R. (1976). _The selfish gene_. Oxford
University Press.

Smaldino, P. E., Schank, J. C., and Mcelreath,
R. (2013). Increased costs of cooperation help
cooperators in the long run. _The American
Naturalist_ , 181(4):451–463.

Caˇ ˇce, I. and Bryson, J. J. (2007). Agent based
modelling of communication costs: Why
information can be free. _Emergence of
Communication and Language_ , pages
305–321.

Wilkinson, G. S. (1984). Reciprocal food sharing
in the vampire bat. _Nature_ ,
308(5955):181–184.



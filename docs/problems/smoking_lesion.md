---
layout: default
title: Smoking Lesion
parent: Problems
navorder: 6
---

# Smoking Lesion

In this game, the world is very different from our own. Smoking doesn't cause cancer. Instead, desire to smoke and proclivity for cancer are both caused by a genetic lesion.

Assume you enjoy smoking. You also enjoy not having cancer a lot more than you enjoy smoking.

Should you smoke?

## Normal Form Game

Assumptions:
* if you have the lesion, smoking is worth $5
* if you don't have the lesion, smoking is worth $1
* cancer is worth -$10
* if you have the lesion, your chance of cancer is 0.8
* if you don't have the lesion, your chance of cancer is 0.2
* use normal expected value to calculate loss in value due to cancer

| | lesion | no lesion |
|---|---|---|
| smoke | -3 | -1 |
| don't  | -8 | -2 |

## Extensive Form Game

Note that nodes with a dotted line between them are in the same information set. The decider in those nodes doesn't know which world they're in.

```mermaid
flowchart TB
	lesion["Have Lesion"]
	lesionYou["You"]
	noLesionYou["You"]
	lesion -- "yes" --> lesionYou
	lesion -- "no" --> noLesionYou
	
	lesionYou o-.-o noLesionYou

	lesionYou -- "smoke" --> ls["-3"]
	lesionYou -- "don't smoke" --> lns["-8"]

	noLesionYou -- "smoke" --> nls["-1"]
	noLesionYou -- "don't smoke" --> nlns["-2"]
```

## Solutions in various Decision Theories

### CDT

The Causal Decision Theorist knows that, in this alternate world, there is no causal link between smoking and cancer. Whether the CDT agent has the lesion or not is determined before the they decide whether to smoke. Smoking or not smoking doesn't change their cancer risk.

The CDT agent decides to smoke.

## References

* [Less Wrong Smoking Lesion Page](https://www.lesswrong.com/tag/smoking-lesion)

<!--
Filename: 	note.md
Project: 	/Users/shume/Developer/AgentBasedModel/ThinkComplexity2e/09
Author: 	shumez <https://github.com/shumez>
Created: 	2019-04-22 14:15:0
Modified: 	2019-05-02 17:49:33
-----
Copyright (c) 2019 shumez
-->

# 09. Agent-bsed models

## Contents

* [09.01. Schelling's Model](#0901_schellings_model)
* [09.02. Implementation of Schelling's model](#0902_implementation_of_schellings_model)
* [09.03. Segregation](#0903_segregation)
* [09.04. Sugarscape](#0904_sugarscape)
* [09.05. Wealth inequality](#0905_wealth_inequality)
* [09.06. Implementing Sugarscape](#0906_implementing_sugarscape)
* [09.07. Migration and Wave Behavior](#0907_migration_and_wave_behavior)
* [09.08. Emergence](#0908_emergence)
* [09.09. Exercises](#0909_exercises)



## 09.01. Schelling's Model

Schelling model ([Schelling, T., 1969][1969_SchellingThomas])

neighborhood

```
| O | X | X |
| X | O | O |
| X | O | X |
```


## 09.02. Implementation of Schelling's model

```py
class Schelling(Cell2D):
    def __init__(self, n, p):
        self.p = p
        choices = [0, 1, 2]
        probs = [.1, .45, .45]
        self.array = np.random.choice(choices, (n, n), p=probs)
```
<!-- <script src="https://github.com/shumez/AgentBasedModel/blob/557615672205fe07b0385208102fb9a73094eded/ThinkComplexity2e/code/Cell2D.py#L30-L36"></script> -->

<script src="https://gist-it.appspot.com/github/shumez/AgentBasedModel/blob/master/ThinkComplexity2e/code/Cell2D.py?slice=29:36"></script>



<!-- ref -->
[1969_SchellingThomas]: https://github.com/AllenDowney/ThinkComplexity2/blob/master/papers/schelling69models.pdf ""

<!-- <style type="text/css">
	img{width: 50%; float: right;}
</style> -->
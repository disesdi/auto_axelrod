# Auto Axelrod

*a python project to auto-generate multi-strategy Axelrod tournaments, & visualize their results*

this Python project is designed to allow the user to input from one to several Axelrod strategies from the `axelrod` package, play their preferred number of matches, generate raw & normalized scores, and visualize the results using `Matplotlib`.

the `axelrod` package contains hundreds of strategies, both original and community-contributed. find package documentation [here](https://axelrod.readthedocs.io/en/fix-documentation/index.html).

code for this project available [in this jupyter notebook](https://github.com/disesdi/auto_axelrod/blob/d83f5b13ad02f1bffaa259a6ee6fd03ce761c487/axelrod_tourney_generator_with_visualization.ipynb).

## how to use

the `make_tourney_multi` function takes 3 inputs: `players`, input as a list of strategies, `num_turns`, the number of turns the user wishes to specify for each player, and `num_reps`, which sets the number of matches in the tournament.

to run a tournament, input the desired strategies from the `axelrod` package in the form of a list, e.g:

`[axl.Alternator(), axl.Cooperator()]`

to see a list of all strategies in the notebook, use `axl.all_strategies`

## visualization

the `make_tourney_multi` function automatically displays boxplot & payoff matrix visualizations of tournament results.

## example

**example code & output for a five-player tournament using the 'Defector', 'Grudger', 'Tit For Tat', 'Alternator', & 'Cooperator' strategies:**

![image](https://user-images.githubusercontent.com/110150470/211300965-1068afcd-4e6c-4235-8eb4-086277744013.png)

**example boxplot & payoff matrix visualizations:**

![image](https://user-images.githubusercontent.com/110150470/211301314-2095789a-c042-49ef-863e-4d1b59521af1.png)

## about the Axelrod tournament

the original [Axelrod tournament](https://axelrod.readthedocs.io/en/fix-documentation/reference/overview_of_strategies.html) was held in 1980 by a University of Michigan political science professor named Robert Axelrod, as a competition to find optimal strategies for the the prisoner's dilemma.

each player in the game known as [the prisoner's dilemma](https://plato.stanford.edu/entries/prisoner-dilemma/) has 2 potential strategies available to them: either cooperate, `C` or defect, `D`.

read Robert Axelrod's original 1980 paper here: https://www.jstor.org/stable/173932

subsequent work:

* Axelrod's second tournament: https://axelrod.readthedocs.io/en/fix-documentation/reference/overview_of_strategies.html#axelrod-s-second-tournament
* Stewart and Plotkin’s Tournament (2012): https://www.pnas.org/doi/pdf/10.1073/pnas.1208087109

the `axelrod` python package is based on this tournament idea. its default settings create a prisoner's dilemma game with built-in strategies and predetermined payoffs.

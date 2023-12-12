# Documentation for nerds

## Code

We are considering the following set of all 3-digits combinations:

$$\mathcal{S} = \\{1, ..., 5\\}.$$

The elements $x\in\mathcal{S}$ are called codes.

## Criteria

A criteria is a function $C$ associating to every code a binary value:

$$ C:\mathcal{S}\to\\{0,1\\}.$$

We say that a code $x\in\mathcal{S}$ satisfies the criteria $C$ if $C(x)=1$.

## Criteria card

A criteria card consists of a criteria $C$ together with 9 sets of codes:

$$S_i \subset \mathcal{S},\qquad i=1,...,9.$$

where the first set $S_1$ is consistent with the criteria in the following sense:

$$S_1 = \\{x\in\mathcal{S} : C(x)=1\\}$$

## Interpretation of the criteria card

All the non-empty sets are described using easy formulas on the criteria card so that the player can easily understand how the set is defined. For example, "the first value is equal to one" would be a way of displaying the following set on the criteria card:

$$\\{1\\}\times\\{1, ..., 5\\}^2$$

Some cards describe less than 9 sets since some of these sets are empty. For example the criteria card number 1 contains only the following two sets:
- The first value is equal to one
- The first value is strictly larger than one

Per definition, we know that the first set will allways be consistent with the criteria card. However for each game, the criteria card does display the sets in order, therefore the user does not know which one of the sets displayed is the set consistent with the criteria. 

The sets are usually disjoint in the easiest criteria cards, but for some more complex cards, we will often face overlapping sets.

## Game

A game consists of 4 to 6 criteria cards together with a secret number $s\in\mathcal{S}$.

The goal of the game is to guess the correct value $s$ as in the lowest possible number of successive rounds. Each rounds is performed under the following ruls:
- The player chooses a code $x\in\mathcal{S}$
- He evaluates at most three of the criteria card at the value $x$ (this means getting the value $C(x)$ for at most three cards $C$)

In case of a tie where two players have found the code in the same round, the player who performed the lowest number of evaluation of criteria cards wins. Otherwise this remains a tie.

### Game specification

The game is guaranteed to fulfill the following properties:
- There exist one unique element $x\in\mathcal{S}$ satisfying all criteria cards from the game.
- This element is the secret number named $s$
- The criteria cards are not redundant in the sense that removing any of the criteria card would cause multiple values to fulfil the criterias.

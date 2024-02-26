# football_teams
Building balanced teams from pools of football players

# Complexity Notation

To be able to reason in a streamlined fashion about computational and memory complexity of the solution, we will use the following conventions associated with parameters of the problem at hand:

- P: Unique number of positions available
- N: Number of players in the player's pool
- T: Number of teams to partition players to (T=2 by problem definition)

# Modelling Approach

To incorporate optimizing for positional balance among the two teams we are looking to build, we take the following modelling approach to account for positional mismatches: for each player, we unroll her/his skill level to each position prescribed. The algorithm for this unrolling is as follows:
- if the position we are unrolling the player to is the player's original position, we assign the original (full) score of the player to it.
- if the position we are unrolling the player to is not the player's original position, we assign a reduced score to it, i.e. we penalize the skill score of the player if s/he is deployed to a team in that position. The rationale of that penalization is the player won't be able to perform to her/his full skill score due to the positional mismatch of the position s/he is deployed versus her/his original skillset.




| Player   | GK | Center Back | Full Back | Defensive Midfielder |  Central Midfielder |  Attacking Midfielder | Winger | Forward |
| -------- | -------  | -------  |  -------  |  -------  |  -------  |  -------  |  -------  |  -------  |
| P1 (85, Goalkeeper)  |   85   |   65   |   65   |  45   |   45   |   45   |   25   |   25   |   25   |
| P2, 87, Center Back  |   67   |   87   |   77   |  67   |   67   |   67   |   47   |   47   |   47   |
| P3, 82, Full Back    |   62   |   72   |   82   |  62   |   62   |   62   |   42   |   42   |   42   |
| P4, 90, Defensive Midfielder  |   67   |   87   |   77   |  67   |   67   |   67   |   47   |   47   |   47   |



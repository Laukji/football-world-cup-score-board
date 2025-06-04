## Football World Cup Score Board
A simple library for implementing a live football world cup score board

## ScoreBoard
The class 'ScoreBoard' provides methods for:
* `startMatch(String homeTeam, String awayTeam)` - add a new match with initial score 0-0 to the scoreboard
* `updateScore(Integer homeTeamScore, Integer awayTeamScore)` - update score for home team and away team for an ongoing match
* `finishMatch(String homeTeam, String awayTeam)` - finish an ongoing match and remove it from the scoreboard
* `getSummary()` - return a summary of ongoing matches ordered by total score and recency

## Assumptions and explanation
* Moved updateScore to the Match model as it logically belongs to a Match. Could have it in the Scoreboard class but would
  need an additional input parameter or two such as matchId/teamNames

* Used Integer as score type for null comparison and avoiding unboxing issues

* Did not add any extra validation to teamName other than checking for null, so current implementation allows for team names such as "ARG" or "XYZ123".
  If I were to add validation it would probably be through customized annotations ensuring the length and characters of the String input.

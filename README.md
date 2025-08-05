# nhl-save-shot-predictor

This is a python algorithm which predicts the expected amount of shots, saves, and goals in an NHL game. It utilizes rolling averages and exponential smoothing (α * x(t) + (1 - α) * S(t-1)) to do so. 

Usage:
Run the script.

Input the team abbreviation (e.g., TOR, BOS).

Input the start and end indices for the sample range of games. (once the new season starts this will change to just the last x games, and I will alter the code)

Input smoothing alpha values for shot differential, opponent shot against differential, shooting percentage, and save percentage.

The script will output:

Rolling shot differential metrics.

Expected shots, goals, and saves for the upcoming game.

A plot showing shots taken vs opponent average shots against.

Note:
The script uses NHL's 2024-2025 season data; update the season code in the script if needed.

Example:
enter team name abbreviation: TOR
beginning of sample: 0
end of sample: 10
alphaShotDiff = 0.33
alphaShotAgainstDiff = 0.45
alphaShootingPct = 0.2
alphaGAPct = 0.2

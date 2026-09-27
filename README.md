# Jane Street puzzles

Dominic Tatakis's solutions to [Jane Street's monthly puzzles](https://www.janestreet.com/puzzles/).

| Puzzle | Answer | Solution |
|---|---|---|
| [Beside the Point](https://www.janestreet.com/puzzles/beside-the-point-index/) (November 2024) | 0.4914075788 | [notebook](2024-11-beside-the-point/beside_the_point.ipynb) |
| [Somewhat Square Sudoku](https://www.janestreet.com/puzzles/somewhat-square-sudoku-index/) (January 2025) | 283950617 | [notebook](2025-01-somewhat-square-sudoku/somewhat_square_sudoku.ipynb) |

Both answers match the solutions Jane Street published after each puzzle closed.

## Beside the Point

Place the blue point in one-eighth of the square, so its closest side is the bottom edge. A point on
that edge equidistant from both points exists exactly when the red point lies in one, but not both, of
the quarter-discs centred on the bottom corners that pass through the blue point. The notebook averages
that area over the blue point with a double integral. It then checks the result against a direct
simulation of 50 million random pairs.

## Somewhat Square Sudoku

Build the rows as rotations of one cycle of nine digits: rotations keep common factors and fit the
Sudoku rules naturally. Searching every cycle gives a highest GCD of 12,345,679, and the pre-filled
cells then fix the grid. A final check shows no grid of any shape does better. The rows sum to
S × 111,111,111, where S is the sum of the nine digits used, so the GCD must divide that. No divisor
above 12,345,679 admits a grid.

## Running the notebooks

Needs Python 3.8 or later:

```sh
pip install -r requirements.txt
jupyter lab
```

Each notebook runs top to bottom in under 15 seconds. The Sudoku notebook uses only the standard library.

## Licence

MIT. See [LICENSE](LICENSE).

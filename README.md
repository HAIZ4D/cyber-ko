# Cyber K.O.

A two-team cyber security fighting game for a classroom, built for **SSW4202 Ethics in Computing** (Chapter 6: Cyber Security and Risk Analysis).

Two teams each control a fighter with 100 HP. Teams spin a wheel, answer a question, and fight:

- **Correct answer:** your fighter hits the opponent.
- **Wrong answer or no answer:** your attack backfires and you take the damage.
- **Double damage:** a wrong answer makes the next turn worth double (no stacking).
- **Final round:** +10 ultimate damage on every hit.
- **K.O.** at 0 HP. Otherwise the higher HP after Round 4 wins. Ties go to sudden death.
- Watch out for the **Mystery** slice.

## How to run

It is one HTML file with no build step. Open `index.html` in a browser, or serve it with any static host (GitHub Pages works).

Runs on one laptop connected to a projector. Students don't need their own devices.

## Host controls

| Key | Action |
| --- | --- |
| `Space` | Spin / continue |
| `A`–`D` | Select the captain's answer |
| `N` | No answer |
| `F` | Fullscreen |
| `M` | Mute |

## Changing the rules

The damage values, rounds and timer are at the top of the `<script>` in `index.html`:

```js
const SLICES=[{c:"mal",dmg:10},{c:"atk",dmg:20},{c:"def",dmg:30},{c:"cia",dmg:10},{c:"eth",dmg:20},{c:"mys",dmg:20}];
const ROUNDS=4,TURNS_PER_ROUND=4,ULT_BONUS=10,QTIME=30;
```

Questions are in the `QS` array just below.

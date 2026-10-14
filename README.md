# Gladiator-Hands

A gesture gladiator duel for phones. The top of the screen animates a pixel-art arena fight; the bottom is a pad where you draw your moves with your finger.

## How to play

Each round you draw **one attack** and up to **two guards**. Your opponent secretly does the same, then both attacks resolve.

- An attack on an unguarded line hits. An attack on a guarded line is **parried** and countered.
- Your **first guard is your main guard**. Parry with it to **riposte** for 1.5× counter damage.
- Attacks cost 1–3 **stamina** and each guard costs 1. You regain 3 per round; **Rest** skips your attack to regain 2 more.
- Read the opponent's **stance** before each round to guess their attack. Some opponents lie.
- A fast, straight stroke is **clean** and deals 25% more damage. Lighter attacks strike first.

| Draw | Attack | Hit | If parried | Cost |
| --- | --- | --- | --- | --- |
| `—` | Slash | 11 | −6 to you | 1 |
| `\|` | Chop | 20 | −14 to you | 3 |
| `/` | Rising cut (drains 2 stamina) | 14 | −9 to you | 2 |
| `\` | Falling cut (foe gets 1 guard next round) | 14 | −9 to you | 2 |
| tap | Thrust (needs the Hasta spear) | 10 | −7 to you | 1 |

## Progression

Beat five ranked opponents (Tiro, Brutus, Vipera, Ferox, Leo) to earn laurels, then spend them in the armory:

- **Hasta** (spear): tap to thrust
- **Galea** (helm): +20 max health
- **Rete** (net): once per fight, the foe can't guard for a round
- **Scutum** (tower shield): a third guard slot

## Running it

Everything is in a single `index.html` with no build step. Open it in a browser, or serve the folder with any static server (for example `python3 -m http.server`) and open it on your phone. Progress is saved in the browser's local storage.

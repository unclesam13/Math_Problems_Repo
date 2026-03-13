# Solution 1 — Events and Probability (Sample Spaces)

## Task 1 — Coin Tossing

### Sample Spaces

**One coin toss** — each outcome is either Heads ($H$) or Tails ($T$):

$$\Omega_1 = \{H, T\}, \quad |\Omega_1| = 2$$

**Two coin tosses** — each outcome is an ordered pair:

$$\Omega_2 = \{HH, HT, TH, TT\}, \quad |\Omega_2| = 4 = 2^2$$

**Three coin tosses** — each outcome is an ordered triple:

$$\Omega_3 = \{HHH, HHT, HTH, HTT, THH, THT, TTH, TTT\}, \quad |\Omega_3| = 8 = 2^3$$

### General Rule

For $n$ coin tosses:

$$|\Omega_n| = 2^n$$

Each elementary outcome represents a **complete sequence** of results across all tosses - for example, $HTH$ means "Heads on toss 1, Tails on toss 2, Heads on toss 3".
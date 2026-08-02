# Confusion Log

One line per entry: the lab, what confused you, and, once it clicks, how.

- **Example** (Lab 0, section 4.3): My noisy-simulation cell came back as
  `{'0': 20000}`, no `1`s at all, and the notebook said I should see some. I thought the
  fake backend wasn't applying noise. It clicked on a reread: the gate error on this qubit
  is only a few in ten thousand, so a perfectly clean run happens sometimes, it isn't a
  broken simulation. Rerunning the cell gave `{'0': 19992, '1': 8}`.

Add your own entries below, one per line:

- Lab 0: ...

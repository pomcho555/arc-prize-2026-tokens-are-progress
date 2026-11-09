# Tokens Are Progress: Serving LLM Coding Agents on ARC-AGI-2 and ARC-AGI-3

Paper for the ARC Prize 2026 Paper Track (Track: ARC-AGI-2, documented submission 57852801).

**[Read the paper (PDF)](paper.pdf)**

Team 復活の混テキスト: isakatsuyoshi, konbu17, pompom555, refv00, tanakaai24 (Kaggle)

## Abstract

We document two ARC Prize 2026 entries built on one design: a general-purpose mixture-of-experts LLM reasons inside a
persistent Python sandbox, and most of the engineering goes into the inference server. Our ARC-AGI-2 submission (grid
tasks; four L4 GPUs; 12 hours) scored 73.47 on the public leaderboard (rank 25 of 3,543 teams). Our ARC-AGI-3
submission (interactive games; one RTX PRO 6000; 9 hours) scored 46.20 (team best 46.82, rank 15 of 4,923). Both follow
from a budget model: under a fixed wall clock, score is roughly the tokens delivered per task times the score each token
buys. Decoding is memory-bound, so a few levers set the token rate. We report each lever's measured effect, the faster
changes that lost because each token bought less, and why different levers paid on a bandwidth-bound and a
capacity-bound GPU.

## Submitted notebooks

- ARC-AGI-2, submission 57852801:
  [refv00/arc2-x-pr177-c150-cpu64-submission-12h-t1nfix](https://www.kaggle.com/code/refv00/arc2-x-pr177-c150-cpu64-submission-12h-t1nfix?scriptVersionId=364368795),
  version 4.
- ARC-AGI-3, submission 57904278:
  [pompom555/arc3-pr46-v7-submit-20261102](https://www.kaggle.com/code/pompom555/arc3-pr46-v7-submit-20261102?scriptVersionId=364615885),
  version 1.

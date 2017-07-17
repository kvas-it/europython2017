# Fighting the controls (programmers vs pilots) (Daniele Procida)

- Pilots and programmers have some similar human judgement failure modes in
  extreme situations.
  - Loss of situational awareness,
  - Panic,
  - Faulty mental models,
  - Misjudging cause and effect,
  - Poor decision making.
- Similarity between pair programming and 2-pilot cockpit.
- Programming is a creative craft kind of like writing, very unlike surgery.
- Feedback is very quick.
- But debugging is very private.
- So we are driven to the same short loop and we lose situational awareness
  because we're too busy fighting the controls.
- When programmers do it, they look foolish, when pilots do it, they die, so
  pilots figured out better ways to deal with it.

# Mitigating loss of situational awareness in aviation

The basic idea is to use simple techniques that reliably work. They can be
performed under stress and have minimal cognitive load.

- Checklists (for normal operation and for emergency),
- Communication, explain to another person what you're doing,
- Stop (at least for a short while). Doing nothing is sometimes better than
  doing random stuff in panic.

# What can we do

- We can adopt checklists,
- Communicate explicitly and with the intention to improve our understanding of
  the situation,
- Stop fighting the controls (in programming it's much cheaper than in
  piloting).

# Q/A

- 15 minute rule (debug for 15 minutes, if you don't solve it, write the
  problem down, ask someone else).
- SRE methods. We can learn from them.
  - Classify all the past tickets and act on this analysis.
- Can we help this with tooling?

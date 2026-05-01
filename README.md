# Dynamic-Wumpus-Logic-Agent
Web-based Dynamic Wumpus Logic Agent using Propositional Logic, CNF Conversion, and Resolution Refutation for safe pathfinding in AI Wumpus World.

## Features
- Dynamic grid sizing (user-defined rows and columns)
- Random placement of pits, Wumpus, and gold
- Breeze and Stench percept generation
- Propositional Knowledge Base
- CNF clause generation from percept biconditionals
- Automated Resolution Refutation
- Safe cell deduction before movement
- Autonomous agent pathfinding
- Interactive web dashboard
- Real-time inference logs and metrics

## Technologies Used
- HTML5
- CSS3
- Vanilla JavaScript
- Propositional Logic
- CNF Conversion
- Resolution Refutation

## Logical Model

### Breeze Rule:
B(x,y) ⇔ (P₁ ∨ P₂ ∨ P₃ ...)

### Stench Rule:
S(x,y) ⇔ (W₁ ∨ W₂ ∨ W₃ ...)

### Safe Cell:
¬P(x,y) ∧ ¬W(x,y)

## CNF Example
B ⇔ (P₁ ∨ P₂)

Converted to:

(¬B ∨ P₁ ∨ P₂) ∧ (¬P₁ ∨ B) ∧ (¬P₂ ∨ B)

## Resolution Logic
To prove a cell is safe:
1. Add negated query to KB
2. Resolve clauses iteratively
3. If contradiction occurs, query is true

# Simplicity-centric React Project Organization Guidelines

This is a resource for front-end engineers who are interested in organizing their React project with a focus on decomposing complexity into its individual simple parts. This is a methodology engineered by Milan Adamovsky with the goal of normalizing problem solving effectiveness across skill levels, where speed is the main differentiating factor.

## <a href="philosophy.md">Philosophy</a>

# Principles

There are a few principles that are observed:

## Alphabetization

Everything that can be alphabetized, should be.
## Single Purpose Principle

Everything should only ever cover one thing and one thing only. This includes not only components, but utilities, user stories, tasks, bugs, etc.

## Decentralization

All assets needed by a component must live together in its folder. Centralization of assets is an anti-pattern in this methodology. 

### Deletability

A component is the definition of a deletable unit. This means if such a unit is removed, all associated dependencies are removed with it. There should be no trailing (dead) files in central assets folders, etc. that need to be tracked down after a component is removed.

## Intentional Coding

Code with intent. Slow down to move forward in a more thoughtful manner. Think through every step and its consequences. Code in a way where the reliance on tooling for quality is not a necessity.

### <a href="explicit.md">Code Explicitly</a>

## KISS Principle

Keeping things simple is at the forefront of this methology. Favor simplicity over sophistication where sophisticated solutions make the Developer Experience (DX) difficult.

# Constraints

There are a few self-imposted constraints that help catch runaway coding. These constaints act a tripwires for the engineer to help identify when closer attention must be paid to the code.

## 100 lines of code per file

A healthy lint count per file should usually be around the 50 to 70 lines of code.  Anything over 100 lines of code should prompt for a conversation with a peer or lead to see how the code can be decomposed.

Do not sacrifice code cleanliness. Maintain proper form (eg indentation, spacing).

## No acronyms or abbreviations

Spell out all words. Remove all doubt and vagueness in the code. Leave minification to tooling.

## One component per file

A component should ever only `export default` one thing and one thing only. No other exports.

## No commented code

Only commit code that is actually being used. Commented code clutters the workspace. Code should be clear to the point that no comments are needed.

## No overwriting of quality control tools

Do not disable lint rules (or similar). They are there for a reason.

# Exceptions

In the event any of these principles or constraints need to be broken, an engineer must call for a technical discussion meeting with peers or tech lead to where an approval must be agreed upon.
# Intro to KBS: Space Mission Launch System

## Description
This is a mini Rule-Based Knowledge-Based System (KBS) built in Python. It uses a forward-chaining inference engine to determine if a space mission is cleared for launch based on propulsion, life support, crew, and weather conditions.

## How to Run
1. Open `kbs_quiz.ipynb` in VS Code or Jupyter Notebook.
2. Select "Run All" or execute the cells sequentially from top to bottom.
3. Observe the printed outputs showing the step-by-step inference and the final launch decision.

## List of Base Facts Used
* `fuel_tanks_full`
* `crew_on_board`
* `weather_clear`
* `oxygen_levels_stable`

## List of Rules
1. **IF** `fuel_tanks_full` **THEN** `propulsion_ready`
2. **IF** `oxygen_levels_stable` **THEN** `life_support_active`
3. **IF** `crew_on_board` **AND** `life_support_active` **THEN** `crew_ready`
4. **IF** `propulsion_ready` **AND** `crew_ready` **THEN** `internal_systems_go`
5. **IF** `internal_systems_go` **AND** `weather_clear` **THEN** `mission_launched`

## Final Decision Logic
The final decision checks for the presence of the `mission_launched` fact. This fact is dynamically inferred only if all prerequisite systems (propulsion, life support, crew readiness, and weather) successfully chain together. If `mission_launched` exists in the final knowledge base, the system outputs "FINAL DECISION: MISSION LAUNCHED 🚀"; otherwise, it outputs "FINAL DECISION: LAUNCH ABORTED 🛑".

## Student Details
**Name:** Fredrick Kisenge  
**Student Number:** 671056
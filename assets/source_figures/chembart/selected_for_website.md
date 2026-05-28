# ChemBART Website Figure Selection

Selected top 5 browser-safe figures for the ChemBART project page.

## Kept

1. `chembart_main_fig_01.png`  
   Project overview. Best first figure because it explains ChemBART as a pretrained reaction-language model connected to precursor/reagent prediction, downstream fine-tuning, RL/MCTS planning, and wet-lab feedback.

2. `chembart_main_fig_05.png`  
   Task framework. Useful for showing how classification, regression, generation, policy-function fitting, and value-function fitting are organized around Transformer representations.

3. `chembart_si_fig_025.png`  
   Top-k reactant-prediction success rate. Kept as convergence evidence after training-system optimization made full pretraining practical.

4. `chembart_si_fig_026.png`  
   Top-k syntax-error rate. Kept because it complements success rate by showing generation validity, which matters for synthesis-planning workflows.

5. `chembart_si_fig_034.png`  
   Value-function comparison. Kept because it connects pretrained ChemBART representations to decision functions used in MCTS-based synthesis planning.

## Deferred

- `chembart_si_fig_035.png`: useful policy-function comparison, but omitted to keep the page focused on five figures.
- `chembart_main_fig_02.png`: interesting interpretability result, but less directly connected to my contribution.
- `chembart_main_fig_03.png`: downstream regression result, but less central to the pretraining-acceleration story.
- `chembart_main_fig_04.png`: full synthetic pathway example, visually large and more about the broader project than my direct contribution.

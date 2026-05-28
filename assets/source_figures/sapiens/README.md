# SAPIENS Extracted Figures

Extracted from `SAPIENS.docx` and `SAPIENS_SI.docx` using the DOCX media archive.

## sapiens_main_fig_01.png
- Source: `SAPIENS.docx`
- Original media: `media/image1.png`
- Size: 1321 x 762 px
- File: `portfolio_site/assets/source_figures/sapiens/sapiens_main_fig_01.png`
- Nearby caption: Fig. 1 | The SAPIENS framework for discovering functional self-assembling peptides. a, Dataset construction. The Data Engine combines LLM-mined positive samples with length-matched unlabeled sequences. To overcome publication bias, the spy-separation algorithm was used to generate the negative dataset. b, Multi-task learning. The AI Engine employs a Transformer encoder to map sequences into a latent space for predicting self-assembly and catalysis. Aggregation propensity and functional activity are balanced via multi-task learning to enhance prediction on rare, high-activity sequences. c, Validation and mechanism. The Discovery Engine executes a “Predict-Test” cycle. AI-selected candidates are experimentally verified, followed by MD simulations to reveal the atomic-level structural basis of the observed activity.

## sapiens_main_fig_02.png
- Source: `SAPIENS.docx`
- Original media: `media/image2.png`
- Size: 1088 x 843 px
- File: `portfolio_site/assets/source_figures/sapiens/sapiens_main_fig_02.png`
- Nearby caption: Fig. 2 | Construction and validation of the self-assembly dataset. a, Workflow integrating LLM-based iterative extraction with a majority-voting filter. b, Extraction performance metrics showing precision (orange) and recall (gray) as a function of voting times. c, Schematic of the PU learning framework. Some positives (blue) acting as “spies” within the unlabeled pool to distinguish reliable negatives (gray) from potential assemblers (light blue). d, Self-assembly propensity distribution (0: non-assembling/negative; 1: assembling/positive). Following the training in stage 1, the probability distributions of the spy samples overlap significantly with those of the true positives, while distinctly differing from the unlabeled data. In stage 2, by filtering out high-scoring unlabeled samples (potential false negatives), the distinction between the positives (including the spies) and the negatives is further enhanced, thereby confirming the high reliability of the resulting negative dataset. e, UMAP visualization of peptide sequence space. The sparse distribution of existing literature data (yellow) 35 is superimposed on the constructed dataset (blue/gray).

## sapiens_main_fig_03.png
- Source: `SAPIENS.docx`
- Original media: `media/image3.png`
- Size: 1435 x 873 px
- File: `portfolio_site/assets/source_figures/sapiens/sapiens_main_fig_03.png`
- Nearby caption: Fig. 3 | Multi-task learning and performance evolution of SAPIENS. a, Overview of the multi-task learning architecture. The model uses a shared encoder to integrate relatively large-scale assembly data (blue) with sparse catalytic data (red), utilizing MGDA regularization to balance objectives. b, c, Virtual screening validation compares results from training solely on catalytic data (b) with those using the SAPIENS framework which incorporates catalytic, self-assembly, and sequence data (c). SAPIENS effectively enriches high-activity sequences (red points) into the top-scoring tier, demonstrating the efficacy of transfer learning in overcoming small-sample overfitting. d, Evolution of catalytic activity of SAPIENS-designed peptides targeting pNPA hydrolysis across four active learning iterations (rounds 1–4) and a rational design control (round 5). Strategies employed include cold-start supervised training (round 1), PU learning (round 2), and PU learning coupled with multi-task learning (rounds 3–4). The lead candidate, GW1, was identified in round 4.

## sapiens_main_fig_04.png
- Source: `SAPIENS.docx`
- Original media: `media/image4.png`
- Size: 808 x 866 px
- File: `portfolio_site/assets/source_figures/sapiens/sapiens_main_fig_04.png`
- Nearby caption: Fig. 4 | Experimental validation of catalytic performance. a, Catalytic activity for pNPA hydrolysis versus sequence similarity to reference peptide IIQ (top right). Comparison between SAPIENS-generated sequences (black) and literature benchmark sequences (light blue) identifies GW1 (top left) as the top candidate, possessing superior catalytic activity and high sequence novelty. b, Catalytic activity of GW1 towards the hydrolysis of various esters. c, Catalytic activity of GW1 in DMP oxidation.

## sapiens_main_fig_05.png
- Source: `SAPIENS.docx`
- Original media: `media/image5.png`
- Size: 1393 x 627 px
- File: `portfolio_site/assets/source_figures/sapiens/sapiens_main_fig_05.png`
- Nearby caption: Fig. 5 | Experimental and mechanistic characterization of the designed peptides assemblies. a, Atomic force microscopy (AFM) images revealing the distinct fibrillar morphology of GW1 (left) and IIQ (right). b, Circular dichroism (CD) spectra indicating the secondary structural differences between GW1 (red) and IIQ (blue). c, Representative snapshots from MD simulations of GW1 (left) and IIQ (right). Odd- and even-numbered residues are rendered in space-filling and stick representations, respectively. Insets (top right) display the backbone topology in cartoon representation. d, Root-mean-square fluctuation (RMSF) analysis showing higher structural flexibility for GW1 compared to IIQ. e, Distribution of twisting angles between two neighboring β-strands in GW1 (red) and IIQ (blue). The grey shaded area represents the distribution region of the angle between the two β-strands at the catalytic active center in the crystal structures of carbonic anhydrase.

## sapiens_main_fig_06.png
- Source: `SAPIENS.docx`
- Original media: `media/image6.png`
- Size: 1080 x 775 px
- File: `portfolio_site/assets/source_figures/sapiens/sapiens_main_fig_06.png`
- Nearby caption: Fig. 6 | Divergent design logics revealed by layer-wise relevance propagation (LRP) analysis. a-b, sequence logo of the peptides from rational design reported in literature (a) and from prediction from this work (b). c, Rational design benchmarks exhibit a strict alternating amphiphilic pattern, where hydrophobicity at position 6 contributes negatively to the prediction. d, SAPIENS identifies a hydrophobic anchor at position 5 and assigns positive relevance to hydrophobic residues at position 6, thereby deviating from the canonical alternating hydrophobic/hydrophilic pattern.

## sapiens_si_fig_01.png
- Source: `SAPIENS_SI.docx`
- Original media: `media/image1.png`
- Size: 830 x 658 px
- File: `portfolio_site/assets/source_figures/sapiens/sapiens_si_fig_01.png`
- Nearby caption: Supplementary Figure S1 | Construction Workflow of Peptide Self-Assembly Dataset.

## sapiens_si_fig_02.png
- Source: `SAPIENS_SI.docx`
- Original media: `media/image2.png`
- Size: 758 x 988 px
- File: `portfolio_site/assets/source_figures/sapiens/sapiens_si_fig_02.png`
- Nearby caption: Supplementary Figure S2 | Distribution of the retrieved literature. a. The year of publications. b. The top-30 publisher.

## sapiens_si_fig_03.png
- Source: `SAPIENS_SI.docx`
- Original media: `media/image3.png`
- Size: 1260 x 414 px
- File: `portfolio_site/assets/source_figures/sapiens/sapiens_si_fig_03.png`
- Nearby caption: Supplementary Figure S3 | Workflow for Data Mining of Peptide Self-Assembly Using Large Language Models

## sapiens_si_fig_04.png
- Source: `SAPIENS_SI.docx`
- Original media: `media/image4.png`
- Size: 1269 x 1060 px
- File: `portfolio_site/assets/source_figures/sapiens/sapiens_si_fig_04.png`
- Nearby caption: Supplementary Figure S4 | Performance metrics of peptide extraction using GPT-5 with a majority voting strategy. To evaluate the model's reliability, we extracted peptide sequences from 100 scientific literatures over 10 independent rounds (x-axis). A "majority voting" mechanism was applied where a peptide is considered valid only if its occurrence frequency exceeds a specific voting threshold (y-axis). The heatmaps illustrate four key metrics compared against a manually curated gold standard: the total number of extracted peptides, Precision, Recall, and F1 Score. The results indicate that GPT-5 achieves a stable baseline performance, with precision and recall showing a steady trade-off as the voting threshold increases.

## sapiens_si_fig_05.png
- Source: `SAPIENS_SI.docx`
- Original media: `media/image5.png`
- Size: 1269 x 1060 px
- File: `portfolio_site/assets/source_figures/sapiens/sapiens_si_fig_05.png`
- Nearby caption: Supplementary Figure S5 | Voting performance metrics for Gemini-2.5-pro in peptide sequence extraction. This figure displays the extraction performance of Gemini-2.5-pro across 10 rounds of execution on the same dataset of 100 literatures. The heatmaps follow the same layout as the previous figure, plotting performance against the number of rounds and voting threshold. Notably, Gemini-2.5-pro tends to extract a significantly higher volume of peptide candidates (as shown in the "Number of Extracted Peptides" panel). However, the Precision heatmap suggests that while the recall potential is high, a stricter voting threshold is required to filter out false positives and achieve precision levels comparable to other models.

## sapiens_si_fig_06.png
- Source: `SAPIENS_SI.docx`
- Original media: `media/image6.png`
- Size: 1269 x 1060 px
- File: `portfolio_site/assets/source_figures/sapiens/sapiens_si_fig_06.png`
- Nearby caption: Supplementary Figure S6 | Evaluation of DeepSeek-R1 performance and rationale for model selection. This figure characterizes the performance of DeepSeek-R1 under the majority voting framework. The four heatmaps demonstrate the model's ability to extract peptides with varying rounds (1-10) and voting thresholds. DeepSeek-R1 was ultimately selected for the final extraction pipeline. As illustrated in the Precision and Recall panels, this model exhibits a superior balance of performance metrics. Specifically, it achieves relatively high precision at moderate-to-high voting thresholds, which is critical for ensuring data quality, while maintaining a considerable recall rate. This high accuracy, combined with its significantly lower cost compared to GPT-5 and Gemini-2.5-pro, makes DeepSeek-R1 the most cost-effective and reliable solution for large-scale peptide mining tasks.

## sapiens_si_fig_07.png
- Source: `SAPIENS_SI.docx`
- Original media: `media/image7.png`
- Size: 1846 x 399 px
- File: `portfolio_site/assets/source_figures/sapiens/sapiens_si_fig_07.png`
- Nearby caption: Supplementary Figure S7 | Transformer-based architecture of SAPIENS.

## sapiens_si_fig_08.png
- Source: `SAPIENS_SI.docx`
- Original media: `media/image8.png`
- Size: 803 x 1004 px
- File: `portfolio_site/assets/source_figures/sapiens/sapiens_si_fig_08.png`
- Nearby caption: Supplementary Figure S8 | Ablation study and performance validation of the SAPIENS multi-task learning framework. a, Predictive performance metrics for different model configurations. The single-task baseline (“cata only”, green) is significantly improved upon by adding auxiliary tasks: sequence reconstruction ("+sequence", blue) and self-assembly prediction ("+sa", purple). The complete SAPIENS model ("+sa+sequence", orange) achieves peak performance across all metrics, notably reaching an NDCG of 0.87. b, Predicted vs. experimental catalytic efficiency (log scale) correlation on the test set. Single-task models show poor prediction clustering (top left). Progressive integration of auxiliary losses refines ranking ability. The full multi-task SAPIENS model (bottom right) shows markedly superior enrichment of high-activity sequences in the top ranks, indicating reduced false positives compared to simpler models.

## sapiens_si_fig_09.png
- Source: `SAPIENS_SI.docx`
- Original media: `media/image9.png`
- Size: 1268 x 394 px
- File: `portfolio_site/assets/source_figures/sapiens/sapiens_si_fig_09.png`
- Nearby caption: Supplementary Figure S9 | Navigation of the peptide sequence space () visualized via ESM-C embeddings. a, Comparison of the structural landscape of generated self-assembling sequences (blue points) against the global background (light grey). b, Activity mapping, where deep blue regions indicate high predicted catalytic potential, acting as a “searchlight” to prioritize functional clusters in the sequence space. c, Discovery of distinct active sequence regions. SAPIENS candidates (red stars) occupy high-activity clusters that are spatially distinct from those based on rational design reported in the literature (purple circles) 3, confirming the exploration of novel functional subspaces derived from AI-discovered logic.

## sapiens_si_fig_10.png
- Source: `SAPIENS_SI.docx`
- Original media: `media/image10.png`
- Size: 1377 x 513 px
- File: `portfolio_site/assets/source_figures/sapiens/sapiens_si_fig_10.png`
- Nearby caption: Supplementary Figure S10 | Correlation analysis between model predictions and coarse-grained molecular dynamics (CGMD) simulation results. The scatter plots compare the predicted scores from SAPIENS (left panel, this work) and Mausa et al. (right panel, previous work 10) against the Aggregation Propensity (AP) calculated from CGMD simulations for a set of 400 peptides 11. The linear regression lines (green) and Spearman correlation coefficients () indicate the degree of alignment. SAPIENS demonstrates a noticeably stronger correlation () compared to the baseline method (). Importantly, SAPIENS predictions are derived exclusively from data mined from scientific literature and were not trained or fine-tuned on simulation data, ensuring there is no data leakage. Although CGMD provides critical physical insights, it is debated within the field and not regarded as “gold standard.” Thus, this alignment functions as a corroborative reference to verify that SAPIENS captures trends consistent with simulation dynamics, rather than serving as a strict ground-truth accuracy benchmark.

## sapiens_si_fig_11.png
- Source: `SAPIENS_SI.docx`
- Original media: `media/image11.png`
- Size: 707 x 953 px
- File: `portfolio_site/assets/source_figures/sapiens/sapiens_si_fig_11.png`
- Nearby caption: Supplementary Figure S11 | Hydrolytic activity of peptides GW1 versus IIQ towards a panel of esters.

## sapiens_si_fig_12.png
- Source: `SAPIENS_SI.docx`
- Original media: `media/image12.png`
- Size: 943 x 694 px
- File: `portfolio_site/assets/source_figures/sapiens/sapiens_si_fig_12.png`
- Nearby caption: Supplementary Figure S12 | Time-dependent secondary structural changes of GW1 monitored by circular dichroism (CD).

## sapiens_si_fig_13.png
- Source: `SAPIENS_SI.docx`
- Original media: `media/image13.png`
- Size: 1572 x 599 px
- File: `portfolio_site/assets/source_figures/sapiens/sapiens_si_fig_13.png`
- Nearby caption: Supplementary Figure S13 | Hydrophobic packing arrangement of GW1 (left) and IIQ (right). The backbone is in cartoon representation; sidechain of key hydrophobic residue is in stick representation. For clarity, only two β-strands per layer (top and bottom) are displayed. Distances are in Å.

## sapiens_si_fig_14.png
- Source: `SAPIENS_SI.docx`
- Original media: `media/image14.png`
- Size: 866 x 724 px
- File: `portfolio_site/assets/source_figures/sapiens/sapiens_si_fig_14.png`
- Nearby caption: Supplementary Figure S14 | Catalytic efficiency of GW1 on pNPA hydrolysis.

# ChemBART Extracted Figures

Extracted from `ChemBart.docx` and `ChemBart_SI.docx` using the DOCX media archive.

Note: many SI figures are embedded as `.emf` vector files. They are preserved, but they are not browser-safe for the website until converted to PNG/SVG with LibreOffice/Inkscape/ImageMagick or another EMF-capable renderer.

## chembart_main_fig_01.png
- Source: `ChemBart.docx`
- Original media: `media/image1.png`
- Size: 1203 x 616 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_main_fig_01.png`
- Nearby caption: Fig. 1 | Overview of ChemBART. ChemBART is a language model pre-trained on chemical reaction data via a mask-filling objective. The model enables direct prediction of reaction precursors and reagents using its pre-trained parameters. Through fine-tuning, ChemBART extends its utility to detailed reaction analysis and molecular property prediction, streamlining chemical synthesis. By integrating reinforcement learning (RL) with Monte Carlo tree search (MCTS), the model facilitates multi-step synthesis planning by leveraging insights gained from auxiliary tasks. These computational routes guide wet-lab validation, which in turn provides experimental feedback to refine the model.

## chembart_main_fig_02.png
- Source: `ChemBart.docx`
- Original media: `media/image2.png`
- Size: 1661 x 1109 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_main_fig_02.png`
- Nearby caption: Fig. 2 | Interpretability analysis of the ChemBART model. (a) Euclidean distances between characteristic element representations in the embedding layer. (b) 2D projections of the reaction pathway. Alcohols (circle), aldehydes (triangle), and acids (square) of the same series are represented by the same color; arrows indicate oxidation pathways. (c) The encoder’s last-layer attention matrix during masked product prediction for a Grignard reaction.

## chembart_main_fig_03.png
- Source: `ChemBart.docx`
- Original media: `media/image3.png`
- Size: 1269 x 348 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_main_fig_03.png`
- Nearby caption: Fig. 3 | Performance of joint regression of temperature and yield. (a) Temperature prediction (R²=0.55, MAE=10%), (b) Yield prediction (R²=0.16, MAE=23%), with heatmap intensity reflecting data density per 40°C/10% interval. The apparent yields of 100–110% are attributed to experimental errors in quantifying reactions with actual yields near the theoretical maximum. (c) Yield prediction on Suzuki-Miyaura dataset (R2=0.816, MAE=7.9%) using one data split.

## chembart_main_fig_04.png
- Source: `ChemBart.docx`
- Original media: `media/image4.png`
- Size: 1270 x 1306 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_main_fig_04.png`
- Nearby caption: Fig. 4 | A 15-step synthetic pathway for compound 2673 designed by ChemBART. Panels (a), (b), and (c) show the planned paths for intermediates 14 and 17, and the target molecule 26, respectively.

## chembart_main_fig_05.png
- Source: `ChemBart.docx`
- Original media: `media/image6.png`
- Size: 1267 x 430 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_main_fig_05.png`
- Nearby caption: Fig. 6 | Frameworks for classification, regression, and generation tasks using Transformers. (a) BART’s classification/regression scheme: Task-specific tokens are appended to the input sequence. The complete sequence is processed by both the encoder and decoder. The decoder’s output corresponding to each task token is passed through a linear layer to obtain the classification or regression label. (b) BERT’s classification/regression scheme: Task-specific tokens are prepended to the input sequence. The encoder processes the entire sequence, and the output corresponding to each task token is passed through a linear layer to obtain the classification or regression label. (c) Fitting policy and value functions: A pre-trained model generates multiple possible precursors for a specific product. The value function v is obtained by inputting the product’s expression into a fine-tuned regression model. The policy function p is derived by inputting each corresponding synthetic reaction for all precursor options into a fine-tuned regression model, then normalizing the output probabilities.

## chembart_main_media_unmapped_006.emf
- Source: `ChemBart.docx`
- Original media: `media/image5.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_main_media_unmapped_006.emf`
- Nearby caption: not detected

## chembart_si_fig_001.jpeg
- Source: `ChemBart_SI.docx`
- Original media: `media/image2.jpeg`
- Size: 1269 x 620 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_001.jpeg`
- Nearby caption: not detected

## chembart_si_fig_002.jpeg
- Source: `ChemBart_SI.docx`
- Original media: `media/image4.jpeg`
- Size: 1268 x 620 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_002.jpeg`
- Nearby caption: not detected

## chembart_si_fig_003.png
- Source: `ChemBart_SI.docx`
- Original media: `media/image6.png`
- Size: 2204 x 606 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_003.png`
- Nearby caption: not detected

## chembart_si_fig_004.jpeg
- Source: `ChemBart_SI.docx`
- Original media: `media/image8.jpeg`
- Size: 1268 x 620 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_004.jpeg`
- Nearby caption: Supplementary Figure SA1 | 1H NMR (400 MHz, CDCl3) of 36

## chembart_si_fig_005.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image9.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_005.emf`
- Nearby caption: Supplementary Figure SA1 | 1H NMR (400 MHz, CDCl3) of 36

## chembart_si_fig_006.jpeg
- Source: `ChemBart_SI.docx`
- Original media: `media/image10.jpeg`
- Size: 1269 x 886 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_006.jpeg`
- Nearby caption: Supplementary Figure SA1 | 1H NMR (400 MHz, CDCl3) of 36

## chembart_si_fig_007.jpeg
- Source: `ChemBart_SI.docx`
- Original media: `media/image11.jpeg`
- Size: 1269 x 886 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_007.jpeg`
- Nearby caption: Supplementary Figure SA2 | 13C NMR (100 MHz, CDCl3) of 36

## chembart_si_fig_008.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image12.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_008.emf`
- Nearby caption: Supplementary Figure SA3 | 1H NMR (400 MHz, CDCl3) of 37

## chembart_si_fig_009.jpeg
- Source: `ChemBart_SI.docx`
- Original media: `media/image13.jpeg`
- Size: 1269 x 886 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_009.jpeg`
- Nearby caption: Supplementary Figure SA3 | 1H NMR (400 MHz, CDCl3) of 37

## chembart_si_fig_010.jpeg
- Source: `ChemBart_SI.docx`
- Original media: `media/image14.jpeg`
- Size: 1269 x 886 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_010.jpeg`
- Nearby caption: Supplementary Figure SA4 | 13C NMR (100 MHz, CDCl3) of 37

## chembart_si_fig_011.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image15.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_011.emf`
- Nearby caption: Supplementary Figure SA5 | 1H NMR (400 MHz, DMSO-d6) of 38

## chembart_si_fig_012.png
- Source: `ChemBart_SI.docx`
- Original media: `media/image16.png`
- Size: 2754 x 1922 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_012.png`
- Nearby caption: Supplementary Figure SA5 | 1H NMR (400 MHz, DMSO-d6) of 38

## chembart_si_fig_013.png
- Source: `ChemBart_SI.docx`
- Original media: `media/image17.png`
- Size: 2754 x 1922 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_013.png`
- Nearby caption: Supplementary Figure SA6 | 13C NMR (101 MHz, DMSO-d6) of 38

## chembart_si_fig_014.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image18.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_014.emf`
- Nearby caption: Supplementary Figure SA7 | 1H NMR (400 MHz, DMSO-d6) of P1

## chembart_si_fig_015.jpeg
- Source: `ChemBart_SI.docx`
- Original media: `media/image19.jpeg`
- Size: 1269 x 886 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_015.jpeg`
- Nearby caption: Supplementary Figure SA7 | 1H NMR (400 MHz, DMSO-d6) of P1

## chembart_si_fig_016.jpeg
- Source: `ChemBart_SI.docx`
- Original media: `media/image20.jpeg`
- Size: 1269 x 886 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_016.jpeg`
- Nearby caption: Supplementary Figure SA8 | 13C NMR (100 MHz, DMSO-d6) of P1

## chembart_si_fig_017.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image21.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_017.emf`
- Nearby caption: Supplementary Figure SA9 | HRMS of 36

## chembart_si_fig_018.png
- Source: `ChemBart_SI.docx`
- Original media: `media/image22.png`
- Size: 1134 x 660 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_018.png`
- Nearby caption: Supplementary Figure SA9 | HRMS of 36

## chembart_si_fig_019.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image12.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_019.emf`
- Nearby caption: Supplementary Figure SA10 | HRMS of 37

## chembart_si_fig_020.png
- Source: `ChemBart_SI.docx`
- Original media: `media/image23.png`
- Size: 1079 x 708 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_020.png`
- Nearby caption: Supplementary Figure SA10 | HRMS of 37

## chembart_si_fig_021.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image15.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_021.emf`
- Nearby caption: Supplementary Figure SA11 | HRMS of 38

## chembart_si_fig_022.png
- Source: `ChemBart_SI.docx`
- Original media: `media/image24.png`
- Size: 1083 x 690 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_022.png`
- Nearby caption: Supplementary Figure SA11 | HRMS of 38

## chembart_si_fig_023.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image18.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_023.emf`
- Nearby caption: Supplementary Figure SA12 | HRMS of P1

## chembart_si_fig_024.png
- Source: `ChemBart_SI.docx`
- Original media: `media/image25.png`
- Size: 1080 x 693 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_024.png`
- Nearby caption: Supplementary Figure SA12 | HRMS of P1

## chembart_si_fig_025.png
- Source: `ChemBart_SI.docx`
- Original media: `media/image26.png`
- Size: 882 x 737 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_025.png`
- Nearby caption: Supplementary Figure S1 | The top-k success rate for reactant prediction on USPTO-MIT dataset for ChemBART training. After the 7th epoch, model convergence observed.

## chembart_si_fig_026.png
- Source: `ChemBart_SI.docx`
- Original media: `media/image27.png`
- Size: 900 x 737 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_026.png`
- Nearby caption: Supplementary Figure S2 | The top-k syntax error rate for reactant prediction on USPTO-MIT dataset for ChemBART training.

## chembart_si_fig_027.png
- Source: `ChemBart_SI.docx`
- Original media: `media/image28.png`
- Size: 712 x 712 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_027.png`
- Nearby caption: Supplementary Figure S3 | 3D visualization using PCA and ChemBART embeddings for the top 20 most frequent elements in the USPTO dataset. The resulting visualization suggests the model has learned certain periodic trends: clustering is observed for organic backbone elements from the same period C, N, O; elements from the same group H, Li, Na, K, Cs and F, Cl, Br, I are nearer in the PCA space; additionally, elements with lower electronegativity B, Al, Si, Cu, Pd, Sn also show a tendency to cluster.

## chembart_si_fig_028.png
- Source: `ChemBart_SI.docx`
- Original media: `media/image29.png`
- Size: 1267 x 530 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_028.png`
- Nearby caption: Supplementary Figure S4 | The cross-attention matrix generated by the ChemBART model for a Grignard reaction, CH3(CH2)5Br + PhMgBr  CH3(CH2)5Ph + MgBr2, by masking the product. (A) The entire reaction; (B) Bromine atom and related atoms; (C) Carbon anion and related atoms.

## chembart_si_fig_029.png
- Source: `ChemBart_SI.docx`
- Original media: `media/image30.png`
- Size: 1271 x 542 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_029.png`
- Nearby caption: Supplementary Figure S5 | The decoder attention matrix generated by the ChemBART model for a Grignard reaction, CH3(CH2)5Br + PhMgBr  CH3(CH2)5Ph + MgBr2, by masking the product. (A) The entire reaction; (B) Bromine atom and related atoms; (C) Carbon anion and related atoms.

## chembart_si_fig_030.png
- Source: `ChemBart_SI.docx`
- Original media: `media/image31.png`
- Size: 1269 x 489 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_030.png`
- Nearby caption: Supplementary Figure S6 | Attention matrices generated by the ChemBART model for a reaction, PhO(CH2)3CH3+Cl2o-ClPhO(CH2)3CH3+p-ClPhO(CH2)3CH3, with products masked. (a-c) Encoder, cross, and decoder attention matrices, respectively. The top panel is about entire reaction, and the bottom panel is about n-Butyl phenyl ether and Cl2.

## chembart_si_fig_031.png
- Source: `ChemBart_SI.docx`
- Original media: `media/image32.png`
- Size: 1269 x 665 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_031.png`
- Nearby caption: Supplementary Figure S7 | Encoder attention matrix generated by masking the reagents for products to reactants (a), and for reactants to products (b).

## chembart_si_fig_032.png
- Source: `ChemBart_SI.docx`
- Original media: `media/image33.png`
- Size: 1000 x 640 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_032.png`
- Nearby caption: Supplementary Figure S8 | Correlation between model size and top-5 accuracy for single-step retrosynthesis on the USPTO-50k dataset. ChemBART achieves relatively strong performance among models of similar size.

## chembart_si_fig_033.png
- Source: `ChemBart_SI.docx`
- Original media: `media/image34.png`
- Size: 1002 x 822 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_033.png`
- Nearby caption: Supplementary Figure S9 | Fine-tuning the pre-trained model on specific datasets enhances the distinction in molecular feature vector distributions. (a-b) The BBBP dataset, before (a) and after (b) fine-tuning, where dark and light shades represent non-penetrating and penetrating molecules, respectively. (c-d) The BACE dataset, before (c) and after (d) fine-tuning, where dark and light shades correspond to non-binders and binders, respectively.

## chembart_si_fig_034.png
- Source: `ChemBart_SI.docx`
- Original media: `media/image35.png`
- Size: 790 x 590 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_034.png`
- Nearby caption: Supplementary Figure S10 | Comparison between ReSynZ and ChemBART in the training of value function. Pre-trained ChemBART-F/M fits value function data well with a lower minimum validation RMSE compared to ReSynZ, while ChemBART-R performs significantly worse.

## chembart_si_fig_035.png
- Source: `ChemBart_SI.docx`
- Original media: `media/image36.png`
- Size: 790 x 590 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_035.png`
- Nearby caption: Supplementary Figure S11 | Comparison between ReSynZ and ChemBART in the training of policy function. Pre-trained ChemBART-F/M show good fitting performance on policy function, while ChemBART-R and ReSynZ exhibit early over-fitting.

## chembart_si_fig_036.png
- Source: `ChemBart_SI.docx`
- Original media: `media/image37.png`
- Size: 1106 x 967 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_036.png`
- Nearby caption: Supplementary Figure S12 | Probability distributions for 53 molecules from the JMC2025 dataset across six properties. (a) LogP, the logarithm of the partition coefficient. (b) MW, molecular weight. (c) QED, quantitative estimate of drug-likeness, quantifies drug-likeness by taking into account the main molecular properties, ranging from 0 (unfavorable) to 1 (favorable). (d) TPSA, topological polar surface area, the sum of surface area over all polar atoms. (e) SAS, synthetic accessibility score, the measurement of the difficulty of synthesizing a compound. It is a score between 1 (easy to make) and 10 (very difficult to make). (f) Heavy atom count.

## chembart_si_fig_037.png
- Source: `ChemBart_SI.docx`
- Original media: `media/image38.png`
- Size: 1180 x 968 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_037.png`
- Nearby caption: Supplementary Figure S13 | t-SNE plot of 53 molecular Morgan fingerprints from the JMC20225 dataset.

## chembart_si_fig_038.png
- Source: `ChemBart_SI.docx`
- Original media: `media/image103.png`
- Size: 2445 x 1624 px
- Browser-safe now: yes
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_038.png`
- Nearby caption: Supplementary Figure S36 | Comparison of the three generation strategies for single-step retrosynthesis on JMC2025 dataset in result diversity and validness.

## chembart_si_fig_039.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image119.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_fig_039.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_040.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image1.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_040.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_041.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image100.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_041.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_042.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image101.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_042.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_043.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image102.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_043.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_044.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image104.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_044.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_045.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image105.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_045.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_046.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image106.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_046.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_047.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image107.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_047.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_048.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image108.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_048.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_049.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image109.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_049.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_050.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image110.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_050.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_051.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image111.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_051.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_052.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image112.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_052.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_053.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image113.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_053.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_054.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image114.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_054.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_055.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image115.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_055.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_056.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image116.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_056.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_057.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image117.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_057.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_058.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image118.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_058.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_059.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image3.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_059.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_060.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image39.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_060.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_061.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image40.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_061.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_062.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image41.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_062.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_063.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image42.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_063.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_064.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image43.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_064.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_065.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image44.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_065.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_066.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image45.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_066.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_067.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image46.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_067.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_068.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image47.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_068.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_069.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image48.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_069.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_070.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image49.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_070.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_071.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image5.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_071.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_072.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image50.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_072.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_073.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image51.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_073.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_074.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image52.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_074.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_075.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image53.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_075.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_076.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image54.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_076.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_077.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image55.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_077.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_078.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image56.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_078.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_079.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image57.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_079.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_080.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image58.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_080.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_081.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image59.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_081.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_082.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image60.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_082.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_083.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image61.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_083.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_084.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image62.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_084.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_085.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image63.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_085.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_086.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image64.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_086.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_087.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image65.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_087.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_088.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image66.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_088.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_089.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image67.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_089.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_090.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image68.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_090.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_091.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image69.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_091.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_092.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image7.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_092.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_093.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image70.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_093.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_094.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image71.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_094.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_095.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image72.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_095.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_096.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image73.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_096.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_097.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image74.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_097.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_098.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image75.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_098.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_099.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image76.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_099.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_100.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image77.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_100.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_101.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image78.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_101.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_102.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image79.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_102.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_103.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image80.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_103.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_104.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image81.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_104.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_105.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image82.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_105.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_106.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image83.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_106.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_107.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image84.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_107.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_108.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image85.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_108.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_109.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image86.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_109.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_110.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image87.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_110.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_111.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image88.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_111.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_112.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image89.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_112.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_113.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image90.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_113.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_114.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image91.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_114.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_115.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image92.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_115.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_116.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image93.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_116.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_117.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image94.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_117.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_118.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image95.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_118.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_119.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image96.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_119.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_120.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image97.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_120.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_121.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image98.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_121.emf`
- Nearby caption: not detected

## chembart_si_media_unmapped_122.emf
- Source: `ChemBart_SI.docx`
- Original media: `media/image99.emf`
- Size: not readable by local image renderer, likely EMF
- Browser-safe now: no
- File: `portfolio_site/assets/source_figures/chembart/chembart_si_media_unmapped_122.emf`
- Nearby caption: not detected

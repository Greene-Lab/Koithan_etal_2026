# pMTG Functional Connectivity and Cognitive Retrieval in Early Adolescence (Koithan et al. 2026)

Code for analyses reported in "pMTG Functional Connectivity and Cognitive Retrieval in Early Adolescence," aimed at characterizing posterior middle temporal gyrus (pMTG) functional connectivity (FC), identifying pMTG FC subtypes, and examining relationships between pMTG FC and retrieval task performance in early adolescence.

## Analysis Workflow

1. `variants.ipynb` evaluates the spatial robustness of the pMTG regions of high inter-individual variability across variant density thresholds, between typically developing and atypically developing subjects, and using jackknife analyses.
2. `calculating_fc.py` calculates FC between pMTG regions and large-scale resting-state brain networks.
3. `data_wrangling.ipynb` merges FC, demographic, behavioral, imaging-quality, and motion data from ABCD, applies sample selection criteria (e.g., filters out high-motion subjects), and preps the analysis dataframe.
4. `PCA_tasks.ipynb` performs exploratory factor analysis of the cognitive retrieval measures with and without controlling for INR.
5. `PCA_FC.ipynb` performs PCA of pMTG FC.
6. `clustering.ipynb` identifies pMTG FC subtypes using Infomap, Louvain, and K-Means. It also evaluates repeated-run agreement and bootstrap stability.
7. `cluster_solution_jaccard.ipynb` compares Infomap and KMeans clustering consensus solutions with and without controlling for INR.
8. `brain_behavior_without_inr_residualization.ipynb` and `brain_behavior_with_inr_residualization.ipynb` run matched brain–behavior and subtype analyses with and without residualizing for INR. The no-INR analysis also computes FC-INR correlations and mediation analyses determining whether pMTG connectivity mediates relationships between SES and task performance.
9. `figures.ipynb` produces some of the figures from the manuscript (others are created in the brain-behavior notebooks).



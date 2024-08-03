Step 1: Download Enrichment Results
- Description:
1) Download enrichment results for Gene Ontology Biological Processes (GO BP), KEGG pathways, and Reactome pathways from the DAVID tool in a txt format.
2) Name the downloaded files as follows:
For GO BP: "aorta_gobp.txt", "carotid_gobp.txt", "coronary_gobp.txt", "aorta_kegg.txt"
For KEGG pathways: "carotid_kegg.txt", "coronary_kegg.txt"
For Reactome pathways: "aorta_reactome.txt", "carotid_reactome.txt", "coronary_reactome.txt" 

Step 2: Prepare TXT Files for Downstream Analyses
- R script name: "1_Prepare_file_for_analyses.R"
- Input file examples: "aorta_gobp.txt", "carotid_gobp.txt", "coronary_gobp.txt"
- Output file examples:
For semantic similarity analysis: "aorta_gobp_for_ss.txt", "carotid_gobp_for_ss.txt", "coronary_gobp_for_ss.txt"
For functional comparative analysis: "aorta_gobp_for_cc.txt", "carotid_gobp_for_cc.txt", "coronary_gobp_for_cc.txt"

Step 3: Perform Semantic Similarity Analysis
- R script name: "2_Semantic_similarity.R"
- Input file examples: "aorta_gobp_for_ss.txt", "carotid_gobp_for_ss.txt", "coronary_gobp_for_ss.txt"
- Output file example: "go_semantic_similarity_top10.pdf"

Step 4: Perform Functional Comparative Analysis
- R script name: "3_Compare_cluster.R"
- Input file examples: "aorta_gobp_for_cc.txt", "carotid_gobp_for_cc.txt", "coronary_gobp_for_cc.txt"
- Output file examples: "compareCluster_gobp_top10.pdf" and "compareCluster_gobp.csv"

Step 5: Process CSV File for Dot Plot of Unique Pathways
- Description: Create a FoldEnrichment column and calculate fold enrichment for each term from values in GeneRatio divided by BgRatio.
- Pre-processed file example: "compareCluster_gobp.csv"
- Processed file example: "diff_vessels_gobp_fordotplot.csv"

Step 6: Generate Dot Plot for Unique Pathways
- R script name: "4_Unique_pathways.R"
- Input file examples: "diff_vessels_gobp_fordotplot.csv"
- Output file examples: "diff_vessels_gobp_dotplot.pdf"

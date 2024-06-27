# Fecal-Microbiome-of-Toothed-and-Baleen-Whales
Codes and files we used for ASB assignment 2

**Code Usage**
pca:
'''
beta_div <- read.delim("beta-div.tsv", sep = "\t", header = TRUE)
'''
in this line where "beta-div.tsv" you can change for whichever beta diversity csv file path you want and run it to generate a PCA graph

shannon:
'''
alpha_div <- data.frame(
  group = c("Bph055", "Bph050", "Bph049", "Bph048", "Bph044", "BphF003", "Bmu025", 
            "Pma188", "Pma185", "Pma179", "Bph063", "Bph058", "Bph057", "Bmu018", "Bbo036"),
  shannon = c(1.546847, 2.77671, 2.10136, 2.861532, 2.356537, 2.061215, 2.115312, 
              1.841776, 2.728204, 2.578837, 2.703602, 2.838636, 2.553966, 1.913494, 0.866619)
'''
copy and paste the data from your csv alpha diversity file into two vectors. 'Group' has the names of the samples and 'shannon' has the shannon index number we couldn't import the csv file as a whole so we just made a dataframe

accession processor 
'''
mapping_file_path = 'mapping_file.txt'
input_file_path = 'alpha-diversity.97.summary'
output_file_path = 'updated_alpha-diversity.summary'
'''
the 'mapping_file.txt' has the content in columns, the first column is the accession numbers and the second column is the names of the samples.
the 'alpha-diversity.97.summary' is the file path of your alpha diversity summary file 
the 'updated_alpha-diversity.summary' is the name of the output file you want. it has the alpha diversity with the name samples over the accession number

to run this script in shell:
'''
python3 accession.py alpha-diversity.97.summary
'''

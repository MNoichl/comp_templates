# Tracing the texture of mathematicised science
Anonymized code for the analysis underlying the article  *Tracing the texture of mathematicised science*

The code is organized in anonymized jupyter notebooks. It contains all steps necessary to procure the dataset, format it adequately, and conduct the exploratory analysis presented in the paper. Because several steps of the data-procurement are both financially and computationally expensive, the final two analysis-notebooks are set up to load well formatted external datasets. All notebooks contain links at the top that should make it very easy to open and run them in the google-colab cloud-computing environment. The notebook containing the formula analysis might be a bit to RAM-intensive for colabs free instances, so that either  a pro-subscription, or a reduction of the sample-size might be necessary for replication.

## The notebooks are

* *procuring_arxiv_data.ipynb* – contains code to download all arXiv-fulltexts from the AWS-bucket.
* *downloading_biorxiv_fulltexts.ipynb* – contains code to download all bioRxiv-fulltexts and formula-images from the AWS-bucket.
* *converting_biorxiv_formulas_to_LaTeX.ipynb* – contains code to convert the images of formulas from the bioRxiv into LaTeX
* *convert_latex_to_mathml.ipynb* – contains code to convert latex to MathML, as required by TangentCFT
* *text_layout.ipynb* – Contains code to download the meta-data from arXiv and bioRxiv, and lay out the abstracts of the articles using UMAP.
* *formulas_training_and_analysis.ipynb* – Contains code to train the FastText model required by TangentCFT, to apply the model to a sample of formulas, to lay them out using umap, and to analyze the resulting structures.

## Abstract
A commonly held background assumption about the sciences is, that they are organised in a hierarchical structure, which usually is thought to follow the order: mathematics, physics, chemistry, biology, psychology, and the social sciences, with interdisciplinary work arising in the bordering regions of adjacent disciplines. Philosophical research into interdisciplinary model transfer has increasingly complicated this picture. But most of these works have been done through case studies, which due to their limited scope are hard-pressed to provide foundations for claims about large-scale relations between multiple scientific disciplines. As an alternative, in this contribution, we propose to philosophers of science the use of modern science mapping techniques to trace connections between modelling techniques in large samples of the literature. We explain in detail how these techniques work, and apply them to a large, contemporary and multidisciplinary data set (n=383.961 articles). Through the comparison of textual to mathematical representations, we suggest formulaic structures that are particularly common among different disciplines and produce first results indicating the general strength and commonality of such relationships

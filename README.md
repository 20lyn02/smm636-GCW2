<h1>Movie Clustering with PCA and Unsupervised Learning</h1>

<h2>Description</h2>
This project applied unsupervised machine learning techniques to a dataset of 50 top-rated IMDb movies. The objective was to reduce dimensionality using PCA and uncover meaningful clusters with K-Means and Hierarchical clustering. The project also compared manual analysis with ChatGPT-4o’s output to critically evaluate the reliability of LLMs in data analysis tasks.
<br />

<h2>Languages and Utilities Used</h2>

- <b>Python</b>  
- <b>Principal Component Analysis (PCA)</b>  
- <b>K-Means Clustering</b>  
- <b>Hierarchical Clustering</b>  
- <b>Silhouette Scoring</b>  
- <b>ChatGPT-4o Comparative Analysis</b>  


<h2>Methodology</h2>

1. <b>Data Preprocessing</b>  
   - Cleaned and prepared the IMDb dataset of 50 top-rated movies.  
   - Excluded the <i>Year</i> variable and standardised numerical features (Runtime, Rating, Votes, Revenue).  

2. <b>Principal Component Analysis (PCA)</b>  
   - Reduced dimensionality to identify key factors driving variance.  
   - Selected 3 principal components, explaining over 92% of total variance.  
   - Interpreted PCs as:  
     - PC1: Popularity / Commercial Success (Votes, Revenue)  
     - PC2: Quality vs. Commercial Performance (Runtime, Rating vs. Revenue)  
     - PC3: Runtime vs. Rating trade-off  

3. <b>K-Means Clustering</b>  
   - Applied clustering to PCA-transformed data.  
   - Used elbow method and silhouette score to determine optimal <i>K</i>.  
   - Chose 6 clusters (silhouette score ≈ 0.376), balancing compactness and separation.  

4. <b>Hierarchical Clustering</b>  
   - Tested complete, average, and single linkage methods.  
   - Average linkage produced 7 clusters with the highest silhouette score (0.378).  
   - Interpreted dendrograms to validate within-cluster similarities.  

5. <b>Qualitative Cluster Analysis</b>  
   - Analysed clusters for interpretability, identifying meaningful themes (e.g., Pixar/Disney family films, Nolan/Tarantino/Scorsese collaborations, Bollywood films with Aamir Khan, international dramas).  

6. <b>ChatGPT-4o Comparison</b>  
   - Replicated PCA and clustering with ChatGPT-4o.  
   - Compared results, highlighting oversimplification (e.g., defaulting to 2 clusters) and lack of methodological robustness without human oversight.  

<h2>Findings</h2>

- PCA revealed three key latent dimensions capturing movie popularity, critical quality, and trade-offs between runtime and ratings.  
- K-Means suggested 6 clusters, while Hierarchical clustering suggested 7, with marginal differences in silhouette scores.  
- Hierarchical clustering provided slightly clearer interpretability, particularly in segmenting Bollywood films and family-oriented animation.  
- Identified meaningful thematic clusters such as:  
  - <b>High-Budget Blockbusters</b> (Avengers, Star Wars)  
  - <b>Family Films</b> (Pixar & Disney titles)  
  - <b>International Dramas</b> (diverse origin, drama-heavy)  
  - <b>Bollywood Films</b> (Aamir Khan-led)  
  - <b>Director-Focused Clusters</b> (Nolan, Tarantino, Scorsese with DiCaprio)  
- ChatGPT-4o’s analysis produced some correct insights but defaulted to oversimplified solutions (2–3 clusters) without prompting, underscoring the need for human validation.  
- Overall, combining PCA with multiple clustering methods yielded richer, more reliable segmentation than automated outputs alone.  

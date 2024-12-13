# Computer-Science
# Duplicate Product Detection Using LSH

This project introduces a methodology to identify duplicate products in large-scale e-commerce datasets.
the following steps are involved:
-**Data cleaning and preprocesing for consistency**
- **Model words** and **key-value pairs** extracted from product attributes.
- **Locality Sensitive Hashing (LSH)** to efficiently select candidate pairs.
- **MinHash signatures** and a **banding technique** to reduce comparisons.
- A **Multi-Component Similarity (MSM)** metric combining cosine, Jaccard, Q-gram, key-value matching, and hierarchical structure matching.
- **Hierarchical clustering** to group related duplicates.
- **bootstrapping** to obtain robust metrics.

## Project Structure

- **Data Loading and Preprocessing**: 
  - Loads a JSON file of product attributes.
  - Cleans and normalizes numeric and categorical features.
  - Extracts model words and applies one-hot encoding.

- **LSH Candidate Generation**:
  - Creates MinHash signatures from one-hot encoded model words.
  - Uses banding to form buckets of similar items and identify candidate duplicates.

- **Similarity Computation and Clustering**:
  - Calculates MSM similarity scores for candidate pairs.
  - Performs hierarchical clustering to refine duplicate detection.

- **Evaluation**:
  - Uses bootstrapping to assess performance stability.
  - Reports metrics (Precision, Recall, F1, Pair Quality, Pair Completeness, F1*).

## How to Use the Code

1. **Data Preparation**:  
   Substitude file path for the JSON dataset path in `file_path` definition.

2. **Run the Script**:  
 
3. **Parameters (b,r)**:  
2 graphs of different configurations of b and r will show. In order to continue running the code, they should be closed, since the rest is run with a preset configuration and these graphs were generated to be included in the final paper.

## Requirements

- Python 3.x
- `pandas`, `numpy`
- `scikit-learn`
- `matplotlib`
- `scipy`
- `re` (built-in)

## Results

The script prints evaluation metrics (average Precision, average Recall, average F1-measure, average pair quality, average pair completeness, average F1*-Measure) and generates plots for "Pair completeness", "Pair Quality", "F1 score" and "F1* score" vs the fractions of comparisons. 





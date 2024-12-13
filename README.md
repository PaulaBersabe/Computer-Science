# Computer-Science
# Duplicate Product Detection Using LSH

This project demonstrates a methodology for identifying duplicate products in large-scale e-commerce datasets. It leverages:

- **Locality Sensitive Hashing (LSH)** to efficiently select candidate pairs.
- **Model words** and **key-value pairs** extracted from product attributes.
- **MinHash signatures** and a **banding technique** to reduce comparisons.
- A **Multi-Component Similarity (MSM)** metric combining cosine, Jaccard, Q-gram, key-value matching, and hierarchical structure matching.
- **Hierarchical clustering** to group related duplicates.

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
   Place your JSON dataset path in `file_path`.

2. **Run the Script**:  
   Execute the Python script to:
   - Load and preprocess the data.
   - Generate candidate pairs via LSH.
   - Compute similarities and cluster products.
   - Evaluate performance metrics.

3. **Adjust Parameters**:  
   Modify LSH parameters (`b`, `r`) or similarity thresholds to optimize performance.

## Requirements

- Python 3.x
- `pandas`, `numpy`
- `scikit-learn`
- `matplotlib`
- `scipy`
- `re` (built-in)

## Results

The script prints evaluation metrics to the console and generates plots that illustrate how performance improves with more comparisons. Results may vary slightly with each run due to bootstrapping and random sampling.





# AMD_Project
Entity Resolution using Locality Sensitive Hashing (LSH)
This project detects and removes duplicate book reviews from the Amazon Books Review dataset (>3M records). It implements a scalable MinHash-LSH pipeline using PySpark to perform similarity searches efficiently without an O(N 
2
 ) bottleneck.

Theoretical Framework
Based on RU Chapter 3:

Shingling (RU 3.2): 5-shingles with integer hashing.

MinHashing (RU 3.3): Vectorized signature generation (100 permutations).

LSH (RU 3.4): Banding technique (b=20,r=5) for candidate selection.

Methodology
Ingestion: Loaded dataset via Kaggle API into Spark.

Preprocessing:

Decoded HTML entities (e.g., &quot; → ").

Removed punctuation/whitespace and filtered short texts (<15 chars).

Generated unique integer IDs for tracking.

Optimization: Replaced Python loops with NumPy vectorization, speeding up MinHashing by ~50x.

Results
Candidate Pairs: Reduced search space to ~6,773 potential duplicates (on subsample).

Verification: Confirmed 100% Jaccard Similarity on detected pairs.

Outcome: Successfully identified and removed 2,919 duplicate reviews.

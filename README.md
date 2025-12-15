# Finding Similar Items in Amazon Book Reviews
# Scalable Similarity Detection of Book Reviews

## Overview
This project detects duplicate and near-duplicate book reviews from a large dataset using scalable similarity techniques. Instead of performing exhaustive pairwise comparisons, it applies **MinHashing** and **Locality Sensitive Hashing (LSH)** to efficiently identify similar reviews.

## Methodology
- **Shingling:** Convert reviews into sets of shingles  
- **MinHashing:** Generate compact signatures using 100 hash functions  
- **LSH:** Efficiently generate candidate pairs (10 bands × 10 rows)  
- **Jaccard Similarity:** Verify similarity with a threshold of 0.55  
- **Deduplication:** Remove redundant reviews

---

## Results
- **Verified similar pairs:** 34,914  
- **Removed duplicates:** 24,663  
- **Dataset reduction:** ~8.2%

## Technologies
Python · NumPy · Apache Spark · Google Colab



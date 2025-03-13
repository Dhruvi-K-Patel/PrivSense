# QueryGuard: Protecting Privacy in AOL Web Search Data  

## Table of Contents  
1. [Project Overview](#project-overview)  
2. [Team Members](#team-members)  
3. [Application](#application)  
4. [Dataset](#dataset)  
5. [Privacy and Security Techniques](#privacy-and-security-techniques)  
6. [Implementation](#implementation)  
   - [K-Means Clustering](#k-means-clustering)  
   - [K-Anonymity](#k-anonymity)  
7. [Testing and Results](#testing-and-results)  
8. [Conclusion](#conclusion)  
9. [References](#references)  

---

## Project Overview  
QueryGuard is a privacy-enhancing system designed to protect user data in web search queries. It implements advanced clustering and anonymization techniques to ensure data privacy while maintaining usability for research and analysis. The project focuses on AOL web search data and aims to provide a balance between data security and utility.  

---

## Team Members  
- **Dhruvi Kaushikbhai Patel**  
- **Arpit Singhal**  
- **Prakhar Nag**  

Each member contributes expertise in computer science, data privacy, and security to ensure a robust and effective solution.  

---

## Application  
QueryGuard is useful in:  
- **Academic Research**: Enables researchers to analyze user search patterns while preserving privacy.  
- **Healthcare and Finance**: Protects sensitive data when analyzing user trends.  
- **Digital Marketing & E-commerce**: Allows businesses to gain insights while complying with privacy regulations.  

---

## Dataset  
- **Source**: AOL Web Query Data (2006)  
- **Size**: 20 million queries from 650,000 users over three months  
- **Fields**:  
  - AnonID (Anonymous User ID)  
  - Query (Search term)  
  - QueryTime (Timestamp)  
  - ItemRank (Rank of clicked item)  
  - ClickURL (Clicked result)  

---

## Privacy and Security Techniques  
QueryGuard employs **semantic similarity-based clustering (SSC)** and **K-anonymity** to anonymize query logs while preserving data usability.  

- **Semantic Similarity-Based Clustering**  
  - Uses **BERT embeddings** to measure similarity between queries.  
  - Groups queries into clusters using **K-Means clustering**.  

- **K-Anonymity**  
  - Ensures each query cluster is indistinguishable from at least **k-1 other clusters**.  
  - Uses **lossless generalization (LG)** and **information loss metrics** to evaluate anonymization effectiveness.  

---

## Implementation  

### K-Means Clustering  
1. **Setup and Installations**  
   - Install necessary libraries (`pandas`, `scikit-learn`, `torch`, `transformers`).  
2. **Data Preprocessing**  
   - Load dataset using `pandas`.  
   - Apply **BERT-based text vectorization** for embedding queries.  
3. **Clustering**  
   - Normalize embeddings and apply **K-Means clustering**.  
4. **Output Storage**  
   - Save clustered data to an **Excel file** for analysis.  

### K-Anonymity  
1. **Generalization of Query Time**  
   - Convert timestamps to **Year-Month format** to reduce precision.  
2. **Cluster Naming**  
   - Assign **semantic labels** to clusters.  
3. **K-Anonymity Application**  
   - Ensure each cluster has at least `k=5` similar records.  
4. **Utility Metrics**  
   - Compute **distortion (0.58)** and **precision (0.42)** to assess data retention.  

---

## Testing and Results  
- **Performance**: Achieves **0.85 similarity score** in clustering.  
- **Privacy Protection**: Effectively reduces re-identification risks.  
- **Scalability**: Supports large datasets with **minimal computational overhead**.  
- **User Feedback**: Highly rated for usability and privacy balance.  

---

## Conclusion  
QueryGuard successfully anonymizes web search data while maintaining analytical value. Future improvements could include **DBScan clustering** and **differential privacy** to further enhance security and utility.  

---

## References  
[1] Adar, E. "User 4XXXXX9: Anonymizing query logs," Proc. Query Log Analysis Workshop, 2007.  
[2] Aggarwal, G., et al. "Achieving anonymity via clustering," PODS, 2006.  
[3] Cao, J., et al. "𝜌-uncertainty: Inference-proof transaction anonymization," VLDB, 2010.  

---


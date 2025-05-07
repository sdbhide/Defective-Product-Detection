# Defective-Product-Detection
Defective Product Detection Using User Reviews from Amazon

In this project, we analyzed Amazon verified reviews to develop a system for detecting potentially defective products. We focused on two product categories — Musical Instruments and Appliances, which were selected for their higher likelihood of quality issues. By processing a large volume of review text with PySpark, we aimed to build a scalable and efficient workflow that could identify defective products early, helping both consumers and vendors improve product satisfaction and quality control.

Main Objectives: Our main objective was to create a scalable method to identify potentially defective products through textual review analysis. We focused on cleaning and preparing the data for analysis, developing a cosine similarity scoring approach to flag reviews indicating defects, and evaluating product-level patterns across two distinct product categories. Using Spark allowed us to efficiently manage large-scale processing and set a foundation for potential expansion to other categories.

Methodology and Key Findings:
Defect Centroid Creation: We generated a defect centroid by embedding a manually selected list of defect-related keywords and calculated cosine similarity between each review and this centroid.
Review Scoring and Labeling: Reviews with a cosine similarity score greater than 0.75 were labeled as indicating potential defects. This threshold effectively separated negative reviews associated with product issues from neutral or positive feedback.
Defect Rate Analysis by Product: Products were evaluated based on the proportion of defect-flagged reviews. Several products in both categories exhibited defect rates exceeding 10%, indicating potential quality concerns.
Category Differences: On average, products in the Appliances category showed a slightly higher median defect rate compared to those in Musical Instruments, suggesting category-specific differences in product reliability.
Model Performance: A Logistic Regression model trained on the defect-labeled data achieved an AUC of 0.69, demonstrating reasonable predictive ability in distinguishing defective products from non-defective ones based on review features.
Visualization Insights: Visualizations revealed that while most products have low defect rates, there is a long tail of products with significantly higher defect rates, emphasizing the importance of early detection mechanisms.


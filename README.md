**The Impact of Artificial Intelligence on the Banking Industry: Addressing Bias in Credit Approval Decisions**
My team and I have undertaken a comprehensive study to explore the impact of Artificial Intelligence (AI) on the banking industry's credit approval decisions. While transformative, the automation of loan approvals using machine learning models has raised significant concerns regarding data biases that may perpetuate societal discrimination and economic inequality.

**Unveiling the Bias**
The study used a dataset from Kaggle, encompassing key variables essential for predicting loan approval. By adopting a positivist philosophy and a quantitative approach, the research aimed to generate generalizable and replicable results. The dataset included over 614 records and was meticulously prepped and cleaned, focusing on attributes such as gender, marital status, income, and loan amount.

A critical finding emerged from the analysis: a significant negative correlation between gender and loan status. This correlation implied that gender unduly influenced the model's final output. Using SHapley Additive exPlanations (SHAP), We further confirmed that gender was the second most influential attribute in the model's decisions. These results underscore the necessity for business analytics managers to address biases in the data management process to ensure fairness.

**The Bigger Picture**
The broader implications of AI bias in the banking industry are profound. By examining the impact of these biases on businesses and customers, it became evident that biased AI models could lead to unfair lending practices, exacerbating socio-economic disparities. Historical data reveals that minority groups often face higher rejection rates and interest rates, despite having comparable or better financial standing than their counterparts.

Addressing these biases is crucial for maintaining the integrity and fairness of financial decision-making processes. Financial institutions must implement robust data auditing processes and utilize model-agnostic tools like SHAP to assess and adjust their AI algorithms continuously.

**Moving Forward**
The findings of this study provide a solid foundation for banks to refine their AI systems. Ensuring data preparation processes are free from biases and regularly auditing models can enhance the fairness of loan approval processes. This approach not only helps build trust with customers but also promotes a more equitable financial environment.

However, challenges remain. Privacy regulations make it difficult to gather real-world data, and different models may require different bias detection tools. Combining tools like SHAP with human expertise and domain knowledge is essential for a comprehensive understanding of bias in AI systems.

**Conclusion**
The integration of AI in banking is undoubtedly transformative, but it comes with the responsibility to ensure fairness and equity in its applications. This research highlights the importance of addressing biases in AI models to prevent the perpetuation of historical inequalities. By adopting proactive measures and continually refining AI systems, financial institutions can pave the way for a more inclusive and just financial landscape.

**Objectives**
•	To uncover and illustrate instances of bias within the data used to develop AI-driven loan eligibility criteria.  
•	To investigate how AI algorithm biases impact businesses and their customers.  
•	To offer actionable recommendations for banks to proactively address bias in AI systems within the competitive financial market. 

**Research questions**
•	What are the discernible instances of bias within the data used for forming AI-driven loan eligibility criteria?  
•	How does bias within AI algorithms affect businesses and their customer base?  
•	What actionable recommendations can be provided to banks for mitigating bias in AI systems within the competitive financial market? 


**Statistical Information**
The banking industry is in a much more robust stand compared to its state post the 2008 financial crisis. In 2022, the total worldwide assets increased to \$154,211, marking a 3.79% year-over-year growth from \$148,583 in 2021, as reported by The Banker's Top 1000 World Banks Ranking for 2022 (Meola).  Projections are that banks will be back to profitability sooner than expected, a short downtrend in 2023 (Deloitte):

![image](https://github.com/user-attachments/assets/9a0e8ac0-9a97-46ab-b132-c37678eca2ce)

**Analysis and Findings**
In this report, the data bias would be illustrated and analysed by using Loan_Train.csv. The dataset consists of several criteria with its loan approval status. In this case, the dataset would be altered by changing the loan status of data of male gender with approved status to either being approved and rejected randomly. These changes simulated bias intentionally by reducing the approval probability of male customers. But first, a quick look at its attributes: 

![image](https://github.com/user-attachments/assets/232ff557-2bd2-44c9-b767-3d21cd64a8f0)

Below is the code for altering the loan approval status:

![image](https://github.com/user-attachments/assets/ed0cbdf2-287e-453f-be3e-c915e799ec89)

The dataset then analysed the correlation of all variables with the loan status by using heatmap. It is visible that there is a significant negative correlation of gender with loan status after the alteration. 

![image](https://github.com/user-attachments/assets/7d1e05ff-02bd-4500-bfe4-993cffbe0ee8)

![image](https://github.com/user-attachments/assets/932b967e-610d-4e42-ad1d-8ecb2dd7593e)

In this scenario, the negative correlation indicates that there could be a tendency of negative impact on gender. The bias here was done to show that male customers could get rejected when they were supposed to be accepted originally following the original model or criteria. The illustration shows that reduce rate of approval could happen due to the bias training dataset and bias model. 
There are some model explain-ability methods that can be used to detect bias in simple way. One of the examples is SHapley Additive exPlanations (SHAP). SHAP provide a measurement of each input contribution towards final output.

![image](https://github.com/user-attachments/assets/f886effb-e045-4115-a01e-75da0d918b1f)

Syntax above shows how two more libraries are import in order to split the dataset and train the model so SHAP tool can weight the inputs contribution to the model. Model is not tested as its score is not relevant for this part of the analysis. 


![image](https://github.com/user-attachments/assets/7602d765-6011-4398-ab38-bea865e49f68)

The bar chart reveals that even though variables like credit history, loan amount and co-borrower income are important, gender plays a crucial role in the model output which denotes a rooted discriminatory factor within data with more importance it should when deciding credit worthiness. For more info on how SHAP works and different bias illustration technics with using it refer to Jan Bieser’s article on the matter.





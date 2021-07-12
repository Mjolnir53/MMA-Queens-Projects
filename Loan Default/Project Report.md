# Executive Summary :

Default risk is the risk that a lender takes on in the chance that a borrower will be unable to make the required payments on their debt obligation. Lenders and investors are exposed to default risk in virtually all forms of credit extensions.
In a typical bank, modelling default risk could include hundreds, even thousands of variables from micro and macro-economic factors to relevant details about the borrower. In recent years, three major factors contributed to a precise calculation of default risk: large volumes of data (internal, external, including social data), the introduction of GPU, a chipset specialized for A.I. and ML calculations that is three orders of magnitude faster than general-purpose CPU chipsets, and the extraordinary and rapid pace of innovation in software by the Open-Source community that made expensive propriety software redundant. These innovations have enabled small fintech start-ups to challenge and succeed in competing with banks and winning with relative ease. Ant Group is a shining FinTech example who created a credit risk model that uses 3,000 variables. The model enables Ant Group to create an automated systems that decide whether to grant loans within three minutes—a claim that may seem far-fetched but for Alibaba's proven ability to handle 544,000 orders per second. Ant is, in short, the world's purest example of the tremendous potential of digital finance.
The dataset had 24 features and 24,000 observations and using feature engineering techniques. From the initial dataset we created 28 new features generated before the modelling exercise started.

In this initiative, we built six models and used accuracy rate and the area under the receiver operating characteristic curve (AUC) as the evaluation indicators of the model.
We have summarized the evaluation parameters of these six models in the table below. Models No. 3,4,6 have a higher accuracy value, but the sensitivity is too low. CTREE has the highest accuracy with a similar sensitivity value comparing with the No. 1 and 5 models, with an AUC value identical to models 1 and 5. We, therefore, conclude that the CTREE model would provide us with the best results and we generated the final output file using CTREE.

# Exploratory Data Analysis

The dataset has 24,000 observations with 24 columns. By ignoring I.D. and predictor (default_0), we could utilize 23 features to build the model.
A preliminary business view of the features, we can categorize features into three distinct categories:
1. Individual (personal) features: These features provide metadata about a client like gender, age, marital status, and education. These features could provide relevant insight about a client's financial well-being. For instance, a 21-year-old may have a higher risk of defaulting on a loan than an older individual, or a highly educated individual has higher earning potential and, therefore, is less likely to default.
2. Bill & Payment: The dataset provides a 6-month aggregate that includes billed and paid amounts in dollars and a corresponding status for each month that records repayment status. The payment status is essential as it records values information like whether the bill was paid in full, paid the minimum amount, was there a delay in payment, and for how many months. There are 18 features related to the bill payment and status, one for each month.
3. Total Credit: The feature "LIMIT_BAL" shows the total amount of credit line that the client has with the bank. This limit includes all individual and family and supplementary credits.

Examine features from a data engineering perspective:
1. Missing data: There was no missing observed in the dataset.
2. Rare Category Analysis: Rare category analysis refers to the problem of representing, identifying, characterizing, and tracking rare examples from underrepresented minority classes in an imbalanced data set. This analysis is necessary to ensure rare values are appropriately grouped and will not affect model outcome and accuracy.















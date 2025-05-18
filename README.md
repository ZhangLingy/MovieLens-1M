# MovieLens-1M
Recommendation model based on intention decomposition and heterogeneous information fusion
Authors：Suqi Zhang and Xinxin Wang and Wenfeng Wang and Ningjing Zhang and Yunhao Fang and Jianxin Li
Abstract：In order to solve the problem of timeliness of user and item interaction intention and the noise caused by heterogeneous information fusion, a recommendation model based on intention decomposition and heterogeneous information fusion (IDHIF) is proposed. First, the intention of the recently interacting items and the users of the recently interacting candidate items is decomposed, and the short feature representation of users and items is mined through long-short term memory and attention mechanism. Then, based on the method of heterogeneous information fusion, the interactive features of users and items are mined on the user-item interaction graph, the social features of users are mined on the social graph, and the content features of the item are mined on the knowledge graph. Different feature vectors are projected into the same feature space through heterogeneous information fusion, and the long feature representation of users and items is obtained through splicing and multi-layer perceptron. The final representation of users and items is obtained by combining short feature representation and long feature representation. Compared with the baseline model, the AUC on the Last.FM and Movielens-1M datasets increased by 1.83 and 4.03 percentage points, respectively, the F1 increased by 1.28 and 1.58 percentage points, and the Recall@20 increased by 3.96 and 2.90 percentage points. The model proposed in this paper can better model the features of users and items, thus enriching the vector representation of users and items, and improving the recommendation efficiency.

After our processing, the Movielens-1M dataset consists of rating.txt, kg.txt, users.dat, and friends.txt.
1. rating.txt: The user's rating information on the movie is stored, and each record in the file is in the form of: user ID, project ID, and the user's rating of the movie
2. kg.txt: The knowledge graph of the project is stored, and each record in the file is in the form of: entity ID, relationship ID, and entity ID
3. users.dat: The relevant attribute information of the user is stored, and the form of each record in the file is: user ID, gender, age, and occupation
(1) Gender: M stands for male, F stands for female
(2) Age: Age is normalized: age divided by maximum age (56)
(3) Occupations: 21 types of occupations
0: "Other" or unspecified 1: "Academic/Educator" 2: "Artist"
3: "Clerical/Administrative" 4: "University/Graduate" 5: "Customer Service"
6: "Doctor/Health Care" 7: "Execution/Management" 8: "Farmer"
9: "Housewife" 10: "Student" 11: "Lawyer"
12: "Programmer" 13: "Retired" 14: "Sales/Marketing"
15: "Scientist" 16: "Self-employed" 17: "Technician/Engineer"
18: "Merchant / Artisan" 19: "Unemployed" 20: "Author"
4. friends.txt: The user's social information is stored, and each record in the file is in the form of: user ID and friend ID
Generating method: (1) The user is represented as a vector of 1 × 23 dimensions, representing the user's 23 attribute information, i.e., gender, age, and occupation
(2) Calculate the cosine similarity between the current user and the rest of the users
(3) Take the first K users with the highest similarity as the friends of the current users
(4) Build a user-friend binad

Cite
Suqi Zhang, Xinxin Wang, Wenfeng Wang, Ningjing Zhang, Yunhao Fang, Jianxin Li. Recommendation model based on intention decomposition and heterogeneous information fusion[J]. Mathematical Biosciences and Engineering, 2023, 20(9): 16401-16420. doi: 10.3934/mbe.2023732

@Article{
title = {Recommendation model based on intention decomposition and heterogeneous information fusion},
journal = {Mathematical Biosciences and Engineering},
volume = {20},
number = {9},
pages = {16401-16420},
year = {2023},
issn = {1551-0018},
doi = {10.3934/mbe.2023732},
url = {https://www.aimspress.com/article/doi/10.3934/mbe.2023732},
author = {Suqi Zhang and Xinxin Wang and Wenfeng Wang and Ningjing Zhang and Yunhao Fang and Jianxin Li},
keywords = {recommendation model, intention decomposition, heterogeneous information fusion, attention mechanism, graph neural networks},
}

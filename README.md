# sb-relax-challenge
18.2.3 - Relax Challenge

Identify which factors predict future user adoption.

# Notebooks For this Project

* [1-EDA.ipynb](1-EDA.ipynb) - exploratory data analysis
* [2-feature-engineering.ipynb](2-feature-engineering.ipynb) - feature engineering
* [3-modeling.ipynb](3-modeling.ipynb) - modeling and analysis

# Results

The model created achieved 91% accruacy in predicting user adoption

* User engagement within the first 30 days played the most significant factor in predicting user adtopion
* Days from account creation to first login also played a factor in predicting user adoption
    * If user does not log in with 14 days , user will very likely not adopt
    * Users that log in 2 to 3 days after account creation tends to adopt
    * Other first log in timeframes has little impact on user adoption
* Users created in months April and May are least likely to adopt while users created in February are most likely to adopt
* Users created in 2014 tended not to adopt
* Guest invites are most likely to adopt while Personal Projects are least likely to adopt



The following features had no impact to our model - after removing them from our dataset, the model accuracy score did not change significantly

* enabled_for_marketing_drip
* opted_in_to_mailing_list
* whether user was invited or not

* org_id also plays a factor in predicting adoption rate - however, when we removed this from our model, our accuracy improved from 86% to 91%. The dataset has over 400 orgs. I suspect that while certain org_id's are helpful in predicting user adotpions, most orgs do not contribution to predicting user adoption and introduced noise in our model
    * around half org_id have negative impact on user adoption while the other orgs have positive impact
    * Top 10 org with users most likely to adopt are:
        * 273, 306, 358, 403, 366, 395, 235, 266, 119, 218
    * Top 10 orgs with users least likely to adopt:
        * 386, 375, 151, 22, 312, 362, 279, 93, 146, 65


## Protocol for building our dataset

### 1. Identify the targeted users

Our first sampling stage is to recover a long list of French Reddit accounts. We scrap the r/france subreddit and gather name of all different accounts which posted anything on it. We do so using the `users_scraping` notebook. The list of scraped usernames is stored in `usernames.txt`.

Once we gather $100,000$ different names, we split this list in three parts. Indeed, since Reddit tries to prevent web-scraping, we seek to leverage our different IP adresses, so that each of us three will gather the sign-up date of one third of the usernames. To this end, we create three `covid_users_X.txt` file ($X \in \{1,2,3\}$) where each of us stores the usernames he found registered between March, 17th 2020 and September, 17th 2025 (six months following the begining of the first lockdown in metropolitan France). 

We will then compute how many accounts fit our restrictions (French, registered during a lockdown), and estimate how many additional accounts scraped from r/france are necessary to achieve our initial aim. We will downgrade our ambitions if needed. Our initial aim is $1000$ accounts (therefore, we assume $1\%$ of scraped usernames will fit our restrictions).
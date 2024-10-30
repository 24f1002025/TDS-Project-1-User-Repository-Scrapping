# GitHub User Analysis: Zurich Developers 🌍💻

- Data was scraped using Python's requests library to interact with GitHub's API, focusing on users in Zurich with over 50 followers and their repositories. 📊  
- The most surprising finding was the weak correlation (0.066) between the number of public repositories and followers, indicating quantity doesn't equate to popularity. ❗  
- Developers should consider using Python for projects, as it is the most popular language among Zurich developers, which could enhance visibility and collaboration opportunities. 🐍✨  

## Key Findings 🔑
1. **Top 5 users by followers:** IDouble, wcandillon, TheOfficialFloW, Seldaek, twpayne 👥  
2. **Most common programming languages:** Python, JavaScript, C++, Java, HTML 💻  
3. **Most popular company:** Google 🌐  
4. **User  with highest average stars per repo:** klaudiosinani (1012.43 stars) ⭐  
5. **Correlation between public repos and followers:** 0.07 📉  
6. **Each additional public repo is associated with:** 1.325 more followers on average 📈  
7. **Correlation between projects and wiki enabled:** 0.363 📚  
8. **Non-hireable users follow:** 888.086 more people on average than hireable users 👥🔍  
9. **Each additional word in a user's bio is associated with:** 39.404 more followers on average 📝  
10. **Top weekend repository creators:** kynan, yakky, devnoname120, Sadullah-TANRIKULU, JonnyBurger 📅  

## Methodology 🛠️
The data was collected using GitHub's API, focusing on users in Zurich with over 50 followers. We analyzed their profiles and repositories, cleaning and processing the data to extract meaningful insights. Statistical analysis was performed to identify trends and correlations within the developer community. 📊🔍  

## Data Scraping Methodology 🛠️

The data was scraped using Python's `requests` library to interact with the GitHub API, focusing specifically on users located in Zurich with over 50 followers. The following techniques were employed to ensure efficient and reliable data collection:

1. **API Token Authentication**: A personal GitHub token was used to authenticate requests, allowing for higher rate limits and access to user details. This is crucial for scraping large datasets without hitting API restrictions.

2. **Querying for Users**: Multiple queries were constructed to cover different variations of the location "Zurich" (including different spellings and formats). This approach maximized the number of unique users retrieved, ensuring a comprehensive dataset.

3. **Handling Pagination**: The script implemented pagination to retrieve up to 100 users per request. This was done in a loop that continued until no more users were found, allowing for thorough data collection.

4. **Unique User Tracking**: A set was used to track unique user logins, preventing duplicates from being added to the final list. This ensured that the dataset contained only distinct users, enhancing the quality of the analysis.

5. **Error Handling**: The script included robust error handling for network requests and unexpected exceptions. In case of an error, the script would wait and retry after a brief pause, minimizing data loss and ensuring continuity in data collection.

6. **Rate Limiting Compliance**: The script included sleep intervals between requests (`time.sleep(2)` and `time.sleep(1)`) to comply with GitHub's rate limits and avoid overwhelming the API, which can lead to temporary bans.

7. **Data Cleaning**: The company names were cleaned to remove any leading characters (like '@') and standardized to uppercase. This step improved consistency when analyzing company affiliations.

8. **CSV Output**: The final user data was written to a CSV file, making it easy to analyze and visualize later. This format allows for straightforward import into data analysis tools.

### Edge Cases Handled
- **Missing Data**: The script accounted for missing fields (like email or company) by using `get()` methods with default values, ensuring that the absence of data did not cause errors in processing.
- **Rate Limit Exceedance**: If the rate limit was exceeded, the script would automatically back off and retry after a longer wait, ensuring that scraping could continue without manual intervention.
- **Network Issues**: In case of network errors, the script would print an error message and wait before attempting to retry, which helps in maintaining the integrity of the data collection process.

By employing these techniques, the scraping process not only maximized data quality but also ensured reliability and efficiency, enabling a comprehensive analysis of the Zurich developer community on GitHub.

## Conclusions 📝
The analysis reveals interesting patterns in the Zurich developer community on GitHub. While the number of repositories doesn't strongly correlate with follower count, other factors like bio length and language choice seem to play a role in a developer's popularity. The prevalence of Python suggests a strong data science and web development community in Zurich. 🌟💡  

# Google-Trends-Real-Time-Stock-Data
The goal of this project was to find a correlation between the price of stocks and google trends. 

### How would I go about doing this?
I would need to figure out a way to programatically enter a stock's ticker symbol and search it on [Google Trends](https://trends.google.com/trends/) real-time. Then, I would need a way to extract and store the data. Lucky for me I used [pytrends](https://pypi.org/project/pytrends/) to make requests to google's servers to get my data. 

### What would I do with all this data?
I would compare the current real-time search trends of stocks to other stocks! I would find the outliers and display them on a table that is updated every few seconds.

### Why would the search results of a company influence its stock price?
I theorize if many people are researching about a company it is worth looking into. Maybe I could make a few trades myself (although I am not interested in that). I just want to maybe find a correlation between the search results (popularity) and a stock's intraday price.

# Problems:
- There are about 5000 companies I would like to constantly scan (search on google trends) real-time. Because of the mass amount of requests I used python [threading](https://docs.python.org/3/library/threading.html) to speed up this process. 
- Google doesn't like when people are bombarding their servers with mutliple requests. Especially when thousands of requests are coming from one person or internet address. So, my IP address would frequently become blocked, and I would not be able to make requests.

### Solution!
Rotate my IP address with [NordVPN](https://nordvpn.com/cybersecurity-site/), when needed. To do this in my program I used a module someone else created called [NordVPN Switcher](https://pypi.org/project/nordvpn-switcher/).

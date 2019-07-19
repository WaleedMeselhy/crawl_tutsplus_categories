# crawl tutsplus categories
* Using scrapy to crawl all articles of all categories in tutsplus
* Using UserAgentRotatorMiddleware to set user agent of request from random list of user agents to avoid getting banned
## sample output
```json
[
    {
        "title": "Options for SSL in WordPress",
        "url": "https://code.tutsplus.com/tutorials/options-for-ssl-in-wordpress--cms-21995",
        "category": ".htaccess",
        "user-agent": "agent_2"
    },
    {
        "title": "How to Use New Relic With PHP & WordPress",
        "url": "https://code.tutsplus.com/tutorials/how-to-use-new-relic-with-php-wordpress--cms-20465",
        "category": ".htaccess",
        "user-agent": "agent_2"
    }
]
```

## Run

```sh
$ cd crawl_tutsplus_categories
$ scrapy crawl tutsplus -o output.json
```

or run in docker container

```sh
$ docker build . -t tutsplus
$ docker run -it tutsplus 
```

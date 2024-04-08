# Training-WWW_Robots

The robots.txt file is used by web crawlers to check if they are allowed to crawl and index your website or only parts of it.

Sometimes these files reveal the directory structure instead protecting the content from being crawled.

Maybe this robots.txt will hidden something we are interesting in.

## Tip

Check (domain)/robots.txt

## Solution

1. In wechall site, the challenge url is "https://www.wechall.net/challenge/training/www/robots/index.php", then we just change to "https://www.wechall.net/robots.txt"

1. And we can see something in "Disallow", it seem like a path

1. copy that path and paste it, "https://www.wechall.net/[REPLACE]"

## References

* http://en.wikipedia.org/wiki/Robots_exclusion_standard

# Training-No DNS

Domain Name System (short for DNS), it will find out which IP is using this domain, and will return IP address for client.

Web browsers interact through Internet Protocol (IP) addresses. DNS translates domain names to IP addresses so browsers can load Internet resources.

## Tip

* modify dns record on local machine

* change header

## Solution

1. Because this challenge already say "NO DNS", so it definitely can not get web page.

1. I decide to look up this domain, in DNS look up online search is not any record. (I'm dumb)

1. Then I think it should be find out what ip address is this.

1. Think about a while, I think the challenge should be back to this web server so it can know that we are done the challenge.

1. Find out the IP of WeChall website (using DNS lookup tool, online tools)

1. Paste IP address on it => [IP]/.....

1. Then I got an error, it should using that domain to access it.

1. Modify windows local file (C:\Windows\System32\drivers\etc\hosts) and add this domain to WeChall's IP.

1. Go to that page with your own cookies (Because it will have some problem on that login page)

    ![F12 page](<Training-No DNS_F12_page.png>)

    I'm using chrome in this challenge, you can use other also well.

    F12 => Application => Cookies => [double click on space place] then add cookie name WC and paste your own value then refresh page

## References

* https://www.cloudflare.com/learning/dns/what-is-dns/

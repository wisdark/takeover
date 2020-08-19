# Takeover - Subdomain Takeover Finder v0.2

![screen](https://i.imgur.com/rggaoj8.png)
![screen2](https://raw.githubusercontent.com/m4ll0k/takeover/master/screen2.png)

Sub-domain takeover vulnerability occur when a sub-domain (**subdomain.example.com**) is pointing to a service (e.g: **GitHub**, **AWS/S3**,..) that has been removed or deleted. This allows an attacker to set up a page on the service that was being used and point their page to that sub-domain. For example, if **subdomain.example.com** was pointing to a GitHub page and the user decided to delete their GitHub page, an attacker can now create a GitHub page, add a **CNAME** file containing **subdomain.example.com**, and claim **subdomain.example.com**. For more information: [here](https://labs.detectify.com/2014/10/21/hostile-subdomain-takeover-using-herokugithubdesk-more/)

## Supported Services

```
'AWS/S3'
'BitBucket'
'CloudFront'
'Github'
'Shopify'
'Desk'
'Fastly'
'FeedPress'
'Ghost'
'Heroku'
'Pantheon'
'Tumbler'
'Wordpress'
'Desk'
'ZenDesk'
'TeamWork'
'Helpjuice'
'Helpscout'
'S3Bucket'
'Cargo'
'StatuPage'
'Uservoice'
'Surge'
'Intercom'
'Webflow'
'Kajabi'
'Thinkific'
'Tave'
'Wishpond'
'Aftership'
'Aha'
'Tictail'
'Brightcove'
'Bigcartel'
'ActiveCampaign'
'Campaignmonitor'
'Acquia'
'Proposify'
'Simplebooklet'
'GetResponse'
'Vend'
'Jetbrains'
'Unbounce'
'Smartling'
'Pingdom'
'Tilda'
'Surveygizmo'
'Mashery'
```

## Installation:

```shell
git clone https://github.com/m4ll0k/takeover.git
cd takeover
python3 setup.py install
```

**or:**

```
wget -q https://raw.githubusercontent.com/m4ll0k/takeover/master/takeover.py && python3 takeover.py
```

## Usage

```
$ python3 takeover.py -d www.domain.com -v 
$ python3 takeover.py -d www.domain.com -v -t 30
$ python3 takeover.py -d www.domain.com -p http://127.0.0.1:8080 -v 
$ python3 takeover.py -d www.domain.com -o <output.txt> or <output.json> -v 
$ python3 takeover.py -l uber-sub-domains.txt -o output.txt -p http://xxx.xxx.xxx.xxx:8080 -v 
$ python3 takeover.py -d uber-sub-domains.txt -o output.txt -T 3 -v 
```

## Docker support

Build the image:

```
docker build -t takeover .
```

Run the container:

```
docker run -it --rm takeover -d www.domain.com -v
```


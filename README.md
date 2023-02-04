<h1 align="center">

</h1>

<h4 align="center"> Most Advanced Open Source Intelligence (OSINT) Framework </h4>

<p align="center">
<a href="https://github.com/bhavsec/reconspider"><img src="https://img.shields.io/static/v1?label=version&message=1.0.7&color=blue"></a>
<a href="https://github.com/bhavsec/reconspider/issues?q=is:issue+is:closed"><img src="https://img.shields.io/github/issues-closed/bhavsec/reconspider?color=orange"></a>


</p>

# SPIDER

SPIDER is most Advanced Open Source Intelligence (OSINT) Framework for scanning IP Address, Emails, Websites, Organizations and find out information from different sources.

SPIDER can be used by Infosec Researchers, Penetration Testers, Bug Hunters and Cyber Crime Investigators to find deep information about their target.

SPIDER aggregate all the raw data, visualize it on a dashboard and facilitate alerting and monitoring on the data.

SPIDER also combines the capabilities of [Wave](https://github.com/adithyan-ak/WAVE), [Photon](https://github.com/s0md3v/Photon) and [Recon Dog](https://github.com/s0md3v/ReconDog) to do a comprehensive enumeration of attack surface.



Reconnaissance is a mission to obtain information by various detection methods, about the activities and resources of an enemy or potential enemy, or geographic characteristics of a particular area.


**Spider = Web crawler**

A Web crawler, sometimes called a spider or spiderbot and often shortened to crawler, is an Internet bot that systematically browses the World Wide Web, typically for the purpose of Web indexing (web spidering).

  



# Version (beta)

  	SPIDER  :     1.1.0


# Overview of the tool:

* Performs OSINT scan on a IP Address, Emails, Websites, Organizations and find out information from different sources.
* Correlates and collaborate the results, show them in a consolidated manner.
* Use specific script / launch automated OSINT for consolidated data.
* Currently available in only Command Line Interface (CLI).




# License Information
```
Spider and its documents are covered under GPL-3.0 (General Public License v3.0)
```



## spider Banner




 #####  ######  ### ######  ####### ######     
 #     # #     #  #  #     # #       #     #     
 #       #     #  #  #     # #       #     #       
  #####  ######   #  #     # #####   ######        
       # #        #  #     # #       #   #        
 #     # #        #  #     # #       #    #      
  #####  #       ### ######  ####### #     #      
                                                                                                       






ENTER 0 - 13 TO SELECT OPTIONS

1.  IP                           Enumerate  information  from  IP Address
2.  DOMAIN                       Gather  information  about  given DOMAIN
3.  PHONENUMBER                  Gather  information  about   Phonenumber
4.  DNS MAP                      Map DNS  records associated  with target
5.  METADATA                     Extract all metadata of  the  given file
6.  REVERSE IMAGE SEARCH         Obtain domain name or IP address mapping
7.  HONEYPOT                     Check if it's honeypot or a real  system
8.  MAC ADDRESS LOOKUP           Obtain information about give Macaddress
9.  IPHEATMAP                    Draw  out  heatmap  of  locations  of IP
10. TORRENT                      Gather torrent download  history  of  IP
11. USERNAME                     Extract Account info. from social  media
12. IP2PROXY                     Check whether  IP  uses  any VPN / PROXY
13. MAIL BREACH                  Checks given domain  has  breached  Mail
99. UPDATE                       Update ReconSpider to its latest version

0. EXIT                         Exit from  ReconSpider  to your terminal
```



# Documentation

Installing and using Spider is very easy. Installation process is very simple.

1. Downloading or cloning ReconSpider github repository.
2. Installing all dependencies.
3. Setting up the Database.

Let's Begin !!


### Setting up the environment

Step 1 - Cloning Spider on your linux system.

In order to download ReconSpider simply clone the github repository. Below is the command which you can use in order to clone ReconSpider repository.
```
git clone hhttps://github.com/kizwit/spider.git
```

Step 2 - Make sure python3 and python3-pip is installed on your system.

You can also perform a check by typing this command in your terminal.

```
sudo apt install python3 python3-pip
```

Step 3 - Installing all dependencies.

Once you clone and check python installation, you will find directory name as **reconspider**. Just go to that directory and install using these commands:
```
cd reconspider
sudo python3 setup.py install
```

Step 4 - Setting up the Database.

**IP2Proxy Database**

```
https://lite.ip2location.com/database/px8-ip-proxytype-country-region-city-isp-domain-usagetype-asn-lastseen
```
Download database, extract it and move to `reconspider/plugins/` directory.


# Updating API Keys

APIs included in ReconSpider are FREE and having limited & restricted usage per month, Please update the current APIs with New APIs in `setup.py` file, and re-install once done to reflect the changes.

> Warning: Not updating the APIs can result in not showing the expected output or it may show errors.

You need to create the account and get the API Keys from the following websites.

* Shodan.io - https://developer.shodan.io/api
* NumVerify - https://numverify.com/documentation
* IP Stack - https://ipstack.com/documentation
* Google Maps - https://developers.google.com/maps/documentation/places/web-service/get-api-key


# Usage


ReconSpider is very handy tool and easy to use. All you have to do is just have to pass values to parameter.
In order to start ReconSpider just type:
```
python3 spider.py
```

**1. IP**

This option gathers all the information of given IP Address from public resources.
```
Spider >> 1
IP >> 8.8.8.8
```

**2. DOMAIN**

This option gathers all the information of given URL Address and check for vulneribility.
```
spider >> 2
HOST (URL / IP) >> vulnweb.com
PORT >> 443
```

**3. PHONENUMBER**

This option allows you to gather information of given phonenumber.
```
spider >> 3
PHONE NUMBER (919485247632) >>
```

**4. DNS MAP**

This option allows you to map an organizations attack surface with a virtual DNS Map of the DNS records associated with the target organization.
```
Spider >> 4
DNS MAP (URL) >> vulnweb.com
```

**5. METADATA**

This option allows you to extract all metadat of the file such as date created, who created it, location, posible email of the creator and so on.
```
spider >> 5
Metadata (PATH) >> /root/Downloads/images.jpeg
```

**6. REVERSE IMAGE SEARCH**

This option allows you to obtain information and similar image that are available in internet.
```
spider >> 6
REVERSE IMAGE SEARCH (PATH) >> /root/Downloads/images.jpeg
Open Search Result in web broser? (Y/N) : y
```

**7. HONEYPOT**

This option allows you to identify honeypots! The probability that an IP is a honeypot is captured in a "Honeyscore" value that can range from 0.0 to 1.0
```
Spider >> 7
HONEYPOT (IP) >> 1.1.1.1
```

**8. MAC ADDRESS LOOKUP**

This option allows you to identify Mac address details who is manufacturer, address, country, etc.

```
spider >> 8
MAC ADDRESS LOOKUP (Eg:08:00:69:02:01:FC) >>
```

**9. IPHEATMAP**

This option provided you heatmap of the provided ip or single ip, if connect all the provided ip location with accurate Coordinator.
```
spider >> 9

    1) Trace single IP
    2) Trace multiple IPs
OPTIONS >>
```

**10. TORRENT**

This option allows you to gathers history of Torrent download history.
```
spider >> 10
IPADDRESS (Eg:192.168.1.1) >>
```

**11. USERNAME**

This option allows you to gathers account information of the provided username from social media like Instagram, Twitter, Facebook.
```
spider >> 11

1.Facebook
2.Twitter
3.Instagram

Username >>
```

**12. IP2PROXY**

This option allows you to identify whether IP address uses any kind of VPN / Proxy to hide his identify.
```
spider >> 12
IPADDRESS (Eg:192.168.1.1) >>
```

**13. MAIL BREACH**

This option allows you to identify all breached mail ID from given domain.
```
spider >> 13
DOMAIN (Eg:intercom.io) >>
```

**99. UPDATE**

This option allows you to check for updates. If a newer version will available, ReconSpider will download and merge the updates into the current directory without overwriting other files.
```
Spider >> 99
Checking for updates..
```

**0. EXIT**

This option allows you to exit from ReconSpider Framework to your current Operating System's terminal.
```
spider >> 0
Bye, See ya again..
```



# Contact Developer

Do you want to have a conversation in private?

    Twitter:            @kizwitofficial
    Facebook:           fb.com/chuckleskizwit
    Instagram:          instagram.com/kizwitofficial
    LinkedIn:           linkedin.com/in/
    Email:              kizwit1@gmail.com
  



# ReconSpider Full Wiki and How-to Guide

Please go through the [ReconSpider Wiki Guide](https://github.com/kizwit/wiki) for a detailed explanation of each and every option and feature.


# Frequent & Seamless Updates
ReconSpider is under development and updates for fixing bugs. optimizing performance & new features are being rolled. Custom error handling is also not implemented, and all the focus is to create required functionality.

https://manytools.org/hacker-tools/ascii-banner/

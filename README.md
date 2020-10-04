# About TorghostNG
**TorghostNG now supports Privoxy**

TorghostNG is a tool that make all your internet traffic anonymized through Tor network.

Rewritten from [TorGhost](https://github.com/SusmithKrishnan/torghost) with Python 3.

TorghostNG was tested on:
* Kali Linux
* Manjaro
* ...

# What's new in TorghostNG 1.7
* Fix updating 
* Fix "Checking Tor connection" loop (by installing `curl`)

# What's new in TorghostNG 1.6
* fIx SoMe BuGs
* Faster installation

# What is Privoxy?
> Privoxy is a non-caching web proxy with advanced filtering capabilities for enhancing privacy, modifying web page data and HTTP headers, controlling access, and removing ads and other obnoxious Internet junk. Privoxy has a flexible configuration and can be customized to suit individual needs and tastes. It has application for both stand-alone systems and multi-user networks.

You can find more about Privoxy at [Privoxy Home Page](https://privoxy.org).

> If you want to hide your IP address from most adversaries, you should consider chaining Privoxy with Tor. The configuration details can be found in [How do I use Privoxy together with Tor](https://wwwprivoxy.org/faq/misc.html#TOR) section just below.

From [Privoxy FAQ 4.7](https://privoxy.org/faq/misc.html).

# Before you use TorghostNG
* For the goodness of Tor network, BitTorrent traffic will be blocked by iptables. Although you can bypass it with some tweaks with your torrent client 😥. It's difficult to completely block all torrent traffic.
* For security reason, TorghostNG is gonna disable IPv6 to prevent IPv6 leaks (it happened to me lmao).

# Installing TorghostNG
TorghostNG currently supports:
* GNU/Linux distros that based on Arch Linux
* GNU/Linux distros that based on Debian/Ubuntu
* GNU/Linux distros that based on Fedora, CentOS, RHEL, openSUSE
* [Solus OS](https://getsol.us)
* [Void Linux](https://voidlinux.org)
* Anh the elder guy: [Slackware](http://slackware.com)
* (Too much package managers for one day :v)

To install TorghostNG, open your Terminal and enter these commands    
    
    git clone https://github.com/githacktools/TorghostNG
    cd TorghostNG
    sudo python3 install.py
    sudo torghostng
    
But with Slackware, you use `sudo python3 torghostng.py` to run TorghostNG :v

# Help
    OPTIONS:
      -h, --help      Show this help message and exit
      -s, --start     Start connecting to Tor
      -x, --stop      Stop connecting to Tor
      -r, --renew     Renew the current Tor circuit
      -id COUNTRY ID  Connect to Tor exit node of a specific country. Go to CountryCode.org to search country ID
      -mac INTERFACE  Randomly change MAC address. Use 'ifconfig' to show interface devices
      -c, --checkip   Check your current IPv4 address
      --dns           Use this to fix DNS when website address can't be resolved
      -l, --language  Change the display language. English is the default
      --list          Show the available languages list
      -u, --update    Check for update
      --nodelay       Disable delay time

You can combine multiple choices at the same time, such as:
* `torghostng -s -m INTERFACE`: Changing MAC address before connecting
* `torghostng -c -m INTERFACE`: Checking IP address and changing MAC address
* `torghostng -s -x`: Connecting to Tor anh then stop :v
* ...

If you have any questions, you can watch this [tutorial videos](https://bit.ly/34TNglL) 🙂

I hope you will love it 😃

# How to update TorghostNG
Open Terminal and type `torghostng -u` with sudo to update TorghostNG, but it will download new TorghostNG to `/root`, because you're running it as root. If you don't like that, you can type `git pull -f` and `sudo python3 install.py`.

# Notes before you use Tor
Tor can't help you completely anonymous, just almost:
* [Tor’s Biggest Threat – Correlation Attack](https://theonionweb.com/2016/10/25/tors-biggest-threat-correlation-attack)
* [Is Tor Broken? How the NSA Is Working to De-Anonymize You When Browsing the Deep Web](https://null-byte.wonderhowto.com/how-to/is-tor-broken-nsa-is-working-de-anonymize-you-when-browsing-deep-web-0148933)
* [Use Traffic Analysis to Defeat TOR](https://null-byte.wonderhowto.com/how-to/use-traffic-analysis-defeat-tor-0149100)
* ...

It's recommended that you should use [NoScript](https://noscript.net) before before surfing the web with Tor. NoScript shall block JavaScript/Java/Flash scripts on websites to make sure they won't reveal your real identify.

# And please
* **Don't spam or perform DoS attacks with Tor.** It's not effective, you will only make Tor get hated and waste Tor's money.
* **Don't torrent over Tor.** If you want to keep anonymous while torrenting, use a no-logs VPN please.

[Bittorrent over Tor isn't a good idea](https://blog.torproject.org/bittorrent-over-tor-isnt-good-idea)

[Not anonymous: attack reveals BitTorrent users on Tor network](https://arstechnica.com/tech-policy/2011/04/not-anonymous-attack-reveals-bittorrent-users-on-tor-network)

![Don't torrent over Tor, please](https://github.com/GitHackTools/Store-the-pictures/raw/master/Don't%20torrent%20over%20Tor.png)

# Changes log
Version 1.7
* Fix updating error
* Fix "Checking Tor connection" loop (by installing `curl`)

Version 1.6
* Fix some bugs
* Faster Installation

Version 1.5
* Fix bugs of version 1.4

Version 1.4
* Support connecting to Tor with Privoxy

You can read how to use Privoxy together with Tor at [Privoxy FAQ](https://privoxy.org/faq/misc.html#TOR)

Version 1.2
* Fix `update_commands` and others in [torghostng.py](https://github.com/gitkern3l/TorghostNG/blob/master/torghostng.py)
* Chang a few things in [`theme.py`](https://github.com/gitkern3l/TorghostNG/blob/master/torngconf/theme.py)
* Chang a few things in [`install.py`](https://github.com/gitkern3l/TorghostNG/blob/master/install.py)
* Now you can change Tor circuit with `-r`

Version 1.1
* Check your IPv6
* Change all "TOR" to "Tor"
* Block BitTorrent traffic
* Auto disable IPv6 before connecting to Tor

# Screenshots of Torghost (Version 1.0, 1.5 and 1.7)
* TorghostNG's Installtion
![TorghostNG's Installtion](https://github.com/GitHackTools/Store-the-pictures/blob/master/TorghostNG%201.7%20installation.png)
* Connecting to Tor with Privoxy

![Connecting to Tor with Privoxy - TorghostNG](https://github.com/GitHackTools/Store-the-pictures/raw/master/Connecting%20to%20Tor%20with%20Privoxy%20-%20TorghostNG.png)

* Connecting to TOR exitnode in US with Privoxy

![Connecting to TOR exitnode in US with Privoxy](https://github.com/GitHackTools/Store-the-pictures/blob/master/TorghostNG%20connecting%20to%20TOR%20exitnode%20in%20US%20with%20Privoxy.png)

* Checking Tor Privoxy connection

![Checking Tor Privoxy connection](https://github.com/GitHackTools/Store-the-pictures/blob/master/TorghostNG%20checking%20Tor%20Privoxy%20connection.png)

* Disconnecting from Tor and Privoxy

![Disconnecting from Tor and Privoxy](https://github.com/GitHackTools/Store-the-pictures/blob/master/TorghostNG%20disconnecting%20from%20Tor%20and%20Privoxy.png)

* Changing MAC address: `torghostng -m INTERFACE`

![Changing MAC address with TorghostNG](https://github.com/GitHackTools/Store-the-pictures/raw/master/TorghostNG%20changing%20MAC%20address.png)

* Checking IP address: `torghostng -c`

![Checking IP address with TorghostNG](https://github.com/GitHackTools/Store-the-pictures/raw/master/TorghostNG%20checking%20IP%20address.png)

* Disconnecting from Tor: `torghostng -x`

![Disconnecting from Tor network with TorghostNG](https://github.com/GitHackTools/Store-the-pictures/raw/master/TorghostNG%20disconnecting%20from%20TOR.png)

* Connecting to Tor exitnode in a specific country: `torghostng -id COUNTRY ID`

![Connecting to TOR exitnode in a specific country](https://github.com/GitHackTools/Store-the-pictures/raw/master/TorghostNG%20connecting%20to%20TOR%20exitnode%20in%20US.png)

* Uninstalling TorghostNG: `python3 install.py`

![Uninstalling TorghostNG](https://github.com/GitHackTools/Store-the-pictures/raw/master/Uninstalling%20TorghostNG.png)

# Contact to the coder
* Twitter: [@SecureGF](https://twitter.com/securegf)
* Github: here 😃
* Website: [Blogspot](https://githacktools.blogspot.com)

# To-do lists
* Block torrent, for you - Tor network
* IPv6 (maybe?)
* GUI version
* Fix bug, improve TorghostNG (always)

# And finally
You can help me by telling me if you find any bugs or issues. Thank you for using my tool 😊


# iseecars scrapper

[![Python](https://img.shields.io/badge/Python-3.6%2B-red.svg)](https://www.python.org/downloads/)

Web scrapping tool for retrieving vehicle information from [iseecars.com](iseecars.com)

# Installation

Before you install ensure that `geckodriver` for Firefox is installed.

 - Download [geckodriver](https://github.com/mozilla/geckodriver)
	 -  ```wget https://github.com/mozilla/geckodriver/releases/download/v0.24.0/geckodriver-v0.24.0-linux64.tar.gz```
- Extract: ```tar -xvzf geckodriver-v0.24.0-linux64.tar.gz```
-  `sudo cp geckodriver /usr/local/bin`

To install Vehicle History Reports, run this command in your bash terminal:

```python
    sudo pip install -Ur requirements.txt
```

# Usage

```bash
usage: iseecars_scrapper.py [-h] --vin VIN [--proxy-host PROXY_HOST] [--proxy-port PROXY_PORT] [--proxy-username PROXY_USERNAME] [--proxy-password PROXY_PASSWORD] --username USERNAME
                            --password PASSWORD [--to-json] [--headless]

Web scrapping tool for Vehicle information from URL: https://www.vehiclehistory.com

optional arguments:
  -h, --help            show this help message and exit
  --vin VIN             VIN number.
  --proxy-host PROXY_HOST
                        Proxy address. [Optional]
  --proxy-port PROXY_PORT
                        Proxy port. [Optional]
  --proxy-username PROXY_USERNAME
                        Username to access proxy. [Optional]
  --proxy-password PROXY_PASSWORD
                        Password to access proxy. [Optional]
  --username USERNAME   Username for iseecars.com
  --password PASSWORD   Password for iseecars.com
  --to-json             Save webpage content to json
  --headless            Open browser [Debugging mode].
```

Example:

**No Proxy**
```
python iseecars_scrapper.py \
--vin WBAFR7C57CC811956 \
--username support@vehiclehistory.report \
--password fak86iak \
--to-json
```

**Through Proxy**
```
python iseecars_scrapper.py \
--vin WBAFR7C57CC811956 \
--username support@vehiclehistory.report \
--password fak86iak \
--proxy-host 5.181.41.31 \
--proxy-port 12333 \
--proxy-username netkingz9 \
--proxy-password test123465 \
--to-json
```

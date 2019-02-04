# MISP modules

[![Build Status](https://travis-ci.org/MISP/misp-modules.svg?branch=master)](https://travis-ci.org/MISP/misp-modules)
[![Coverage Status](https://coveralls.io/repos/github/MISP/misp-modules/badge.svg?branch=master)](https://coveralls.io/github/MISP/misp-modules?branch=master)
[![codecov](https://codecov.io/gh/MISP/misp-modules/branch/master/graph/badge.svg)](https://codecov.io/gh/MISP/misp-modules)

MISP modules are autonomous modules that can be used for expansion and other services in [MISP](https://github.com/MISP/MISP).

The modules are written in Python 3 following a simple API interface. The objective is to ease the extensions of MISP functionalities
without modifying core components. The API is available via a simple REST API which is independent from MISP installation or configuration.

MISP modules support is included in MISP starting from version 2.4.28.

For more information: [Extending MISP with Python modules](https://www.circl.lu/assets/files/misp-training/switch2016/2-misp-modules.pdf) slides from MISP training.

## Existing MISP modules

### Expansion modules

* [BGP Ranking](misp_modules/modules/expansion/bgpranking.py) - a hover and expansion module to expand an AS number with the ASN description, its history, and position in BGP Ranking.
* [BTC transactions](misp_modules/modules/expansion/btc_steroids.py) - An expansion hover module to get a blockchain balance and the transactions from a BTC address in MISP.
* [CIRCL Passive DNS](misp_modules/modules/expansion/circl_passivedns.py) - a hover and expansion module to expand hostname and IP addresses with passive DNS information.
* [CIRCL Passive SSL](misp_modules/modules/expansion/circl_passivessl.py) - a hover and expansion module to expand IP addresses with the X.509 certificate seen.
* [countrycode](misp_modules/modules/expansion/countrycode.py) - a hover module to tell you what country a URL belongs to.
* [CrowdStrike Falcon](misp_modules/modules/expansion/crowdstrike_falcon.py) - an expansion module to expand using CrowdStrike Falcon Intel Indicator API.
* [CVE](misp_modules/modules/expansion/cve.py) - a hover module to give more information about a vulnerability (CVE).
* [DBL Spamhaus](misp_modules/modules/expansion/dbl_spamhaus.py) - a hover module to check Spamhaus DBL for a domain name.
* [DNS](misp_modules/modules/expansion/dns.py) - a simple module to resolve MISP attributes like hostname and domain to expand IP addresses attributes.
* [DomainTools](misp_modules/modules/expansion/domaintools.py) - a hover and expansion module to get information from [DomainTools](http://www.domaintools.com/) whois.
* [EUPI](misp_modules/modules/expansion/eupi.py) - a hover and expansion module to get information about an URL from the [Phishing Initiative project](https://phishing-initiative.eu/?lang=en).
* [Farsight DNSDB Passive DNS](misp_modules/modules/expansion/farsight_passivedns.py) - a hover and expansion module to expand hostname and IP addresses with passive DNS information.
* [GeoIP](misp_modules/modules/expansion/geoip_country.py) - a hover and expansion module to get GeoIP information from geolite/maxmind.
* [hashdd](misp_modules/modules/expansion/hashdd.py) - a hover module to check file hashes against [hashdd.com](http://www.hashdd.com) including NSLR dataset.
* [intel471](misp_modules/modules/expansion/intel471.py) - an expansion module to get info from [Intel471](https://intel471.com).
* [IPASN](misp_modules/modules/expansion/ipasn.py) - a hover and expansion to get the BGP ASN of an IP address.
* [iprep](misp_modules/modules/expansion/iprep.py) - an expansion module to get IP reputation from packetmail.net.
* [macaddress.io](misp_modules/modules/expansion/macaddress_io.py) - a hover module to retrieve vendor details and other information regarding a given MAC address or an OUI from [MAC address Vendor Lookup](https://macaddress.io). See [integration tutorial here](https://macaddress.io/integrations/MISP-module).
* [onyphe](misp_modules/modules/expansion/onyphe.py) - a modules to process queries on Onyphe.
* [onyphe_full](misp_modules/modules/expansion/onyphe_full.py) - a modules to process full queries on Onyphe.
* [OTX](misp_modules/modules/expansion/otx.py) - an expansion module for [OTX](https://otx.alienvault.com/).
* [passivetotal](misp_modules/modules/expansion/passivetotal.py) - a [passivetotal](https://www.passivetotal.org/) module that queries a number of different PassiveTotal datasets.
* [rbl](misp_modules/modules/expansion/rbl.py) - a module to get RBL (Real-Time Blackhost List) values from an attribute.
* [reversedns](misp_modules/modules/expansion/reversedns.py) - Simple Reverse DNS expansion service to resolve reverse DNS from MISP attributes.
* [securitytrails](misp_modules/modules/expansion/securitytrails.py) - an expansion module for [securitytrails](https://securitytrails.com/).
* [shodan](misp_modules/modules/expansion/shodan.py) - a minimal [shodan](https://www.shodan.io/) expansion module.
* [Sigma queries](misp_modules/modules/expansion/sigma_queries.py) - Experimental expansion module querying a sigma rule to convert it into all the available SIEM signatures.
* [Sigma syntax validator](misp_modules/modules/expansion/sigma_syntax_validator.py) - Sigma syntax validator.
* [sourcecache](misp_modules/modules/expansion/sourcecache.py) - a module to cache a specific link from a MISP instance.
* [STIX2 pattern syntax validator](misp_modules/modules/expansion/stix2_pattern_syntax_validator.py) - a module to check a STIX2 pattern syntax.
* [ThreatCrowd](misp_modules/modules/expansion/threatcrowd.py) - an expansion module for [ThreatCrowd](https://www.threatcrowd.org/).
* [threatminer](misp_modules/modules/expansion/threatminer.py) - an expansion module to expand from [ThreatMiner](https://www.threatminer.org/).
* [urlscan](misp_modules/modules/expansion/urlscan.py) - an expansion module to query [urlscan.io](https://urlscan.io).
* [virustotal](misp_modules/modules/expansion/virustotal.py) - an expansion module to pull known resolutions and malware samples related with an IP/Domain from virusTotal (this modules require a VirusTotal private API key)
* [VMray](misp_modules/modules/expansion/vmray_submit.py) - a module to submit a sample to VMray.
* [VulnDB](misp_modules/modules/expansion/vulndb.py) - a module to query [VulnDB](https://www.riskbasedsecurity.com/).
* [Vulners](misp_modules/modules/expansion/vulners.py) - an expansion module to expand information about CVEs using Vulners API.
* [whois](misp_modules/modules/expansion) - a module to query a local instance of [uwhois](https://github.com/rafiot/uwhoisd).
* [wikidata](misp_modules/modules/expansion/wiki.py) - a [wikidata](https://www.wikidata.org) expansion module.
* [xforce](misp_modules/modules/expansion/xforceexchange.py) - an IBM X-Force Exchange expansion module.
* [YARA query](misp_modules/modules/expansion/yara_query.py) - a module to create YARA rules from single hash attributes.
* [YARA syntax validator](misp_modules/modules/expansion/yara_syntax_validator.py) - YARA syntax validator.

### Export modules

* [CEF](misp_modules/modules/export_mod/cef_export.py) module to export Common Event Format (CEF).
* [GoAML export](misp_modules/modules/export_mod/goamlexport.py) module to export in [GoAML format](http://goaml.unodc.org/goaml/en/index.html).
* [Lite Export](misp_modules/modules/export_mod/liteexport.py) module to export a lite event.
* [Simple PDF export](misp_modules/modules/export_mod/pdfexport.py) module to export in PDF (required: asciidoctor-pdf).
* [Nexthink query format](misp_modules/modules/export_mod/nexthinkexport.py) module to export in Nexthink query format.
* [osquery](misp_modules/modules/export_mod/osqueryexport.py) module to export in [osquery](https://osquery.io/) query format.
* [ThreatConnect](misp_modules/modules/export_mod/threat_connect_export.py) module to export in ThreatConnect CSV format.
* [ThreatStream](misp_modules/modules/export_mod/threatStream_misp_export.py) module to export in ThreatStream format.

### Import modules

* [CSV import](misp_modules/modules/import_mod/csvimport.py) Customizable CSV import module.
* [Cuckoo JSON](misp_modules/modules/import_mod/cuckooimport.py) Cuckoo JSON import.
* [Email Import](misp_modules/modules/import_mod/email_import.py) Email import module for MISP to import basic metadata.
* [GoAML import](misp_modules/modules/import_mod/) Module to import [GoAML](http://goaml.unodc.org/goaml/en/index.html) XML format.
* [OCR](misp_modules/modules/import_mod/ocr.py) Optical Character Recognition (OCR) module for MISP to import attributes from images, scan or faxes.
* [OpenIOC](misp_modules/modules/import_mod/openiocimport.py) OpenIOC import based on PyMISP library.
* [ThreatAnalyzer](misp_modules/modules/import_mod/threatanalyzer_import.py) - An import module to process ThreatAnalyzer archive.zip/analysis.json sandbox exports.
* [VMRay](misp_modules/modules/import_mod/vmray_import.py) - An import module to process VMRay export.

## How to install and start MISP modules in a Python virtualenv?

**Warning:** 
The pip3 package url-normalize==1.4.1 isn't available in debian-stretch.

~~~~bash
sudo apt-get install python3-dev python3-pip libpq5 libjpeg-dev tesseract-ocr imagemagick
sudo -u www-data virtualenv -p python3 /var/www/MISP/venv
cd /usr/local/src/
sudo git clone https://github.com/MISP/misp-modules.git
cd misp-modules
sudo -u www-data /var/www/MISP/venv/bin/pip install -I -r REQUIREMENTS
sudo -u www-data /var/www/MISP/venv/bin/pip install .
sudo apt install ruby-pygments.rb -y
sudo gem install asciidoctor-pdf --pre
sudo sed -i -e '$i \sudo -u www-data /var/www/MISP/venv/bin/misp-modules -l 127.0.0.1 -s > /tmp/misp-modules_rc.local.log &\n' /etc/rc.local
/var/www/MISP/venv/bin/misp-modules -l 127.0.0.1 -s & #to start the modules
~~~~

## How to install and start MISP modules?

**Warning:** 
The pip3 package url-normalize==1.4.1 isn't available in debian-stretch.


~~~~bash
sudo apt-get install python3-dev python3-pip libpq5 libjpeg-dev tesseract-ocr imagemagick
cd /usr/local/src/
sudo git clone https://github.com/MISP/misp-modules.git
cd misp-modules
sudo pip3 install -I -r REQUIREMENTS
sudo pip3 install -I .
sudo apt install ruby-pygments.rb -y
sudo gem install asciidoctor-pdf --pre
sudo sed -i -e '$i \sudo -u www-data /var/www/MISP/venv/bin/misp-modules -l 127.0.0.1 -s > /tmp/misp-modules_rc.local.log &\n' /etc/rc.local
/var/www/MISP/venv/bin/misp-modules -l 127.0.0.1 -s & #to start the modules
~~~~

## How to install and start MISP modules on Alpine Linux (For example: docker)

~~~~bash
apk --no-cache add \
        sudo \
        git \
        g++ \
        python3-dev \
        libjpeg-turbo-dev \
        tesseract-ocr \
        imagemagick \
        ruby-pygments \
        libpq \
        linux-headers \
        zlib-dev \
        curl \
        ;

git clone https://github.com/MISP/misp-modules.git /usr/local/src/misp-modules \
     ;cd /usr/local/src/misp-modules \
     ;sudo pip3 install -I -r REQUIREMENTS --no-cache-dir \
     ;sudo pip3 install -I . --no-cache-dir \
     ;gem install asciidoctor-pdf --pre \
     ;
~~~~
If you reuire an finished docker container for misp-modules you can use:
* hub.docker.com: dcso/misp-dockerized-misp-modules:2
* sources (version 2.x): https://github.com/DCSO/MISP-dockerized-misp-modules/

## How to add your own MISP modules?

Create your module in [misp_modules/modules/expansion/](misp_modules/modules/expansion/), [misp_modules/modules/export_mod/](misp_modules/modules/export_mod/), or [misp_modules/modules/import_mod/](misp_modules/modules/import_mod/). The module should have at minimum three functions:

* **introspection** function that returns a dict of the supported attributes (input and output) by your expansion module.
* **handler** function which accepts a JSON document to expand the values and return a dictionary of the expanded values.
* **version** function that returns a dict with the version and the associated meta-data including potential configurations required of the module.

Don't forget to return an error key and value if an error is raised to propagate it to the MISP user-interface.

Your module's script name should also be added in the `__all__` list of `<module type folder>/__init__.py` in order for it to be loaded.

~~~python
...
    # Checking for required value
    if not request.get('ip-src'):
        # Return an error message
        return {'error': "A source IP is required"}
...
~~~


### introspection

The function that returns a dict of the supported attributes (input and output) by your expansion module.

~~~python
mispattributes = {'input': ['link', 'url'],
                  'output': ['attachment', 'malware-sample']}

def introspection():
    return mispattributes
~~~

### version

The function that returns a dict with the version and the associated meta-data including potential configurations required of the module.


### Additional Configuration Values

If your module requires additional configuration (to be exposed via the MISP user-interface), you can define those in the moduleconfig value returned by the version function.

~~~python
# config fields that your code expects from the site admin
moduleconfig = ["apikey", "event_limit"]

def version():
    moduleinfo['config'] = moduleconfig
    return moduleinfo
~~~


When you do this a config array is added to the meta-data output containing all the potential configuration values:

~~~
"meta": {
      "description": "PassiveTotal expansion service to expand values with multiple Passive DNS sources",
      "config": [
        "username",
        "password"
      ],
      "module-type": [
        "expansion",
        "hover"
      ],

...
~~~


If you want to use the configuration values set in the web interface they are stored in the key `config` in the JSON object passed to the handler.

~~~
def handler(q=False):

    # Check if we were given a configuration
    config = q.get("config", {})

    # Find out if there is a username field
    username = config.get("username", None)
~~~


### handler

The function which accepts a JSON document to expand the values and return a dictionary of the expanded values.

~~~python
def handler(q=False):
    "Fully functional rot-13 encoder"
    if q is False:
        return False
    request = json.loads(q)
    src = request.get('ip-src')
    if src is None:
        # Return an error message
        return {'error': "A source IP is required"}
    else:
        return {'results':
                codecs.encode(src, "rot-13")}
~~~

#### export module

For an export module, the `request["data"]` object corresponds to a list of events (dictionaries) to handle.

Iterating over events attributes is performed using their `Attribute` key.

~~~python
...
for event in request["data"]:
        for attribute in event["Attribute"]:
          # do stuff w/ attribute['type'], attribute['value'], ...
...

### Returning Binary Data

If you want to return a file or other data you need to add a data attribute.

~~~python
{"results": {"values": "filename.txt",
             "types": "attachment",
             "data"  : base64.b64encode(<ByteIO>)  # base64 encode your data first
             "comment": "This is an attachment"}}
~~~

If the binary file is malware you can use 'malware-sample' as the type. If you do this the malware sample will be automatically zipped and password protected ('infected') after being uploaded.


~~~python
{"results": {"values": "filename.txt",
             "types": "malware-sample",
             "data"  : base64.b64encode(<ByteIO>)  # base64 encode your data first
             "comment": "This is an attachment"}}
~~~

[To learn more about how data attributes are processed you can read the processing code here.](https://github.com/MISP/PyMISP/blob/4f230c9299ad9d2d1c851148c629b61a94f3f117/pymisp/mispevent.py#L185-L200)


### Module type

A MISP module can be of four types:

- **expansion** - service related to an attribute that can be used to extend and update an existing event.
- **hover** - service related to an attribute to provide additional information to the users without updating the event.
- **import** - service related to importing and parsing an external object that can be used to extend an existing event.
- **export** - service related to exporting an object, event, or data.

module-type is an array where the list of supported types can be added.

## Testing your modules?

MISP uses the **modules** function to discover the available MISP modules and their supported MISP attributes:

~~~
% curl -s http://127.0.0.1:6666/modules | jq .
[
  {
    "name": "passivetotal",
    "type": "expansion",
    "mispattributes": {
      "input": [
        "hostname",
        "domain",
        "ip-src",
        "ip-dst"
      ],
      "output": [
        "ip-src",
        "ip-dst",
        "hostname",
        "domain"
      ]
    },
    "meta": {
      "description": "PassiveTotal expansion service to expand values with multiple Passive DNS sources",
      "config": [
        "username",
        "password"
      ],
      "author": "Alexandre Dulaunoy",
      "version": "0.1"
    }
  },
  {
    "name": "sourcecache",
    "type": "expansion",
    "mispattributes": {
      "input": [
        "link"
      ],
      "output": [
        "link"
      ]
    },
    "meta": {
      "description": "Module to cache web pages of analysis reports, OSINT sources. The module returns a link of the cached page.",
      "author": "Alexandre Dulaunoy",
      "version": "0.1"
    }
  },
  {
    "name": "dns",
    "type": "expansion",
    "mispattributes": {
      "input": [
        "hostname",
        "domain"
      ],
      "output": [
        "ip-src",
        "ip-dst"
      ]
    },
    "meta": {
      "description": "Simple DNS expansion service to resolve IP address from MISP attributes",
      "author": "Alexandre Dulaunoy",
      "version": "0.1"
    }
  }
]

~~~

The MISP module service returns the available modules in a JSON array containing each module name along with their supported input attributes.

Based on this information, a query can be built in a JSON format and saved as body.json:

~~~json
{
  "hostname": "www.foo.be",
  "module": "dns"
}
~~~

Then you can POST this JSON format query towards the MISP object server:

~~~bash
curl -s http://127.0.0.1:6666/query -H "Content-Type: application/json" --data @body.json -X POST
~~~

The module should output the following JSON:

~~~json
{
  "results": [
    {
      "types": [
        "ip-src",
        "ip-dst"
      ],
      "values": [
        "188.65.217.78"
      ]
    }
  ]
}
~~~

It is also possible to restrict the category options of the resolved attributes by passing a list of categories along (optional):

~~~json
{
  "results": [
    {
      "types": [
        "ip-src",
        "ip-dst"
      ],
      "values": [
        "188.65.217.78"
      ],
      "categories": [
        "Network activity",
        "Payload delivery"
      ]
    }
  ]
}
~~~

For both the type and the category lists, the first item in the list will be the default setting on the interface.

### Enable your module in the web interface

For a module to be activated in the MISP web interface it must be enabled in the "Plugin Settings.

Go to "Administration > Server Settings" in the top menu
- Go to "Plugin Settings" in the top "tab menu bar"
- Click on the name of the type of module you have created to expand the list of plugins to show your module.
- Find the name of your plugin's "enabled" value in the Setting Column.
"Plugin.[MODULE NAME]_enabled"
- Double click on its "Value" column

~~~
Priority        Setting                         Value   Description                             Error Message
Recommended     Plugin.Import_ocr_enabled       false   Enable or disable the ocr module.       Value not set.
~~~

- Use the drop-down to set the enabled value to 'true'

~~~
Priority        Setting                         Value   Description                             Error Message
Recommended     Plugin.Import_ocr_enabled       true   Enable or disable the ocr module.       Value not set.
~~~

### Set any other required settings for your module

In this same menu set any other plugin settings that are required for testing.

## Install misp-module on an offline instance.
First, you need to grab all necessary packages for example like this :

Use pip wheel to create an archive
~~~
mkdir misp-modules-offline
pip3 wheel -r REQUIREMENTS shodan --wheel-dir=./misp-modules-offline
tar -cjvf misp-module-bundeled.tar.bz2 ./misp-modules-offline/*
~~~
On offline machine :
~~~
mkdir misp-modules-bundle
tar xvf misp-module-bundeled.tar.bz2 -C misp-modules-bundle
cd misp-modules-bundle
ls -1|while read line; do sudo pip3 install --force-reinstall --ignore-installed --upgrade --no-index --no-deps ${line};done
~~~
Next you can follow standard install procedure.

## How to contribute your own module?

Fork the project, add your module, test it and make a pull-request. Modules can be also private as you can add a module in your own MISP installation.


## Tips for developers creating modules

Download a pre-built virtual image from the [MISP training materials](https://www.circl.lu/services/misp-training-materials/).

- Create a Host-Only adapter in VirtualBox
- Set your Misp OVA to that Host-Only adapter
- Start the virtual machine
- Get the IP address of the virutal machine
- SSH into the machine (Login info on training page)
- Go into the misp-modules directory

~~~bash
cd /usr/local/src/misp-modules
~~~

Set the git repo to your fork and checkout your development branch. If you SSH'ed in as the misp user you will have to use sudo.

~~~bash
sudo git remote set-url origin https://github.com/YourRepo/misp-modules.git
sudo git pull
sudo git checkout MyModBranch
~~~

Remove the contents of the build directory and re-install misp-modules.

~~~python
sudo rm -fr build/*
sudo pip3 install --upgrade .
~~~

SSH in with a different terminal and run `misp-modules` with debugging enabled.

~~~python
sudo killall misp-modules
misp-modules -d
~~~


In your original terminal you can now run your tests manually and see any errors that arrive

~~~bash
cd tests/
curl -s http://127.0.0.1:6666/query -H "Content-Type: application/json" --data @MY_TEST_FILE.json -X POST
cd ../
~~~

## Documentation

In order to provide documentation about some modules that require specific input / output / configuration, the [doc](doc) directory contains detailed information about the general purpose, requirements, features, input and ouput of each of these modules:

- ***description** - quick description of the general purpose of the module, as the one given by the moduleinfo
- **requirements** - special libraries needed to make the module work
- **features** - description of the way to use the module, with the required MISP features to make the module give the intended result
- **references** - link(s) giving additional information about the format concerned in the module
- **input** - description of the format of data used in input
- **output** - description of the format given as the result of the module execution

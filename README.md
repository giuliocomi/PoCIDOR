# PocIDOR
A quick-to-edit script for providing Proof of Concept related to Insecure Direct Object Reference vulnerabilities in web application assessments when exposed resources can be requested by specifying their URL path.

It supports authenticated requests (session cookie needs to be specified) and proxying in order to log the traffic generated by the script.

Use {} has a placeholder for the sequential indexes.

- ![#1589F0](https://placehold.it/15/1589F0/000000?text=+)
Usage: pocidor.py [options] <target_url>
- ![#f03c15](https://placehold.it/15/f03c15/000000?text=+)
<code><pre>Options:
  -h, --help            show this help message and exit
  -c COOKIE_STRING, --cookie=COOKIE_STRING
                        Set cookies for the request
  -e EXTENSION, --extension=EXTENSION
                        Set extension
  -o FILENAME, --output=FILENAME
                        Set filename output
  -d DIRECTORY, --directory=DIRECTORY
                        Set directory
  -p PROXY, --proxy=PROXY
                        Set proxy
  -u USER_AGENT, --user-agent=USER_AGENT
                        Set User-Agent
  -m MIN, --min=MIN     Set minimum value
  -M MAX, --max=MAX     Set maximum value
  -P PAD, --padding=PAD
                        Set padding size
</pre></code>          

- ![#c5f015](https://placehold.it/15/c5f015/000000?text=+) Example:

<code>./pocidor.py --proxy 127.0.0.1:8080 --user-agent Security-Test --cookie JSESSIONID:valore "https://target.site/path/actionDoc.asp?method=details&idDoc=DOCA0{}&extensionFile=PDF&requestToken=ANTICSRFTOKEN" -m 000000 -M 999999 --padding 6</code>


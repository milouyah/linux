# [curl](https://curl.se/)


## Config Files
* `.curlrc`

* [Set Up cURL to Permanently Use a Proxy](https://www.baeldung.com/linux/curl-permanent-proxy)
* [curl: (77) error setting certificate verify locations](https://youremindmeofmymother.com/2016/03/28/curl-77-error-setting-certificate-verify-locations/)

```bash
proxy=http://127.0.0.1:8080
```

```bash
insecure 
# or
cacert=/etc/ssl/certs/ca-certificates.crt
```

# add export

```
export REQUESTS_CA_BUNDLE=~/crt/DigitalCity.crt

```
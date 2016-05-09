---
tags: citrix
created_on: 2016-05-09
---

# How to setup Citrix on Linux (tested on Fedora 23)

1. Download and install Citrix receiver (I used the web-version). [Link](https://www.citrix.com/downloads/citrix-receiver/linux/receiver-for-linux-latest.html)
2. Install the downloaded package:
  ```
  $ sudo dnf install ./ICAClientWeb-rhel-[...].rpm
  ```
3. Add additional certificates (optional)
  1. Download the certificates, e.g. [Thawte Root Certificates](https://www.thawte.com/roots/) (I selected Root 1 - without further reading into it)
  2. Move the certificates into the citrix directory:
    ```
    mv /path/to/cert.pem /path/to/citrix/ICAClient/keystore/cacerts/
    ```
4. Enjoy! (Or cry, that you now can use citrix)

# pf-cxs-dist
This repository contains the CXS distribution jar files you need in order to run CXS locally for development with a PubFactory site.

# 1.x
* Initial distribution.

# 2.x
* Updated for Java 10
* Basic auth support added
* Proxy support added

# Configuration
The above distributions include sample configuration files (cxs.yml).  These are dropwizard configuration files.

Generally you will only need to edit the lines with comments:

server > connector > **port** - By default the local CXS application will listen on port 8080.  If something else on your local machine is using this port, you can edit this value to use a different port.

* httpClient > **basicAuthUsername** - If connecting to a PubFactory site that is behind basic authentication, this is the basic auth username.

* httpClient > **basicAuthPassword** - If connecting to a PubFactory site that is behind basic authentication, this is the basic auth password.

* httpClient > **proxy** - If you access the internet through a proxy you will need this section.  Otherwise the entire proxy section can be removed.

* httpClient > proxy > **host** - The host for your proxy.

* httpClient > proxy > **port** - The host for your proxy.

* httpClient > proxy > **auth** - If your proxy requires authentication you will need this section.  Otherwise this section can be omitted.

* httpClient > proxy > auth > **username** - The username for your proxy.

* httpClient > proxy > auth > **password** - The password for your proxy.

* assets > overrides > **/** - The path to where you have checked out the "pf-client-*name*" git repository.

* workspace > **path** - The path to where you have checked out the "pf-client-*name*" git repository.

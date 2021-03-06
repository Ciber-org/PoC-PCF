# Pivotal Cloud Foundry

---

Cloud Foundry is an open source, multi cloud application_ _**platform as a service\(PaaS\)** governed by the Cloud Foundry Foundation. Cloud Foundry is promoted for continuous delivery as it supports the full application development lifecycle, from initial development through all testing stages to deployment. Cloud Foundry’s container-based architecture runs apps in any programming language over a variety of cloud service providers. This multi-cloud environment allows developers to leverage the cloud platform that suits specific app workloads and move those workloads as necessary within minutes with no changes to the app.

The_** cf**_ utility provides many options, but for deployment cf push is all that is required. It accepts arguments to specify the name of the application, where to load it from and the URL that should be used to access it. For example:

```
   cf push spring-music -i 2 -m 512M -n spring-music-v1 -p build/libs/spring-music.war
```

A commercial version called Pivotal Cloud Foundry \(PCF\) is available from Pivotal. It provides extra tools for installation and administration not included in the open software product. Pivotal Web Services \(PWS\), however, is an instance of Pivotal Cloud Foundry hosted on Amazon Web Services \(AWS\).

| Devolopers | Cloud Foundry Foundation /[Pivotal Software](https://en.wikipedia.org/wiki/Pivotal_Software) |
| :--- | :--- |
| Initial release | 2011; 7 years ago |
| Repository | [https://github.com/cloudfoundry/](https://github.com/cloudfoundry/)[![](https://upload.wikimedia.org/wikipedia/commons/thumb/7/73/Blue_pencil.svg/10px-Blue_pencil.svg.png "Edit this at Wikidata")](https://www.wikidata.org/wiki/Q5135664#P1324) |
| Written in | [Ruby](https://en.wikipedia.org/wiki/Ruby_%28programming_language%29),[Go](https://en.wikipedia.org/wiki/Golang) |
| Type | [Cloud computing](https://en.wikipedia.org/wiki/Cloud_computing) |
| License | [Apache License](https://en.wikipedia.org/wiki/Apache_License)2.0 |
| Website | [cloudfoundry.org](http://cloudfoundry.org/) |

This book is intended to document all the activities related to proof of concept developed for the deployment of applications on PCF/PWS. Records every steps from setup to deployment to scaling to continuous integration and continuous deployment.

#### **Contact:**

Mail us for any clarifications or suggestions 

Hahn, Mark &lt;[MHahn@ciber.com](/MHahn@ciber.com)&gt;

Lingaraj, Arunkumar &lt;[ALingaraj@ciber.com](/ALingaraj@ciber.com)&gt;


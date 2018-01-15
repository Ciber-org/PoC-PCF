### Getting Started

---

#### Create Account

Lets begin with Pivotal web services , an instance of PCF to deploy web apps.

Create an account using below link. You will receive an verification email from _**no-reply@run.pivotal.io. **_

[https://account.run.pivotal.io/z/uaa/sign-up](https://www.gitbook.com/book/ciber-org/anything-on-pcf/edit#)

* Click on the link to verify
* Proceed with mobile verification
* Create Org and add a space

#### Install CF CLI

Click on the link below to download. For windows, unzip and execute the file and follow the install instructions.

[https://pivotal.io/platform/pcf-tutorials/getting-started-with-pivotal-cloud-foundry/install-the-cf-cli](https://pivotal.io/platform/pcf-tutorials/getting-started-with-pivotal-cloud-foundry/install-the-cf-cli "Download CF CLI")

Open _**cmd**_ prompt and enter below command to check successful installation

```
cf -version
```

#### Set Credentials

Open command prompt and set your credentials for the pivotal end point.

```
cf login
```

Enter Email and Password. Default org will be selected. You can choose your space if more than one

##### ![](/assets/authenticate.png)

##### You are all set to deploy :\)




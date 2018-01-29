### Scale your Application

---

Scaling the application includes increasing your memory, disk space and/or increasing the running instances. _**Vertically scaling**_ an application changes the disk space limit or memory limit that Cloud Foundry applies to all instances of the application.

_**Horizontally scaling**_ an application creates or destroys instances of your application. Incoming requests to your application are automatically load balanced across all instances of your application, and each instance handles tasks in parallel with every other instance. Adding more instances allows your application to handle increased traffic and demand

We can scale our apps either using **cf **command line or using web login

### Using _cf_

**Scale Horizontally:**

Increase the number of app instances from one to two:

```
cf scale cf-spring -i 2
```

Check the status of the app and verify there are two instances running:

```
cf app cf-spring
```

**Scale Vertically:**

Scaling your app vertically, changes the disk space limit or memory limit for each app instance.

Increase the memory limit for each app instance:

```
cf scale cf-spring -m 1G
```

Increase the disk limit for each app instance:

```
cf scale cf-spring -k 512M
```

### Using Web

Login to your pivotal web services account and choose your organization and space. Click on your deployed application. You can see below screen. Increase/decrease your instances, memory limit and/or disk limit and click on _SCALE APP_ button. You can also choose auto scaling option for your applications.

![](/assets/scaleApp.png)

##### References:

* ###### [https://pivotal.io/platform/pcf-tutorials/getting-started-with-pivotal-cloud-foundry/scale-the-app ](/h ttps://pivotal.io/platform/pcf-tutorials/getting-started-with-pivotal-cloud-foundry/scale-the-app )
* ###### [http://docs.run.pivotal.io/devguide/deploy-apps/deploy-app.html\#intro](https://docs.run.pivotal.io/devguide/deploy-apps/cf-scale.html)




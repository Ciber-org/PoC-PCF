### Scale your Application

---

Scaling the application includes increasing your memory, disk space and/or increasing the running instances. _**Vertically scaling**_ an application changes the disk space limit or memory limit that Cloud Foundry applies to all instances of the application.

_**Horizontally scaling**_ an application creates or destroys instances of your application. Incoming requests to your application are automatically load balanced across all instances of your application, and each instance handles tasks in parallel with every other instance. Adding more instances allows your application to handle increased traffic and demand

We can scale our apps either using cf command line or using web login

### Using cf

Increase the number of app instances from one to two:

```
cf scale cf-spring -i 2
```

Check the status of the app and verify there are two instances running:

```
cf app cf-spring
```

Scaling your app vertically, changes the disk space limit or memory limit for each app instance.

Increase the memory limit for each app instance:

```
cf scale cf-spring -m 1G
```

Increase the disk limit for each app instance:

```
cf scale cf-spring -k 512M
```




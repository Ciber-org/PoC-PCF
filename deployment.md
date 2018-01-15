### Deploy

---

#### Prerequisites

Install below requisites before downloading sample applications. Ignore this step if its available

* Java 8 and above

  ```
             [https://java.com/en/download/\]\(https://java.com/en/download/](https://java.com/en/download/]%28https://java.com/en/download/)
  ```

* Gradle 4.4.x

  ```
             [https://gradle.org/install/\]\(https://gradle.org/install/](https://gradle.org/install/]%28https://gradle.org/install/)
  ```

* git

  ```
             [https://www.atlassian.com/git/tutorials/install-git](https://www.atlassian.com/git/tutorials/install-git)
  ```

#### Download

Clone a sample application from gitlab.

```
git clone https://gitlab.com/markphahn/st-test-01.git
```

Build the application using gradle. Change it to project directory and run

```
gradle build
```

#### ![](/assets/build.png)

#### Deploy

After successful build, deploy application to your created Org and Space. Run below cf push command in your project directory

```
cf push SpringTeamTest -p build/libs/SprintTeamTest.war
```

![](/assets/deploy.png)

Check the link [https://springteamtest.cfapps.io/](https://springteamtest.cfapps.io/) to test the running app.

###### You are all set to scale your app :\)




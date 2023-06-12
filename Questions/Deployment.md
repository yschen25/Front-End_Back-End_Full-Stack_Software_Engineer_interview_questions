# Deployment Questions

### **What Is CI (Continuous Integration)?**
> - A software development practice in which developers regularly merge their code changes into a shared repository. CI helps to ensure the codebase is always stable and there are no conflicts between different branches of code.

<br/>

### **What Is CD (Continuous Delivery)?**
> - An approach for software delivery in which development teams produce and test code in short but continuous cycles, usually with high degrees of automation, to improve software quality. 

<br/>


### **What Is CI/CD?**

<p align="center">
    <img src="img/itops-cicd_pipeline.png" alt="itops-cicd_pipeline.png" title="itops-cicd_pipeline.png" width="90%">
</p>

> - The following are general stages in a CI/CD process: <br/>
> (1) **Source**: The first step in the pipeline is where developers write and commit the smallest distributable units of code. The code gets tested by reviews, unit tests and static analysis. <br/>
> (2) **Build**: The source code is collected from the repository, linked to libraries, modules and dependencies, and compiled into an executable file. Tools log the process and denote errors to fix. Some builds may employ scripts to translate the executable file into a packaged or deployable execution environment, such as a VM or a Docker container. <br/>
> (3) **Test**: At this point, the code should be executable. It is tested at the subsystem level, including functional, performance and security tests. These ensure that the developed code meets the quality standards of an end user and the specifications of the project.  <br/>
> (4) **Deploy**: Finally, the software should be ready to be deployed into the production environment, but first, the code is manually checked one last time. <br/>
> - Related Reference: [continuous delivery (CD)](https://www.techtarget.com/searchitoperations/definition/continuous-delivery-CD)

<br/>



### **What Is Cloud Computing?**
> - The cloud(internet) computing is a way of `managing IT resources that replaces local machines and private data centers with virtual infrastructure`, including servers, storage, databases, networking, software, analytics. Users access virtual compute, network, and storage resources made available online by a remote provider. 
> - These resources can be provisioned instantly, which is particularly useful for companies that need to scale their infrastructure up or down quickly in response to fluctuating demand.
> - Related Reference: [徹底了解 Cloud Computing](https://www.ithome.com.tw/article/93006)

<br/>


### **How Do You Deploy Your Code To The Production?**
> - (1) Scan code quality by ESLint and SonarLint.
> - (2) Test by product manager.
> - (3) Push to github then test by pipeline.
> - (4) Code review by boss or colleagues.
> - (5) Repeat 2 - 5 until to the production.

<br/>


### **What Is The Semantic Version?**

| 3 | 2 | 6 | 
|---|---|---|
| Major | Minor | Patch  |


> - The semantic version is `consist of Major, Minor and Patch`.
> - **Add Major** : it means add new function and it **IS NOT** downward compatibility, mahor number add one, minor and patch number change to 0.
> - **Add Minor** : it means add new function and it **IS** downward compatibility, minor number add one, patch number change to 0.
> - **Add Patch** : it means fixs the simple bugs, patch number add one.
> - Related Reference : [SemVer - 語意化版本規範](https://www.eebreakdown.com/2016/09/semver.html)

<br/>



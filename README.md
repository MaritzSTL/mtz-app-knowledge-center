# Polymer Knowledge Center

_Our Promise: We'll take you from having zero knowledge of Polymer to fixing your first bug in under four weeks!_

---

### About

1.  [What Is The Objective?](#What-Is-The-Objective)
2.  [How Do I Contribute?](#How-Do-I-Contribute)
3.  [Additional Tasks](#Additional-Tasks)

### Getting Started

1.  [Developer Access](#Developer-Access)
2.  [Environment Setup](#Environment-Setup)
3.  [Deployment](#Deployment)

### Learning Resources

1.  [References](#References)
2.  [Video Training Courses](#Video-Training-Courses)
3.  [Tutorials](#Tutorials)

---

### What Is The Objective?

Polymer allows you to put software in any person's hands, anywhere on earth, faster and more maintainably than its competitors. However, Polymer has a problem: all of its documentation is reference material, not teaching material. Polymer's documentation is written for people who already understand Polymer, not those who are just getting started.

The purpose of the Polymer Knowledge Center is to teach Polymer by taking a learning by teaching approach.

References the [Learning Resources](#Learing-Resources) section for training and relevant Polymer information.

As you build out each chapter writing the markdown files of your own, you can both learn and refine the material for this project for the entire team.

##### [back to top](#Polymer-Knowledge-Center)

---

### How Do I Contribute?

1.  Get Familiar With Polymer [Learning Resources](#Learning-Resources)
2.  Complete [Getting Started](#Getting-Started)
3.  Commit and push the changes from your local branch.
4.  Make a pull request.
    * Complete any of the [additional tasks](#Additional-Tasks)
    * Update this README.md file with any relevant information that meets the following criteria:
      * Any information you found helpful
      * Any information you found unclear
      * Any information obsolete

##### [back to top](#Polymer-Knowledge-Center)

---

### Additional Tasks

## Tasks Which Need to Be Completed

* Analytics Embedded Into App
  * Online
  * Offline
* Authentication

## Chapters Which Need to Be Written

* Linting / Code Format Standards
* Appropriate Testing
* Device Responsiveness
* i18n
* Customizability
  * Is responsive to app-level defaults
  * For example: you can set app colors on per-client basis
* Actual Code
  * Events Up
  * Properties Down
* Reuse Considerations
* Service Workers

##### [back to top](#Polymer-Knowledge-Center)

---

### Developer Access

##### [back to top](#Polymer-Knowledge-Center)

---

1.  Make sure you have a registered Maritz email address receiving mail.
2.  Create a [BitBucket](https://bitbucket.org) account with your Maritz email address.
3.  Create a [GitHub](https://github.com) account.
    * If you already have a GitHub account
      * Use your personal account if you prefer
    * If you don't have a GitHub account
      * Create your new GitHub account using your personal OR Maritz email address
      * It would be helpful to create an SSH Key to avoid entering your username and password every time
      * It would be useful to add an environment variable to git.exe
4.  Request a BitBucket Invitation.
    * Kindly ask Adam for an invitation **adam.rider@maritz.com**
    * Adam will need your Maritz email address
5.  Request a GitHub Invitation.
    * Kindly ask Chris for an invitation **chris.zempel@maritz.com**
6.  Check the 'Other' conversations link via Microsoft Outlook if you do not immediately see the email invites in your inbox.

---

### Environment Setup

##### [back to top](#Polymer-Knowledge-Center)

---

1.  Make sure you have an active Maritz email account.
2.  Install any desired code editor.
    * [Atom](https://atom.io)
    * [Brackets](http://brackets.io)
    * [Notepad++](https://notepad-plus-plus.org)
    * [Sublime Text](https://www.sublimetext.com)
    * [Visual Studio Code](https://code.visualstudio.com)
3.  Install [Node.js](https://nodejs.org/en/download)

4.  Install [Git](https://git-scm.com/downloads).
5.  Modify global Git configuration.

    * Provide User Name
      * Provide full name
      * Full name will be attached to your commits
      ```ps
      git config --global user.name '<user name>'
      ```
    * Provide Maritz Email Address
      * Email addresses can be uniquely modified locally per repository
      ```ps
      git config --global user.email '<maritz email>'
      ```
    * Git Ignore File Configuration
      * This may already be set with a fresh installation of Git
      ```ps
      git config --global core.excludesfile '~/.gitignore'
      ```
    * Git Http Post Buffer Configuration

      * This is needed when dealing with bigger projects to set up a buffer big enough for transferring data

      ```ps
      git config --global http.postBuffer 524288000
      ```

6.  Create desired working directory for repository
    ```ps
    mkdir c:\YOUR_DESIRED_PATH\mtz-app-knowledge-center
    ```
7.  Clone [Maritz Knowledge Center](https://github.com/MaritzSTL/mtz-app-knowledge-center) repository.
    * Use an SSH key and passphrase from account.
    ```ps
    git clone git@github.com:MaritzSTL/mtz-app-knowledge-center.git
    ```
8.  Install [Bower](https://bower.io).
    ```ps
    npm install -g bower
    ```
9.  Create a local branch from master.

    * Using your initials lowercase seems to be the convention for mtz-app-knowledge-center repository contributions

10. Install Polymer.

    ```ps
    npm install -g polymer-cli
    ```

---

### Deployment

##### [back to top](#Polymer-Knowledge-Center)

---

1.  Navigate to your mtz-app-knowledge-center working directory.
2.  Install Bower locally.
    ```ps
    bower install
    ```
3.  Open 'mtz-app-knowledge-center' in desired code editor.
    ```ps
    polymer serve --open
    ```
4.  Make sure you have your branched checked out.

    ```ps
    git branch
    ```

5.  Push your branch.
    ```ps
    git pull https://github.com/forkuser/forkedrepo.git yourBranchNameHere
    ```

---

# Learning Resources

### References

* [Polymer Project](https://www.polymer-project.org)
  * [Polymer 1](https://www.polymer-project.org/1.0/docs/devguide/feature-overview)
  * [Polymer 2](https://www.polymer-project.org/2.0/docs/devguide/feature-overview)
  * [Polymer 3](https://www.polymer-project.org/3.0/docs/devguide/feature-overview)
* [Web Components](https://www.webcomponents.org)

##### [back to top](#Polymer-Knowledge-Center)

### Video Training Courses

* [Lynda](https://www.lynda.com)
  * Free unlimited subscription with a registered [St. Louis County Library](https://www.slcl.org) card
  * 30 day free trial
    * [Learning Polymer](https://www.lynda.com/Polymer-tutorials/Learning-Polymer/540536-2.html?srchtrk=index%3a1%0alinktypeid%3a2%0aq%3aPolymer%0apage%3a1%0as%3arelevance%0asa%3atrue%0aproducttypeid%3a2)
    * [Learning Web Components](https://www.lynda.com/Web-Development-tutorials/Learning-Web-Components/540537-2.html?srchtrk=index%3a4%0alinktypeid%3a2%0aq%3aWeb+Components%0apage%3a1%0as%3arelevance%0asa%3atrue%0aproducttypeid%3a2)
* [Pluralsight](https://www.pluralsight.com)
  * 30 day free trial
    * [Getting Started with Polymer.js](https://www.pluralsight.com/courses/polymer-js-getting-started)
    * [Working with Polymer.js Elements](https://www.pluralsight.com/courses/polymer-js-elements-working)
    * [Building a Web Application with Polymer.js and Material Design](https://www.pluralsight.com/courses/building-web-application-polymer-material-design)
* [Udemy](https://www.udemy.com)
  * Pricing varies per course
    * [Learn and Build using Polymer 2 - plus Polymer 1](https://www.udemy.com/learn-and-build-using-polymer)
    * [Polymer 3 - Code Like A Google Developer](https://www.udemy.com/polymer-3-code-like-a-google-developer)

##### [back to top](#Polymer-Knowledge-Center)

### Tutorials

* [Building Your First Polymer App](https://auth0.com/blog/build-your-first-app-with-polymer-and-web-components)

##### [back to top](#Polymer-Knowledge-Center)

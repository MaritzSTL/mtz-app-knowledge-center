# Polymer Knowledge Center

_Our Promise: We'll take you from having zero knowledge of Polymer to fixing your first bug in under four weeks!_

---

### About

1.  [What Is The Objective?](#what-is-the-objective)
2.  [How Do I Contribute?](#how-do-i-contribute)
3.  [Additional Tasks](#additional-tasks)

### Getting Started

1.  [Developer Access](#developer-access)
2.  [Environment Setup](#environment-setup)
3.  [Deployment](#deployment)

### Learning Resources

1.  [References](#references)
2.  [Video Training Courses](#video-training-courses)
3.  [Tutorials](#tutorials)

### Chapters

* This Polymer app simply iterates over all of the markdown files in the chapters folder, then displays them on the home page when the application starts.
* The chapters are zero base indexed.

1.  Chapter 0: [Web Components](chapters/0.md)
2.  Chapter 1: [A New Kind of `<div>`](chapters/1.md)
3.  Chapter 2: [Developing Better](chapters/2.md)
4.  Chapter 3: [Routing](chapters/3.md)

### Troubleshooting

* [Setting Up SSH Keys](#setting-up-ssh-keys)

---

### What Is The Objective?

Polymer allows you to put software in any person's hands, anywhere on earth, faster and more maintainably than its competitors. However, Polymer has a problem: all of its documentation is reference material, not teaching material. Polymer's documentation is written for people who already understand Polymer, not those who are just getting started.

The purpose of the Polymer Knowledge Center is to teach Polymer by taking a learning by teaching approach.

References the [Learning Resources](#learning-resources) section for training and relevant Polymer information.

As you build out each chapter writing the markdown files of your own, you can both learn and refine the material for this project for the entire team.

##### [back to top](#polymer-knowledge-center)

---

### How Do I Contribute?

1.  Get familiar with Polymer [Learning Resources](#learning-resources).
2.  Complete [Getting Started](#getting-started).
3.  Update, rewrite, or add any additional chapters.

    * Reference [Chapters](#chapters) for additional ideas.
    * Reference [known issues](https://github.com/maritzstl/mtz-app-knowledge-center/issues) via GitHub
    * Complete any of the [additional tasks](#additional-tasks)
    * Update this README.md file with any relevant information that meets the following criteria:
      * Any information you found helpful
      * Any information you found unclear
      * Any information obsolete

4.  Commit and push the changes from your local branch.
5.  Make a pull request.
    * Via BitBucket (TODO)
    * Via GitHub
      * Navigate to [Pull Requests](https://github.com/maritzstl/mtz-app-knowledge-center/pulls)
        1.  Make sure your changes are pushed.
        2.  Click **New Pull Request**.
        3.  Make sure you see the following **base: master <- compare: yourBranchNameHere**.
        4.  Click **Create Pull Request** button.
        5.  Begin pull request message body with **_#X some text here_** (where X is the number of the issue).
        6.  Provide title or description of your pull request.
        7.  Update the Slack channel [se-pull-requests](https://maritz-motivation.slack.com/messages/C9BQ4GPLK) accordingly.

##### [back to top](#polymer-knowledge-center)

---

### Additional Tasks

## Tasks Which Need to Be Completed

* Analytics Embedded Into App
  * Online
  * Offline
* Authentication
* Add BitBucket Pull Request Steps

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

##### [back to top](#polymer-knowledge-center)

---

### Developer Access

##### [back to top](#polymer-knowledge-center)

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

##### [back to top](#polymer-knowledge-center)

---

1.  Make sure you have an active Maritz email account.
2.  Install any desired code editor.
    * [Atom](https://atom.io)
    * [Brackets](http://brackets.io)
    * [Notepad++](https://notepad-plus-plus.org)
    * [Sublime Text](https://www.sublimetext.com)
    * [Visual Studio Code](https://code.visualstudio.com)
3.  Install [Node.js](https://nodejs.org/en/download).
4.  Install [Git](https://git-scm.com/downloads).
5.  Modify global Git configuration.

    * Provide User Name
      * Provide full name
      * Full name will be attached to your commits
      ```ps
      git config --global user.name "yourUserName"
      ```
    * Provide Maritz Email Address
      * Email addresses can be uniquely modified locally per repository
      * Note: Although your global email address will be globally set for Maritz, your registered GitHub email will be required locally for this Polymer Knowledge Center repository.
      ```ps
      git config --global user.email "yourEmail@maritz.com"
      ```
    * Git Ignore File Configuration
      * This may already be set with a fresh installation of Git
      ```ps
      git config --global core.excludesfile "~/.gitignore"
      ```
    * Git Http Post Buffer Configuration

      * This is needed when dealing with bigger projects to set up a buffer big enough for transferring data

      ```ps
      git config --global http.postBuffer 524288000
      ```

6.  Create desired working directory for repository.
    ```ps
    mkdir c:\YOUR_DESIRED_PATH\mtz-app-knowledge-center
    ```
7.  Clone the [Polymer Knowledge Center](https://github.com/MaritzSTL/mtz-app-knowledge-center) repository.
    * Use an SSH key and passphrase from account.
    * See [Setting Up SSH Keys](#setting-up-ssh-keys) if you do not already have keys setup.
    ```ps
    git clone git@github.com:MaritzSTL/mtz-app-knowledge-center.git
    ```
8.  Set your local config file 'user.email' and 'username'.

* This is where you set your local config email address to whichever one is tied to your GitHub account
* The user name you set here will be your GitHub profile user name shown in your GitHub profile url
  ```ps
  git config user.email "yourRegisteredEmailWithGitHub@example.com"
  git config username "yourUserName"
  ```

9.  Verify your local config file user settings.

    * Open and inspect config file **"..\mtz-app-knowledge-center\.git\config"**

    Example

    ```ps
        [user]
            name = Terrence Bowen
            email = terrence.bowen@gmail.com
            username = terrencebowen
    ```

10. Install [Bower](https://bower.io).


    ```ps
    npm install -g bower
    ```

11. Create a local branch from master.

    * Using your initials lowercase seems to be the convention for mtz-app-knowledge-center repository contributions

12. Install Polymer.

    ```ps
    npm install -g Polymer-cli
    ```

---

### Deployment

##### [back to top](#polymer-knowledge-center)

---

1.  Navigate to your mtz-app-knowledge-center working directory.
2.  Install Bower locally.
    ```ps
    bower install
    ```
3.  Open 'mtz-app-knowledge-center' in desired code editor.
    ```ps
    Polymer serve --open
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

##### [back to top](#polymer-knowledge-center)

### Video Training Courses

* [Lynda](https://www.lynda.com)
  * Free unlimited subscription with a registered [St. Louis County Library](https://www.slcl.org) card
  * 30 day free trial
    * [Learning Polymer](https://www.lynda.com/Polymer-tutorials/Learning-Polymer/540536-2.html?srchtrk=index%3a1%0alinktypeid%3a2%0aq%3aPolymer%0apage%3a1%0as%3arelevance%0asa%3atrue%0aproducttypeid%3a2)
    * [Learning Web Components](https://www.lynda.com/web-development-tutorials/learning-web-components/540537-2.html?srchtrk=index%3a4%0alinktypeid%3a2%0aq%3aweb+components%0apage%3a1%0as%3arelevance%0asa%3atrue%0aproducttypeid%3a2)
* [Pluralsight](https://www.pluralsight.com)
  * 30 day free trial
    * [Getting Started with Polymer.js](https://www.pluralsight.com/courses/polymer-js-getting-started)
    * [Working with Polymer.js Elements](https://www.pluralsight.com/courses/polymer-js-elements-working)
    * [Building a Web Application with Polymer.js and Material Design](https://www.pluralsight.com/courses/building-web-application-polymer-material-design)
* [Udemy](https://www.udemy.com)
  * Pricing varies per course
    * [Learn and Build using Polymer 2 - plus Polymer 1](https://www.udemy.com/learn-and-build-using-polymer)
    * [Polymer 3 - Code Like A Google Developer](https://www.udemy.com/polymer-3-code-like-a-google-developer)

### Tutorials

* [Building Your First Polymer App](https://auth0.com/blog/build-your-first-app-with-polymer-and-web-components)

##### [back to top](#polymer-knowledge-center)

# Troubleshooting

### Setting Up SSH Keys

1.  Open git bash (Use the Windows search. To find it, type "git bash") or the Mac Terminal.

    **Pro Tip: You can use any nix based command prompt (but not the default Windows Command Prompt!)**

2.  Type cd ~/.ssh. This will take you to the root directory for Git (Likely C:\Users\[YOUR-USER-NAME]\.ssh\ on Windows).

3.  Within the .ssh folder, there should be these two files: id_rsa and id_rsa.pub. These are the files that tell your computer how to communicate with GitHub, BitBucket, or any other Git based service. Type ls to see a directory listing. If those two files don't show up, proceed to the next step.

    **NOTE: Your SSH keys must be named id_rsa and id_rsa.pub in order for Git, GitHub, and BitBucket to recognize them by default.**

4.  To create the SSH keys, type ssh-keygen -t rsa -C "yourRegisteredEmailWithGitHub@example.com". This will create both id_rsa and id_rsa.pub files.

5.  Now, go and open id_rsa.pub in your favorite text editor (you can do this via Windows Explorer or the OSX Finder if you like, typing open . will open the folder).

6.  Copy the contents--exactly as it appears, with no extra spaces or lines--of id_rsa.pub and paste it into GitHub and/or BitBucket under the Account Settings > SSH Keys. NOTE: I like to give the SSH key a descriptive name, usually with the name of the workstation I'm on along with the date.

7.  Now that you've added your public key to Github and/or BitBucket, try to git push again and see if it works.

For more help available from GitHub [Connecting to GitHub with SSH](https://help.github.com/articles/connecting-to-github-with-ssh) and BitBucket Help [Troubleshoot SSH issues](https://confluence.atlassian.com/bitbucket/troubleshoot-ssh-issues-271943403.html).

##### [back to top](#polymer-knowledge-center)

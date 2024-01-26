# Resources for Instructors

---

## Course Website

The course website ([https://mountain-hydrology-research-group.github.io/data-analysis/](https://mountain-hydrology-research-group.github.io/data-analysis/)) is hosted on [GitHub Pages](https://pages.github.com/) as a repository under the Mountain-Hydrology-Research-Group github organization, [here](https://github.com/Mountain-Hydrology-Research-Group/data-analysis). It is organized and formatted as a [Jupyter Book](https://jupyterbook.org/en/stable/intro.html). 

### Getting started

1. **Log into your github account**, or create an account on [github](https://github.com/) (Note: your account will need to be connected to the Mountain-Hydrology-Research-Group github organization)
2. **Go to the course website repository** at https://github.com/Mountain-Hydrology-Research-Group/data-analysis
3. **Create your own [fork](https://www.earthdatascience.org/workshops/intro-version-control-git/about-forks/) of the repository**. (It is good practice to work on a separate fork, your own personal copy, of the repository while you update the website.)
4. **[Clone](https://www.earthdatascience.org/workshops/intro-version-control-git/basic-git-commands/) the repository** onto the class JupyterHub or to your personal computer. (The advantage of having a clone of the respository on the JupyterHub is to test out the jupyter notebooks for labs in the same environment students will be using.)
5. Repeat steps 2-4 with the [repository containing homework solutions](https://github.com/Mountain-Hydrology-Research-Group/data-analysis-solutions). (This is a private repository accessible only to approved users. It is not connected to the class website.)
6. **Add and Commit changes to your own fork** as you work on updating content.
7. When your own fork is now up to date with your changes, **open a [pull request](https://www.earthdatascience.org/workshops/intro-version-control-git/pull-request/)** to merge the changes from your fork into the repository under the Mountain-Hydrology-Research-Group github organization.

The website is currently published through github pages, so the following step only needs to be taken if the site was ever un-published. I am just including it here for reference. When you are ready to publish the website, click on *Settings* (with the gear icon) in the menu at the top of the repository page (the Mountain-Hydrology-Research-Group repository, not your own fork). On the left side of the Settings menu, click on *Pages*. Now you need to tell GitHub to enable "Pages" and which branch you would like to publish. For the dropdown menu under *Source* make sure that "Deploy from a branch" is selected. Then used the dropdown menu  under *Branch* to select the branch you want to publish (currently this is the "gh-pages" branch), then from the new dropdown menu that appears with the folder icon, make sure that "/ (root)" is selected. This is telling GitHub where the files for your website are located. Then click "Save" and the website should be up in a few minutes.

### File organization

In your cloned respository, in the top level `data-analysis/` directory, you can find a subdirectory called `book` which contains the website. Under `book` course content is organized into:
* `overview` folder, contains syllabus and project pages
* `modules` folder, each module/lab corresponds roughly to one week of the quarter. The `module#.md` files create the main page for each module with the lab and homework assignment text, while the `lab#/` folder corresponding to that modules contains the jupyter notebook files. The `data/` folder contains any data files for labs or homeworks.
* `resources` folder, jupyter and python documentation and links to other websites of interest to students learning hydrology, statistics, and programming
* `images` folder containing any images to embed on the website
* the file `_toc.yml` controls the table of contents displayed on the left side of the website

### Updating the website and Jupyter Notebooks

Working with your fork of the repository that you've cloned, you can directly edit any of the markdown (.md) files in any text editor. If you are working on the JupyterHub, the lab jupyter notebooks can be opened and edited directly from the hub. If you are working on your own computer, you will need to launch your own instance of jupyter notebook then open the notebook files to edit. Besides the webpage markdown (.md) files and jupyter notebook (.ipynb) files, there are data files (primarily csv or excel files) for homework and lab activities within the `data-analysis/modules/data` directory.

When you've made the changes you want, [commit and push](https://www.earthdatascience.org/workshops/intro-version-control-git/basic-git-commands/) the modified files to your fork of the respository. Then [open a pull request](https://www.earthdatascience.org/workshops/intro-version-control-git/pull-request/) from the [upstream repository](https://github.com/Mountain-Hydrology-Research-Group/data-analysis) to pull the changes made in your fork. After merging the pull request, the changes will appear on the class website within a few minutes as the page is re-built from the new files.

### Tag a commit and make end-of-year release

I've started adding a tag to the last commit made at the end of the quarter to label the state of the website at the time that each year's class ends. To tag a commit from the command line, first find the commit id on github (seven character string, looks something like this "25b6522"). Then in your command line (on your own fork of the repository) use the command:

`git tag -a v2022.0 25b6522 -m "End of year 2022"`

This is tagging the commit with id "25b6522" with the tag "v2022.0" (I just started using the year as a version number, perhaps if someone wanted to use these tags more they could have v2022.1, v2022.2, etc). Additionally this adds a message to describe what we're doing here (-m "End of year 2022"). Next, we need to push this tag, not to your own fork, but to the Mountain-Hydrology-Research-Group repository. If you have this [configured as "upstream"](https://devopscube.com/set-git-upstream-respository-branch/) then you can use the command:

`git push upstream --tags`

Now on the [repository on github](https://github.com/Mountain-Hydrology-Research-Group/data-analysis/), you can create a new [Release](https://github.com/Mountain-Hydrology-Research-Group/data-analysis/releases) and pick the tag you just created from the dropdown menu.

## Slack

### Create a new Slack workspace

1. Go to https://slack.com/create and start by entering your uw.edu email address, then entering the confirmation code sent to you.
2. For *"What's the name of your company or team?"* use the course name and year in a format like **uw-waterdata2021** (this will be the name and URL of the Slack workspace)
3. For *"What’s a project your team is working on?"* enter "projects" to create a channel with this name (a channel to discuss final projects). More channels can be added later.
4. You can click "skip" when prompted for *"Who do you email most about this project?"* (People can be added later to the workspace)
5. Then finish up by clicking *"See your slack channel"*
6. Your slack workspace should now be accessable at *uw-waterdata2021.slack.com* in a web browser, or as *uw-waterdata2021* in the Slack desktop application.
7. For a 10-week course with ~15 students, the free plan has been sufficient. For larger classes, you might hit the 10K message limit during the quarter, in which case, some early messages will not longer be visible.

### Add people to the workspace

1. In the slack workspace, click on the workspace name on the left to open a dropdown menu.
2. Then select *Settings & Administration*, then under Administration select *Manage Members*.
3. Here you can invite people using their email addresses, as well as change their *Account Type* (such as for adding additional administrators). You can do this with list of email addresses or click the "*Get an invite link to share*" and send to an email list.
4. Set default channels to join (such as the channels mentioned below)
* More workspace settings are available on the left hand side of this admin webpage.
* Optional: add a unique icon for the workspace (useful if you are logged into many workspaces on Desktop app)

### Set up your workspace channels

1. Add private `#admin` channel for TAs, IT staff
2. Add public `#it_help` channel for students to get help with Jupyter issues
3. Add public `#project` channel for discussion of student projects (will see more activity later in quarter)
4. Optional: limit permissions on the `#general` channel so only admins and specific users can post announcements
5. On the `#general` channel, post a new welcome message and create a quick-reference list of links to the various resources that will be used throughout the course (Jupyterhub url, Github Organization url, etc.).  
   * Pin this by clicking the three dots in upper right corner of the message and selecting "*Pin to channel*".  
   * Add a note that students can always find this list by clicking the Pin icon near top of the channel:

Example:
> **Welcome to the Data Analysis in Water Sciences - Fall 2022 Slack Workspace**
> We will be using Slack for most day-to-day communications, and for you all to collaborate on labs, homework assignments, and (for graduate students) projects.
> There is a channel for each weekly module for discussions about each lab and assignment, a channel for initiating discussion around #projects, a #general channel for announcements and general discussions, and an #it_help channel for trying to resolve issues with JupyterHub or other IT issues.
> **Please edit your Slack profile, add a picture, add your preferred name and pronouns as your "Display Name", and your time zone.**
> Please bookmark these pages for easy access:
> * **Class website**: https://mountain-hydrology-research-group.github.io/data-analysis/ (contains the syllabus, labs, homework assignments, links to other resources)
> * **UW Canvas**: https://canvas.uw.edu/ (for turning in assignments, grades, extra reading resources)
> * **JupyterHub**: https://rttl.axdd.s.uw.edu/2022-autumn-cee-465-a/ (the computing environment we’ll be using for labs, homework, projects, instructions for getting started are here)
> * **Slack Workspace**: uw-waterdata2020.slack.com (for communication, questions, collaboration)







---

Thank you to David Shean for providing course organization ideas and help from [this guide](https://github.com/UW-GDA/gda_course_2020/tree/master/resources/instructors).
* Slack setup steps are modified from [these instructions](https://github.com/UW-GDA/gda_course_2021/blob/master/resources/instructors/instructor_initial_setup.md)
* 

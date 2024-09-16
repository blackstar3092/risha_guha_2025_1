---
layout: page
title: Tools
permalink: /tools/
---
## Tools Setup

Prior to setting up my tools for this class, I already had experience with Github, VSCode, and WSL. I needed to install a new version of WSL (24.04 as opposed to 22.04). Because of my prior experience with Linux, installation and cloning of the Github repositories went smoothly. However, I did not realize that I needed to fork the repository before cloning it; as soon as I fixed this issue, I was able to edit the repository to customize it.


<h2> Tools Hacks </h2>

<h3> Shell Command Descriptions: </h3>
  <ul>
    <li>wsl - access Windows Subsystem for Linux - We are using Ubuntu 24.04 for our projects. </li>
    <li>cd - change directoru</li>
    <li>mkdir - create directory</li>
    <li>echo - print text</li>
    <li>sudo - execute commands with elevated privileges</li>
    <li>apt - manage packages in Debian-based Linux distributions</li>
    <li>git - manage version control of files and directories</li>
    <li>code - open files or directories in Visual Studio Code</li>
    <li>ls - list directory contents</li>
    <li>rm - remove files or directories</li>
    <li>cp - copy files or directories</li>
    <li>mv - move files or directories</li>
    <li>find - search for files or directories</li>
    <li>grep - search for text patterns within files</li>
  </ul>

<h3> Version Control </h3>

**GitHub and VSCode Setup**

- Version Control: A system to track changes to files over time. We use GitLens and VSCode commit history as version control.
- Git: A popular version control system.
- GitHub: A web-based hosting service for Git repositories.
- Repository: A collection of files and directories, which can be local or stored on the cloud. 

**Files on Local Machine**

- Cloning: Downloading a repository from GitHub to your local machine.
- Navigation: Use the terminal to navigate to the cloned repository's directory.
- Files: Located within the cloned repository's structure. They can be locally stored or not. 

**Updating GitHub**

- Committing: Recording changes to files in your local repository.
- Pushing: Sending committed changes to your remote GitHub repository.
- Navigation: Use GitHub's web interface to navigate to the repository and view the files.

**Updating Portfolio_2025 Template**

- Clone: Clone the template repository to your local machine.
- Edit: Modify the files to suit your specific course requirements.
- Commit: Commit your changes.
- Push: Push the changes to your remote GitHub repository.

<h3> Localhost vs. Deployed Server and DNS </h3>

- A localhost server has a url of http://127.0.0.1:4100/myrepositoryname. Changes shown on local repository before I push changes are not necessarily reflected to everyone on the internet. Others can not access my website through this link.
- A deployed server has a url of http://myusername.github.io/page. This is globally available and only shows pushed changes
- The domain for my GitHub Pages is https://blackstar3092.github.io/.
- My url is similar to my neighbors because it relies on the base url of github.io, but our usernames are different. 

<h2> Tools Verification </h2>

**Installation**
- My git version is 2.43.0
- My ruby version is 3.2.3
- My python version is 3.12.3

While installing ruby, I was met with an error regarding permissions. However, running the venv environment as administrator and reinstalling solved the problem.


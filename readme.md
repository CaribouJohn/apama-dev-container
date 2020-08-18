Apama dev-container
===================

This repository is a base for developing an apama project without installing Apama on your local hardware. The default image that will be used will contain the Apama software and command line tooling necessary to build a project and run in a correlator. vs-code, pysys-vscode-extension and apama-vscode-extension provide the framework for writing, debugging and launching the code.

Requirements
------
vs-code requires that the remote [development extension]https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack) be installed

The dev-container requires a docker installation to be accessible to the instance of vs-code opening the dev-container. The following documents detail what is required and gives a good explanation of what it does.

* See [Developing inside a Container](https://code.visualstudio.com/docs/remote/containers)
  * Mount a local volume (__persistent__)
* See [Cloning into a Container](https://code.visualstudio.com/docs/remote/containers#_quick-start-open-a-git-repository-or-github-pr-in-an-isolated-container-volume)
  * Work within the container (__transient__)

How-To
------

* Clone this repo or download the zip from [GitHub](https://github.com/CaribouJohn/apama-dev-container.git)
* **or** shift-ctrl-p git: clone in vscode its self
* Now open the folder in vscode
* vs-code should show a dialog asking whether you wish to reopen in a container or clone into the container.
* choose the option you prefer
  * if you reopen then you will mount the current dir as a volume
  * if you clone it will mean you develop in the container

Modifying the Setup
------------------------

The Dockerfile is currently a minimal working example of what can be done. By modifying the Dockerfile the user can add extra tooling and sources to handle requirements of all sorts.

Examples of what you could do with the Dockerfile can be found in a blog post on the Apama Community site: [Build test and deploy Apama Projects using the apama-builder-image](http://www.apamacommunity.com/build-test-and-deploy-apama-projects-using-the-apama-builder-image/)

The devcontainer.json file also allows easy setup of mounts, port forwarding and even access to docker from within docker.

The microsoft tutorial for using the facility more generally can be accessed here : [Containers Tutorial](https://code.visualstudio.com/docs/remote/containers-tutorial)

Options in the devcontainer.jso can be found [here](https://code.visualstudio.com/docs/remote/devcontainerjson-reference)

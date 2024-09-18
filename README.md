# Local Development Options for Windows

When working through the course, I use two main approaches to run my notebooks locally:

1. **Using WSL2**  
   Jeremy has covered this in parts throughout the course.

2. **Using DevContainers**  
   I find DevContainers to be a convenient way to get started on a new project. Essentially, each project is isolated inside its own Linux environment, functioning like a self-contained development machine.

## DevContainer Basics

A **DevContainer** is a feature in Visual Studio Code that allows developers to define a containerized environment for their projects. This helps streamline development by ensuring consistent environments across different machines, eliminating the "it works on my machine" issue. By using a `devcontainer.json` configuration file, you can specify the tools, dependencies, and settings needed for your project. These are automatically applied when the container starts, making DevContainers ideal for collaborative teams or projects with complex setups.

## DevContainer Requirements

To start using DevContainers, you'll need a few key components:

- **Docker**, which provides the containerization platform.
- **Visual Studio Code** with the **Remote - Containers** extension, allowing seamless integration of DevContainers into VS Code.

Once these are installed, you can define the environment for your project using a `devcontainer.json` file, which configures tools, libraries, and settings.

## Bootstrapping Your New Project

If you check out my sample project [here](https://github.com/CraigRichards/fastai_pet_clasifier), you'll notice a DevContainer folder that contains the necessary configuration files to get started.

Once you have Docker and the VS Code extensions installed, opening this project will trigger a prompt to **Reopen in Container**. VS Code will automatically build the container, install the required dependencies in a Linux environment, and create a Conda environment named `work`, all set up and ready for development.

The code in the project is secondary—if you open the notebook, you'll see that a kernel named `work` is ready for you.

## Bootstrapping Your Own Project

If you have the course repository cloned locally or want to set up your personal project, simply copy the `.devcontainer` folder from my project into your own. When you open it in VS Code, it'll automatically bootstrap a new environment for you.

## Pro-Tip

For each new project, don't forget to update the environment name in the `devcontainer.json` file. While not strictly necessary, giving your environment a unique name can help you stay organized, especially when managing multiple projects.

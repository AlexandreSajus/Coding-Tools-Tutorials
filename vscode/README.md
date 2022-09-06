# **VSCode**

VSCode is a code editor available for Windows, Mac, and Linux. It comes with a rich ecosystem of extensions for languages support, version control, code verification, formatting, auto-completion and more.

<p align="center">
  <img src="media/vscode.png" alt="VSCode Example" width="100%"/>
</p>

## **Table of contents**
- [**VSCode**](#vscode)
  - [**Table of contents**](#table-of-contents)
  - [**Why use VSCode?**](#why-use-vscode)
  - [**Installation**](#installation)
    - [**Windows**](#windows)
    - [**Linux**](#linux)
    - [**Mac**](#mac)
  - [**Useful extensions**](#useful-extensions)

## **Why use VSCode?**

VSCode is an extremely user-friendly code editor. Its intuitive UI makes coding, version control and debugging easy. The extension marketplace allows users to install and use many tools for linting, formatting, collaboration and more.

Here are some example usecases of VSCode:

+ **Jupyter Support**
  + VSCode supports the edit and run of Jupyter notebooks, it has more features than other Jupyter editors since the extensions from the marketplace (linters, formatters, auto-completion) still function inside Jupyter notebooks.
  + Here is a Jupyter notebook creating and evaluating a model, Pylance (an extension) explains the "add" method of the "keras.models.Sequential" class.
<p align="center">
  <img src="media/jupyter.png" alt="Jupyter Example" width="80%"/>
</p>

+ **Version Control**
  + VSCode has built-in support for Git, it allows you to commit, push, pull, merge branches... directly from the interface.
<p align="center">
  <img src="media/source_control.png" alt="Source Control" width="40%"/>
</p>

+ **LiveShare**
  + VSCode allows you to edit your code with other people in real-time, it's an efficient way to collaborate on a project.
<p align="center">
  <img src="media/liveshare.jpg" alt="LiveShare" width="80%"/>
</p>

## **Installation**

This section will cover the basic installation of VSCode in [*Windows*](#windows), [*Linux*](#linux) and [*Mac*](#mac).

### **Windows**

1. Download the installer from the [VSCode website](https://code.visualstudio.com/download).
2. Launch the installer and follow the instructions.
3. Launch VSCode and follow the customization steps.

### **Linux**

... to be continued

### **Mac**

... to be continued

## **Useful extensions**

Installing extensions is done through the sidebar, click on the "Extensions" icon and search for the extension you want to install.

<p align="center">
  <img src="media/extensions.png" alt="Extensions Menu" width="30%"/>
</p>

Here is a list of useful extensions

+ **Python**
  + This extension adds support for Python to VSCode, it allows you to run, lint and debug Python code. It also adds interface elements to manage Python environments.
  + The extension comes prepackaged with the Pylance and Jupyter extensions which are described below.
  + To use this extension, just create a python file and edit it in VSCode.
  + To choose the Python interpreter, open the command palette (```Ctrl+Shift+P``` on Windows/Linux, ```Cmd+Shift+P``` on Mac) and select ```Python: Select Interpreter```.	

<p align="center">
  <img src="media/debugger.png" alt="Debugger" width="70%"/>
</p>

<p align="center">
  <img src="media/interpreter.png" alt="Interpreters" width="70%"/>
</p>

+ **Jupyter**
  + Adds support for Jupyter notebooks to VSCode, it allows the edit and run Jupyter notebooks.
  + To use this extension, just create a Jupyter notebook (.ipynb) and edit it in VSCode.

<p align="center">
  <img src="media/jupyter_simple.png" alt="Simple Notebook" width="50%"/>
</p>

+ **Pylance**
  + This extension adds support for type checking and auto-completion to VSCode, it is a replacement for the Python extension's IntelliSense engine.
  + Pylance understands what type a variable has and uses this information to do completion, check for errors and provide documentation
  + Pylance is enabled automatically when you edit Python:
    + It will color code text according to type
    + Hover over a variable/function to see its type and documentation
    + ```Ctrl+Click``` or ```Cmd+Click``` on a variable/function to see its source code

<p align="center">
  <img src="media/pylance.png" alt="Pylance" width="80%"/>
</p>

+ **Pylint**
  + This extension installs pylint in VSCode if it is not in your environment, it checks for errors and bad practices in your code.
  + To use this extension, just create a python file and edit it in VSCode, pylint will underline malpractices.
  + For more information (pylint configuration, linting on save): go to this wiki page (ADD LINK)

<p align="center">
  <img src="media/linter.png" alt="Linter Example" width="80%"/>
</p>

+ **Black Formatter**
  + This extension installs Black in VSCode if it is not in your environment, it automatically formats your code to follow a certain standard.
  + To use this extension, open the command palette (```Ctrl+Shift+P``` on Windows/Linux, ```Cmd+Shift+P``` on Mac) and select ```Format Document```.
  + For more information (black configuration, formatting on save): go to this wiki page (ADD LINK)
  + Before/After example:

<p align="center">
  <img src="media/formatting_example.png" alt="Before/After Formatting" width="80%"/>
</p>

+ **Github Copilot** (paid and optional)
  + This extension is a paid subscription based service but its capabilities are well worth the price.
  + Copilot is a code completion tool based on OpenAI Codex and it is extremely powerful.
  + It reads and understands your codebase and often successfully writes docstrings, simple functions and classes.
  + For more information, visit this [*link*](https://github.com/features/copilot).
  + Here is an example output, I only typed the function name and variables, copilot's suggestion is written in grey:

<p align="center">
  <img src="media/copilot.png" alt="Before/After Formatting" width="80%"/>
</p>

... to be continued (LINK THE RELEVANT WIKI PAGES, ADD EXTENSIONS)


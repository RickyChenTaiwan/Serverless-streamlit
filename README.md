# serverless-streamlit
Converting streamlit web app to Executable (Pure Desktop application)

## Objective: how to convert streamlit web app to executable (desktop application).
## Requirements: install node.js, create virtual environment

### Folder structure:

![folder_structure](https://github.com/RickyChenTaiwan/serverless-streamlit/assets/42162312/924b7ffc-34c3-40d5-b16b-4051c2e16546)

### Files explanation:

* package.jsaon: It's a setting file for project. It provides a simplified way to manage a project's dependencies and metadata.

![package](https://github.com/RickyChenTaiwan/serverless-streamlit/assets/42162312/00443754-1285-45a0-80c6-6a3b01c74e0a)

  
* requirements.txt: python packages needed for this project.

![requirements](https://github.com/RickyChenTaiwan/serverless-streamlit/assets/42162312/eaece435-a318-43d4-bbf4-5697a18d5af2)
* streamlit_app.py: streamlit python code.

![streamlit](https://github.com/RickyChenTaiwan/serverless-streamlit/assets/42162312/a8aa8202-cdcb-457e-84ce-6888893cd8b9)

### Here are 4 steps to build executable:
1. **Create package.json and requirements.txt files**
* package.json:
  * stlite: Serverless Streamlit app platform <br />
    * license: Apache-2.0 license <br />
    * version: 0.36.0
  * electron-builder: Build cross-platform desktop apps with JavaScript, HTML, and CSS.
    * license: MIT license
    * version: 24.6.3
* requirements.txt:
  * python packages needed for this project

2. npm install => **create a node_modules directory:**
    * Note: this command installs packages and dependency.
3. npm run dump streamlit_app -- -r requirements.txt => **create a build directory**
    * Note: this command creates ./build directory include streamlit_app directory, site-package-snapshot.tar.gz
4. npm run dist => **create a dist directory**




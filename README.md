# python-venv-guide

## Description

This repository aims to provide an introductory guide for creating Python virtual environments using both `virtualenv` and the `venv` module (included in Python 3.3 and later).

## Introduction

In essence, Python virtual environments allow users to isolate Python installations and associatiated pip packages. This isolation enables the independent installation and management of packages, safeguarding the global environment and base Python installation from conflicts or version mismatches.

## Installation

### Prerequisites

- **Python**: A recent version of Python (*Python 3.x recommended*). Python 3.3 and later versions include the `venv` module, which can be used to create virtual environments without needing an additional package like `virtualenv`.  Check your Python version by running `python --version` in your terminal.

- **pip**: The Python package installer. It usually comes with Python. Verify its installation by running `pip --version` (or `pip3 --version` for Python 3.x).

### Setting up a virtualenv and installing dependencies

1. **Install virtualenv** (Skip this step if you have Python 3.3 or later)

     If using an older version of Python without the `venv` module, install `virtualenv`:

    Open your terminal (Command Prompt on Windows or Terminal on macOS/Linux) and run:
    
   ```bash
   pip install virtualenv
   # Use pip3 for Python 3.x
   ```

2. **Clone the Repository**

   First, clone the repository to your local machine:

   ```bash
   git clone https://github.com/some-username/repository-name.git
   ```

   Navigate to the project directory:

   ```bash
   cd repository-name
   ```
   
3. **Create a Virtual Environment**
    Depending on your Python Version, create a virtual environment in the project directory.

    For installation using `virtualenv`:
   ```bash
   virtualenv venv
   #
   ```

   For installation with Python 3.3 or later using `venv`:

      ```bash
   venv venv
   # Python 3.3 or later
   ```
    
   This command creates a new folder `venv` in your project directory, containing the virtual environment.

4. **Activate the Virtual Environment**

   Before installing dependencies, activate the virtual environment:

   - On Windows:

     ```bash
     venv\Scripts\activate
     ```

   - On macOS and Linux:

     ```bash
     source venv/bin/activate
     ```

   Your command prompt should change to indicate that the virtual environment is activated.
   
5. **Install Project Dependencies**

   Install dependencies from a `requirements.txt` file:

   Given a **.txt** file with relevant dependencies in the following format:

   ```txt
   numpy
   pandas
   matplotlib
   ```

   With the virtual environment activated, install relevant packages from `requirements.txt`:

   ```bash
   pip install -r requirements.txt
   # Use pip3 for Python 3.x
   ```

      **Alternative Methods:**

      <sub>*Not covered in this guide*<sub>
   - **Pipenv**: Use `pipenv install` with a `Pipfile`.
   - **Poetry**: Use `poetry install` with a `pyproject.toml`.
   - **Conda**: Manage dependencies with an `environment.yml` file.

6. **Deactivating the Virtual Environment**

   When you're finished working, you can deactivate the virtual environment:

   ```bash
   deactivate
   ```


## Troubleshooting
 - **Issue**: Venv unable to activate
    - *Solution*: Ensure you are in the correct directory and using the correct command for your OS.
 - **Issue**: `pip` not found
    - *Solution*: Ensure that `pip` is installed, install it if not
 - **Issue**: Errors when installing dependencies.
    - *Solution*: Verify that `requirements.txt` is correctly formatted and all listed packages are available.
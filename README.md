# EDA project - King County House Sales
## Data
This repository contains exploratory data analysis of King County House Sales dataset to come up with several recommendations and insights for our stakeholder. Rhe first notebook [(Fetching_the_data_eda)](1_Fetching_the_data_eda.ipynb) describes how to fetch the data and save it in a csv file. To be able to plot location coordinates on a King Count map, dowload the zip folder `tl_2022_53033_addrfeat` from the [US Census website](https://www2.census.gov/geo/tiger/TIGER2022/ADDRFEAT/).

## Stakeholder
Our stakeholder, Jennifer Montgomery, would like to buy a property and has following requirements:
- High budget,
- wants to show off,
- timing within a month,
- waterfront,
- renovated, 
- high grades,
- resell within 1 year.

## Set up your Environment
This repo contains a requirements.txt file with a list of all the packages and dependencies you will need. Before you install the virtual environment, make sure to install postgresql if you haven't done it before.

 - Check the **postgresql version**  by run the following commands:
    ```sh
    psql --version
    ```
    If you haven't installed it yet, begin at `step_1`. Otherwise, proceed to `step_2`.


Before you can start with plotly in Jupyter Lab you have to install node.js (if you haven't done it before).
- Check **Node version**  by run the following commands:
    ```sh
    node -v
    ```
    If you haven't installed it yet, begin at `step_2`. Otherwise, proceed to `step_3`.


### **`macOS`** type the following commands : 

- `Step_1:` Update Homebrew and install Postgresql by following commands:
    ```sh
    brew update
    brew install postgresql@14
    ```
  Restart Your Terminal and than check the **postgresql version**  by run the following commands:
     ```sh
    psql --version
    ```
  If `psql --version` doesn't display the version, add PostgreSQL to your macOS PATH by following these steps:

  * Find and copy the PostgreSQL bin directory on macOS.
  
    The default path is typically `/Library/PostgreSQL/<version>/bin`, where is your PostgreSQL version.
  * Edit the .zshrc or a similar .conf file using a text editor like Nano, Vim, or VSCode.

     ```sh
    nano ~/.zshrc
    ```
  * Add the following line to the .zshrc file. Make sure to replace <version> with your PostgreSQL version.
    ```sh
    export PATH="/Library/PostgreSQL/<version>/bin:$PATH"
    ```
  * Save and exit the text editor. In nano, you can do this by pressing Ctrl + O, then Enter, and then Ctrl + X to exit.
  * Restart Your Terminal
    ```sh
    source ~/.zshrc
    psql --version
    ```


- `Step_2:` Update Homebrew and install Node by following commands:
    ```sh
    brew update
    brew install node
    ```

- `Step_3:` Install the virtual environment and the required packages by following commands:

    ```BASH
    pyenv local 3.11.3
    python -m venv .venv
    source .venv/bin/activate
    pip install --upgrade pip
    pip install -r requirements.txt
    ```
### **`WindowsOS`** type the following commands :

- `Step_1:` Update Chocolatey and install Postgresql by following commands:
    ```sh
    choco upgrade chocolatey
    choco install postgresql14
    ```
    Restart Your Terminal and than check the **postgresql version**  by run the following commands:
     ```sh
    psql --version
    ```
  If `psql --version` doesn't display the version, add PostgreSQL to your winOS PATH by following these steps:

  * Find and copy the PostgreSQL bin directory on winOS.

    The default path is typically `C:\Program Files\PostgreSQL\<version>\bin`, where <version> is your PostgreSQL version.

  * Open Command Prompt as Administrator:

    * Search for "Command Prompt" in your Start menu.
    * Right-click on "Command Prompt" and select "Run as administrator."

  * Add PostgreSQL to PATH:
    * Replace 14 with your PostgreSQL version if it's different.

    ```PowerShell
    setx PATH "$($env:PATH);C:\Program Files\PostgreSQL\14\bin"
    ```
  * Close the Administrator Command Prompt window.


  * Open a new Terminal and run the following command 
    ```PowerShell
    psql --version
    ```

- `Step_2:` Update Chocolatey and install Node by following commands:
    ```sh
    choco upgrade chocolatey
    choco install nodejs
    ```

- `Step_3:` Install the virtual environment and the required packages by following commands.

   For `PowerShell` CLI :

    ```PowerShell
    python -m venv .venv
    .venv\Scripts\Activate.ps1
    pip install --upgrade pip
    pip install -r requirements.txt
    ```

    For `Git-Bash` CLI :
    ```
    python -m venv .venv
    source .venv/Scripts/activate
    pip install --upgrade pip
    pip install -r requirements.txt
    ```
 

 **`Note:`**
    If you encounter an error when trying to run `pip install --upgrade pip`, try using the following command:

   ```Bash
   python.exe -m pip install --upgrade pip
   ```

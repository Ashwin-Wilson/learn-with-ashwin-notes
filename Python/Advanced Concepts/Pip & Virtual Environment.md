# Pip

## What is `pip`?

- `**pip**` stands for **Preferred Installer Program**.

- It is Python’s **package manager**, used to **install, upgrade, and uninstall external libraries**.

- Think of it as an **app store** for Python packages.

### Common `pip` Commands

|**Command**|**Purpose**|
|---|---|
|`pip --version`|Check pip version|
|`pip list`|List all installed packages|
|`pip install package_name`|Install a package|
|`pip uninstall package_name`|Uninstall a package|
|`pip install --upgrade package_name`|Update a package|

## **Installing a Package**

```bash
pip install requests
```

## Uninstalling a Package

```bash
pip uninstall requests
```

# Virtual Environment

## What is a Virtual Environment?

- A **virtual environment** (venv) is an **isolated workspace** for Python projects.

- It allows you to:
    
    - **Separate dependencies** for different projects.
    
    - Avoid **version conflicts** between libraries.
    
    - Keep your **global Python environment clean**.
    

## Creating a Virtual Environment

Run this command inside your project folder:

```bash
python -m venv myenv
```

`myenv` → Name of the virtual environment folder.

## Activating the Virtual Environment

|**Operating System**|**Command**|
|---|---|
|**Windows (Command Prompt)**|`myenv\Scripts\activate`|
|**Windows (PowerShell)**|`.\myenv\Scripts\Activate.ps1`|
|**Linux / Mac**|`source myenv/bin/activate`|

After activation, you’ll see `(myenv)` before your command prompt, showing that the virtual environment is active.

## Deactivating the Virtual Environment

To deactivate and return to the global Python environment:

```bash
deactivate
```

## Installing Packages Inside venv

Once the venv is active, any installed package will **stay inside that environment only**.

```bash
pip install flask
```

Flask will now be **isolated** to this environment.  

## **Real-World Example**

![[/image 64.png|image 64.png]]

Imagine you are working on **two projects**:

- **Project A** needs **Flask v2.0**

- **Project B** needs **Flask v3.0**

Without a virtual environment:

- Installing Flask v3.0 would **overwrite v2.0**, breaking Project A.

With a virtual environment:

- Create separate environments:

> [!important]
> 
> projectA_env → Flask v2.0
> 
> projectB_env → Flask v3.0

**No conflicts** between projects.
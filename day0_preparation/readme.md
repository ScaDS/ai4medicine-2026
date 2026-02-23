# Prepare Your Computer

Although we will also use computing resources of the University of Leipzig's Computing Center, a lot of the practical work will be done locally on your computer. In this section, you will find information on how to prepare your computer for the training. **Please read everything carefully first and then follow the individual steps.**

## What you need

* Your laptop with internet access
* Administrator rights to install software
* The terminal:
  * **Windows**: CommandPrompt or PowerShell
  * **macOS**/**Linux**: Terminal

## 1. Install and verify Python

* If Python is not already available on your system (see verify step below), install it:  
  https://www.python.org/downloads/ _(version 3.11 or higher)_
* In the Windows installer, make sure that “Add Python to PATH” is checked
* After installation, verify in your terminal (shall display the version):

```bash
python --version
```
* If `python` is not found, try:

```bash
python3 --version
```

## 2. Install uv

* [`uv`](https://docs.astral.sh/uv/) is a fast and convinient tool for Python package and project management
* Install `uv`: https://docs.astral.sh/uv/getting-started/installation/
* After installation, verify in your terminal:

```bash
uv --version
```

## 3. Create a virtual environment (venv)

* Create a folder `ai4medicine`, e.g. on your desktop
* Download the file [`pyproject.toml`](../pyproject.toml), save it in this folder
* Open the terminal and navigate to this folder:

```bash
cd /path/to/ai4medicine
```

* Create a venv using `uv`

```bash
uv sync
```

* This creates a local virtual environment in `ai4medicine/.venv` (hidden folder), installs the Python packages defined in `pyproject.toml`, and finally creates the file `uv.lock`.

## 4. Start JupyterLab from the venv

* As a test, start [JupyterLab](https://jupyter.org/), a web-based interactive development environment for data science that was already installed via `uv` in the venv
* While still in the terminal and in the folder `ai4medicine`:

```bash
uv run jupyter lab
```

* Your browser should now open JupyterLab
* If it doesn't, copy the URL displayed in the terminal into your browser  
  (should start with `http://localhost:8888/lab?token=...`)
* To stop JupyterLab, press in the terminal:

```text
Ctrl + C
```

> **If everything worked: Congratulations! You are done and prepared for the training school.**  
>
> **If you encounter any problems, please reach out via [email](mailto:matthias.taeschner@uni-leipzig.de?subject=AI4Medicine%20School%202026%20Preparation)**

## Download the Files for the Practical Exercise

A few days before the start of the training school, the notebooks and files for the practical exercises will be made available as a ZIP file here:

* [day1_downloads.zip](day1_downloads.zip)
* [day2_downloads.zip](day2_downloads.zip)
* [day3_downloads.zip](day3_downloads.zip)

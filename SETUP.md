# Custom Setup

> [!IMPORTANT]
> **Run all commands from the terminal.**

> [!NOTE]
> On Windows, **All commands must be ran from inside Windows Subsystem**
> **for Linux (WSL)**.
> Once you have WSL installed, you can enable it at any time inside 
> the terminal by executing the command `wsl`.

> [!NOTE]
> These steps require _Git_ to be installed. If your linux distribution does not
> come with Git by default, you must install it first.
> Please see instructions for your linux distribution to find out
> how to install Git.
>
> **You are fine if you are using Ubuntu.**

## Windows Only

### Install Windows Terminal

> [!NOTE]
> You may not need to perform this step on Windows 11!

Follow the instructions here: [https://learn.microsoft.com/en-us/windows/terminal/install](https://learn.microsoft.com/en-us/windows/terminal/install)

### Install Windows Subsystem for Linux

[https://learn.microsoft.com/en-us/windows/wsl/install](https://learn.microsoft.com/en-us/windows/wsl/install)

### Upgrade from WSL 1 to WSL 2

[https://learn.microsoft.com/en-us/windows/wsl/install](https://learn.microsoft.com/en-us/windows/wsl/install)

## Install Miniconda3 (Inside WSL)

Follow the **Linux Installer** instructions here: [https://docs.anaconda.com/free/miniconda/miniconda-install/](https://docs.anaconda.com/free/miniconda/miniconda-install/)

## Clone The Repository (Inside WSL)

Run the following commands (inside WSL):

```sh
git clone https://github.com/farhadfarhadii/llama3
```

```sh
cd llama3
```

## Create a Virtualise Python Environment with Miniconda

> [!NOTE]
> Commands should be run inside the directory of this repository!

Run the following command:

```sh
conda env create -f .environment.yml -p ./.venv
```

## Activate The Virtualised Python Environment

> [!NOTE]
> Commands should be run inside the directory of this repository!

Run the following command:

```sh
conda activate ./.venv
```

You should now see something like `(/.venv) user@host:` in your terminal

> [!NOTE]
> You can deactivate the conda shell by using the following the command:

```sh
conda deactivate
```

## Install Llama3 Dependencies

> [!IMPORTANT]
> Commands should be run inside the directory of this repository!

> [!NOTE]
> Tiktoken may fail to install and complain about a missing Rust compiler.
> If this happens to you, run the command
> `conda install -c conda-forge rust` _while your [conda environment is activated](#activate-the-virtualised-python-environment)_.

Run the following command:

```sh
pip install -e .
```

## Download the Models

Follow the instructions [here](./README.md#download).

## Running the Models

Follow the instructions [here](./README.md#quick-start).

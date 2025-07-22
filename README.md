# ActivitySim User Environment

This repository contains a user environment for ActivitySim, a tool for activity-based 
travel demand modeling. The user environment is designed to be used with the ActivitySim 
core code and provides a set of utilities and configurations to facilitate model 
development and execution.

This repository uses `uv` to manage the user environment, which allows for easy installation and
management of dependencies.


## Installation 

The installation process is straightforward and consists of a few steps.  The steps 
outlined below will set up the user environment for ActivitySim on Windows.

### Step 1: Install UV

ActivitySim uses [`uv`](https://docs.astral.sh/uv/) to manage the user environment,
so users will need to install `uv` on their machines. This should only be needed once 
per machine.

```pwsh
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/0.8.1/install.ps1 | iex"
``` 

It is possible that you will need to restart your terminal after running the above command.
Also, if it has been some time since you installed `uv`, you may want to run the following command to update it:

```pwsh
uv self update
``` 

### Step 2: Clone this Repository

The user does *not* need to clone the ActivitySim core repository itself.  That 
repository is quite large and contains a lot of history.  Instead, this repository
contains the necessary files to set up the user environment, by installing
ActivitySim as a dependency.

To clone this repository, you will need to have `git` installed on your machine,
and/or the GitHub command line tools (i.e., `gh`).

Instructions for installing the `gh` command line tool can be found 
[here](https://github.com/cli/cli?tab=readme-ov-file#windows).

If have `git` or `gh` installed, you can clone this repository by running the following command:

```pwsh
gh repo clone driftlesslabs/asim
```

To clone the repository using `git`, you can run:

```pwsh
git clone https://github.com/driftlesslabs/asim.git
```

### Step 3: Install the User Environment (optional)

Once you have cloned the repository, navigate to the directory where it was cloned:

```pwsh
cd asim
```

Then, run the following command to install the user environment:

```pwsh 
uv sync --locked
```

### Step 4: Run ActivitySim

To run ActivitySim, you can use the `uv` command to run within the environment.
(Note you need to call this command from the directory where you cloned the repository.)

```pwsh 
uv run activitysim
```


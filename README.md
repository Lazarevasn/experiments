# Jupyter setup in DevContainer

Experiments in this repository is assumed to be in Dev Container.

To run dev-container:

1. Clone this repository
    ```bash
    git clone https://github.com/myadryshnikova/jupyter-setup.git
    ```
2. Start the Docker service
3. Open the repository in VSCode
4. Run the Dev Containers: `Open Folder in Container...` command from the Command Palette (F1).


A notification will then appear that the Dev Container has started building. As soon as the build is finished, you can do experiments, the environment for the project is set up.

## Adding dependencies to the environment
This project uses poetry (https://python-poetry.org/) as a package manager. The python packages used can be seen in the `pyproject.toml` file.

To add a dependency: 
```bash 
poetry add <package-name> 
```

You can also directly update `pyproject.toml` by following the example of how other packages are written in it. After that, you need to synchronize it with the `poetry.lock` file using: 
```bash 
poetry lock 
```

If the dependency is not applied to the project after successful installation, you can rebuild the Dev Container.


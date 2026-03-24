# How to use this template

> [!WARNING]
> This file is meant to be deleted once you have populated your repository. It is only there to provide some guidance regarding what you should put where. The usage for each file/folder is described in the sections below.

## README.md

There is already a layout to follow in the `README.md` file. Please add your changes to each section.

## requirements.txt

The `requirements.txt` is there to specify the dependencies you used for your project. 

> [!NOTE]
> There are also dependency management tools that exit, such as Poetry. Poetry is useful to lock all dependencies and make sure that there are not version conflicts. If you decide to use poetry, please read their documentation. In that case, two files will have to be added in the root of your repository: `pyproject.toml` and `poetry.lock`.

## LICENSE

The license that is included in this template is the MIT license. There are tons of licenses. You can change the license by deleting the current file and following [these instructions on the Github Docs](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/adding-a-license-to-a-repository).

## .gitignore

The `.gitignore` file allows you to specify the files that you want git to ignore, meaning that if you are adding or modifying those files in the repository locally, those changes will never be pushed on your remote version. For example, if you create a virtual environment in your repository and called it either `.env`, `.venv`, `env/`, `venv/`, `ENV/`, `env.bak/`, `venv.bak/`, your virtual environment and its content will never be pushed on Github. If you want to call your virtual environment something else (e.g., `my_venv`), you can just add `my_env/` in the `.gitignore` file (see what is listed under `# Environments` in the `.gitignore` file).


> [!NOTE]
> You will notice that there are also `.gitignore` in the `source_data` and `output_data` folders. The reason is that we want to avoid pushing data on Github. Currently different file formats are specified, but add any file formats that are not covered and make sure that the content of those folders are not showing when you do a `git status` in your terminal.


## code/

This folder is used to store your python scripts.

## notebooks/

This folder is used to store all your jupyter notebooks. In general, it is a good to write code for your analyses in python scripts (run linearly) rather than in notebooks (don't run linearly), but notebooks are useful when exploring your data, making figures and sharing tutorials.

## source_data/

The `source_data/` folder is used to store the data used for your analyses.

> [!TIP]
**Bonus point !**  If your dataset is stored in a git repository (through git annex files), you can add it as a submodule in that folder. This will allow you to track the data version that you used for your analyses by specifying the release branch of the dataset repository.


## output_data/

When you generate outputs, please consider using `output_data/` as your output directory.

## slurm_files/

If you are running your analyses on Alliance Canada, you can use that folder to store your bash files and the slurm log files. The content of that folder would not be pushed on Github (please check the file format that are specified in the `.gitignore` file to make sure nothing is forgotten).
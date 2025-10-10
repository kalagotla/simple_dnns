# Simple DNNs
Basics of Deep Neural Networks (DNNs)

# Use the provided setup files to start. If they fail, follow the steps to setup manually below.

### Steps to install and test PyTorch
1. Open anaconda-navigator and run `conda update -n base conda`
2. Download from [GitHub](https://github.com/kalagotla/simple_dnns/tree/main) as a .zip file and extract
3. Navigate to the folder named **simple_dnns-main** in anaconda-navigator
4. Run `conda env create --name torch --file torch.yml` This will install PyTorch in a virtualenv called *torch*
5. Test by running...
 - `conda activate torch`
 - `python test_torch.py`
6. Now that the installation worked. Let's close off by running the following commands, which are used to open torch env in jupyter-notebook
 - `pip install --user ipykernel`
 - `python -m ipykernel install --user --name=torch`
 - `conda deactivate`

### If using a Mac/Linux, you may need to do the following:
Instead of step 4, run the following commands:
 - `conda config --add channels conda-forge`
 - `conda config --set channel_priority strict`
 - `conda env create --name torch --file requirements.txt`

### Models directory
Saved training checkpoints (.tar files) are now stored in the `models/` directory.

- Default save/load filenames in `simple_dnns/univariate.py`, `simple_dnns/bivariate.py`, `simple_dnns/simple_data.py`, and `simple_dnns/noise_data.py` now use `models/...` paths (e.g., `models/1var_model.tar`).
- The `models/*.tar` artifacts are ignored by git via `.gitignore`.
- If you have existing `.tar` files in the project root, move them into `models/`.
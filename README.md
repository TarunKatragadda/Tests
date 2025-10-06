# Tests Project

A lightweight workspace containing Jupyter notebooks for data parsing and ETL experimentation.

## Project Structure

- `etl.ipynb`: Exploratory ETL (extract-transform-load) workflows.
- `parser.ipynb`: Parsing routines and experiments.

## Prerequisites

- Python 3.9+ recommended
- Jupyter (Notebook or Lab)
- Windows PowerShell (commands below use PowerShell)

## Quick Start (Windows PowerShell)

1. Create and activate a virtual environment:
   ```powershell
   python -m venv .venv
   .\.venv\Scripts\Activate
   ```

2. Upgrade `pip` and install Jupyter:
   ```powershell
   python -m pip install --upgrade pip
   pip install jupyterlab
   ```

3. Launch Jupyter Lab and open the notebooks:
   ```powershell
   jupyter lab
   ```
   Alternatively, to use classic Notebook:
   ```powershell
   pip install notebook
   jupyter notebook
   ```

## Working With The Notebooks

- Open `etl.ipynb` or `parser.ipynb` and run cells top-to-bottom.
- If the notebooks depend on local files or environment variables, ensure those are present before execution.
- Use the kernel menu to select the Python environment created in `.venv`.

## Exporting Results

To export a notebook to HTML or a Python script:
```powershell
# HTML
jupyter nbconvert --to html etl.ipynb

# Python script
jupyter nbconvert --to script parser.ipynb
```

## Tips

- Keep datasets outside of version control unless they are tiny and shareable.
- Use separate conda/venv environments per project when possible.
- Consider adding a `requirements.txt` once dependencies stabilize:
  ```powershell
  pip freeze > requirements.txt
  ```
  And to recreate later:
  ```powershell
  pip install -r requirements.txt
  ```

## Troubleshooting

- If Jupyter cannot find the kernel, reinstall `ipykernel` in the active env:
  ```powershell
  pip install ipykernel
  python -m ipykernel install --user --name tests-venv --display-name "Python (tests)"
  ```
- If PowerShell blocks scripts, you may need to adjust execution policy (run as Administrator):
  ```powershell
  Set-ExecutionPolicy -ExecutionPolicy RemoteSigned
  ```

## License

Specify your license here (e.g., MIT). If unsure, keep the repository private until decided.

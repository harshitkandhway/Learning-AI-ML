Here are some commonly used conda commands that can be useful for development:

1. Create a new environment:
   ```
   conda create --name my_env
   ```

2. Create a new environment with a specific version of Python:
   ```
   conda create -n my_env python=3.6
   ```

3. Create a new environment with a specific package:
   ```
   conda create -n my_env numpy
   ```

4. Activate an environment:
   ```
   conda activate my_env
   ```

5. Deactivate the current environment:
   ```
   conda deactivate
   ```

6. List all environments:
   ```
   conda env list
   ```

7. Delete an environment:
   ```
   conda env remove --name my_env
   ```

8. Update a specific package in the current environment:
   ```
   conda update numpy
   ```

9. Update Python in the current environment:
   ```
   conda update python
   ```

10. Install a package:
    ```
    conda install numpy
    ```

11. Remove a package:
    ```
    conda remove numpy
    ```

12. List all packages and their versions in the current environment:
    ```
    conda list
    ```

13. Check conda version:
    ```
    conda --version
    ```

14. Update conda to the latest version:
    ```
    conda update conda
    ```

15. Search for a package in the Anaconda package index and in the conda package index:
    ```
    conda search numpy
    ```

Remember, whenever you create a new environment, don't forget to activate it using `conda activate my_env`. Otherwise, the changes you make will be applied to the base environment. It's always a good practice to create separate environments for different projects to avoid package conflicts.

Complete set of Conda commands can be found from the documentation at below link :
[Conda commands documentation](https://docs.conda.io/projects/conda/en/latest/commands/index.html)

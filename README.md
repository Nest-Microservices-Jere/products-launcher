


## Dev

1. Clone the repository
2. Create an .env based on .env.template
3. Run the `git submodule update --init --recursive` command to rebuild the submodules.
4. Run the command `docker compose up --build`.


### Steps to create Git Submodules

1. Create a new repository on GitHub
2. Clone the repository on the local machine.
3. Add the submodule, where `repository_url` is the url of the repository and `directory_name` is the name of the folder where you want the sub-module to be stored (it must not exist in the project)
```
git submodule add <repository_url> <directory_name>
```
4. Add changes to repository (git add, git commit, git push)
Ex:
```
git add .
git commit -m ‘Add submodule’
git push
```
5. Initialise and update Sub-modules, when someone clones the repository for the first time, they should run the following command to initialise and update the sub-modules
```
git submodule update --init --recursive
```
6. To update the submodule references
```
git submodule update --remote
```


## Important
If working in the repository that has the sub-modules, **first update and push** the sub-module and **then** the main repository. 

If you do it the other way around, you will lose references to the sub-modules in the main repository and will have to resolve conflicts.

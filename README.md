# Jekyll-Data-Science
A Jekyll project template for Data Science

## Project Organization
```
├── Makefile       <- Makefile with commands like `make build-site`.
├── README.md      <- The top-level README for developers using this project.
├── _jupyter
│   ├── notebooks  <- Jupyter notebooks for conversion are stored here.
│   └── templates  <- Where nbconvert templates are stored.
│
├── _layouts       <- Where Jekyll layout templates are stored.
│
├── _posts         <- Where Jekyll markdown posts are stored.
│
├── assets
│   ├── css        <- Where CSS files are stored.
│   └── images     <- Where image files are stored.
│
├── pages          <- Where pages (i.e. non-post files) are stored.
│
└── _config.yml    <- The config file for Jekyll.
```

## Make
Here we will document the different `make` commands defined in the `Makefile`.
All *commands* (excluding the `all` command which is simply executed by
running `make`) are executed by the following format: `make [COMMAND]`. To see
the *contents* of a command that will be executed upon invocation of the
command, simply run `make -n [COMMAND]`.

### Commands
+ `all`: (*aka*: `make`) defaults to converting all UN-converted notebooks
+ `jupyter`: launches the Jupyter notebook development Docker image
+ `execute`: execute all Jupyter notebooks (in place)
+ `convert`: convert all Jupyter notebooks (even if not changed)
+ `sync`: copy all converted files to necessary directories
+ `jekyll`: startup Docker container running Jekyll server
+ `build-site`: build Jekyll static site
+ `pause`: pause PSECS (to pause between commands)
+ `address`: get Docker container address/port
+ `containers`: launch all Docker containers
+ `commit`: git add/commit all synced files
+ `push`: git push to remote branch
+ `publish`: [ *WARNING* ] convert, sync, commit, and push all at once
+ `list-containers`: list all running containers
+ `stop-containers`: simply stops all running Docker containers
+ `restart-containers`: restart all containers
+ `unsync`: remove all synced files
+ `clear-nb`: simply clears Jupyter notebook output
+ `clear-output`: removes all converted files
+ `clear-jekyll`: removes Jekyll _site/ directory
+ `clean`: combines all clearing commands into one
+ `reset`: [ *WARNING* ] reverses all changes prior to `commit` command

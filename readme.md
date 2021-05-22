# AutoSource
AutoSource isa VIM plugin that finds each `.vimrc` file from your `$HOME` directory to the opened file. For example, with the given tree, while editing `myfile`, AutoSource will source the `.vimrc` files in `a/` and `c/`, but not `d/`.
```
.
└── a
    ├── .vimrc
    ├── b
    │   └── c
    │       ├── .vimrc
    │       └── myfile
    └── d
        └── .vimrc
```

## Security
To prevent arbitrary code execution attacks, AutoSource will prompt you to approve new `.vimrc` files and to re-approve those which have changed. This check happens whenever a file is opened.

### WARNING
This plugin has not yet been thoroughly tested and so this feature can not be guaranteed.

## Variables
### `g:autosource_hashdir`
**Default:** `$HOME/.autosource_hashes`
This directory is where AutoSource stores the hashes of your files to check for changes so it can prompt you for re-approval.

## Planned Work
- Add tests
- Add docs

While I do plan on adding these in the near future, this project is not my highest priority. PRs welcome.

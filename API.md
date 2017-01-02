# `midot` API
This section outlines `midot`'s public API,
which can be used internally in your own
dotfiles, as long as your dotfiles are
`midot` compliant.

## General
- `rm_dir`: Removes a directory with debug messages
```sh
rm_dir ~/.directory_i_want_to_remove
```

- `symlink_all`: Symlinks all files ending with `.symlink`
	- Contains an optional argument: max_depth: Maximum number of nested directories it will search, no arg defaults to 3
```sh
symlink_all # Symlinks everything, using a default max depth of 3
symlink_all 5 # Symlinks everything, using a passed in max depth of 5
```

## Git
- `set_git`: Sets a `git` configuration key-value pair
```sh
set_git user.name "Your Name Here"
set_git user.email "Your email here"
set_git push.default simple
set_git color.ui auto
set_git core.editor "Your favourite terminal editor here"
```

## Pretty debug messages
- `info`
```sh
info "YOUR MESSAGE ABOUT PASSING A CHECKPOINT HERE"
```

- `user`
```sh
user "YOUR PROMPT TO RECEIVE USER INPUT HERE"
```

- `success`
```sh
success "YOUR SUCCESSFUL COMPLETION MESSAGE HERE"
```

- `warn`
```sh
warn "YOUR WARNING ABOUT A NON-FATAL ERROR HERE"
```

- `fail`
```sh
fail "YOUR MESSAGE ABOUT A FATAL ERROR HERE"
```

## NOTE
This API file listing will attempt to be updated
to be as close to the current API as possible.
When in doubt on whether one of `midot`'s functions
are available, use `midot api` as the singular source
of truth.

# MWE reproducing jekyll issue

This is a repository designed to reproduce the issue in [jekyll/jekyll#6295](https://github.com/jekyll/jekyll/issues/6295).

To reproduce, clone this repository and run `jekyll serve -w`. Confirmed with version 3.8.3.

```bash
$ jekyll --version
jekyll 3.8.3
$ jekyll serve -w
Configuration file: /tmp/jekyll-symlink-mwe/_config.yml
            Source: /tmp/jekyll-symlink-mwe
       Destination: /tmp/jekyll-symlink-mwe/_site
 Incremental build: disabled. Enable with --incremental
      Generating... 
                    done in 0.049 seconds.
 Auto-regeneration: enabled for '/tmp/jekyll-symlink-mwe'
    Server address: http://127.0.0.1:4000/
  Server running... press ctrl-c to stop.
        ** ERROR: directory is already being watched! **

        Directory: /tmp/jekyll-symlink-mwe/exclude_this_dir/_layouts

        is already being watched through: /tmp/jekyll-symlink-mwe/exclude_this_dir/_layouts

        MORE INFO: https://github.com/guard/listen/wiki/Duplicate-directory-errors
```


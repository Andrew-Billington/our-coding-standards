# Some tips on making your analyses simple to reproduce

## Include a git hash

If practical, the output of your code should include the git hash
of the code that produced it. By doing so, the analysis should be
more reproducible, there is no ambiguity about the specific code 
that was used to generate it.

### R
You can access the git hash using either of the following code:
snippets.
```{r}
library(git2r)

repo <- repository(".")
print(head(repo))
```

or

```{r}
print(system("git rev-parse --short HEAD", intern = TRUE))
```

### Python
You can access the git hash using the following code:
```import subprocess

def get_git_revision_hash():
    return subprocess.check_output(['git', 'rev-parse', 'HEAD'])

def get_git_revision_short_hash():
    return subprocess.check_output(['git', 'rev-parse', '--short', 'HEAD'])```

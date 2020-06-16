# GitHub and GitLab pages

There are two types of GitHub/GitLab pages:
1. User or Group pages `https://user-name.git{hub|lab}.io`.
2. Project pages `https://username.git{hub|lab}.io/project-name`.

These two types of GitHub/GitLab pages have diffrent settings of urls when we generate the static sites with `Jekyll`:
1. Default configuration.
2. Configure the url as
```
url: https://username.gitlab.io
baseurl: /project-name
```

In each type, GitHub and GitLab also handles things differently.

GitLab:
* For `type 1` and `type 2` the files are put into a sub folder, e.g. `public`, and `CI` need to be configured.

Github:
* For `type 1` the files are put into the project and all are set.
* For `type 2` the files are put into the `docs` sub-folder.

The established work flow is as follows:
1. Edit and build in `jekyll_site-name`
2. Copy the output contents into corresponding git the repository

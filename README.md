# Dyne.org theme for software webpages made in mkdocs

For information about the base system see https://mkdocs.org

This theme uses [Bulma](bulma.io) and provides basic styling for our projects.

## Usage

Usage requires mkdocs (python) and zsh: `apt install mkdocs`.

Step by step notes on basic usage scenarios follow: initialize, update and deploy.

### Initialize

1. make a `web` directory in your project and enter it

2. clone this repo

```
git clone https://github.com/dyne/mkdocs-dyne-theme
```

3. run `./mkdocs-dyne-theme/init`

4. edit the configuration file `mkdocs.yml` with the right project settings

5. edit the contents in `docs/index.md` or symlink to README.md

### Update the theme

Run `./mkdocs-dyne-theme/update` to actualize the theme to its latest version.

Commit the changes to your project.

Keep in mind that this theme is not a submodule of your project, it is copied inside it.

### Deploy the webpage

Run `./mkdocs-dyne-theme/deploy` to create a branch `gh-pages` and upload the page.

Go to https://dyne.github.io/project-name to see it.

Contact a sysadmin to setup project-name.dyne.org.



## Configuration

Example configuration:
```yml
site_name: RedRoom
site_url: https://decodeproject.github.io/RedRoom
repo_url: https://github.com/decodeproject/redroom
site_author: Jaromil
site_description: RedRoom is powered by the Zenroom crypto VM to bring easy to use yet advanced cryptographic functionalities for Redis.
copyright: Copyright (C) 2019 by the <a href="https://dyne.org">Dyne.org foundation</a>. The source code is licensed <a href="https://www.gnu.org/licenses/agpl-3.0.en.html">AGPLv3</a>.

plugins: []

extra_css:
  - //fonts.googleapis.com/css?family=Montserrat&display=swap
  - css/custom.css

markdown_extensions:
  - admonition
  - codehilite

theme:
  name: null
  custom_dir: 'mkdocs-dyne-theme/'

extra:
  links:
    releases: https://files.dyne.org/redroom
    docker: https://hub.docker.com/r/dyne/redroom
	quickstart: https://github.com/decodeproject/redroom/wiki
	forum: https://lists.dyne.org
  drift_handle: s64nd7w43g53
  nav:
    subtitle: Redis powered by Zenroom
    logo: null # /img/redroom-trans.png
    og_image_large: /img/redroom-trans.png
```
 
## Acknowledgement
 
This plugin is licensed AGPLv3.

It is maintained by @jaromil and @puria

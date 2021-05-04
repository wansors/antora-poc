# antora-poc
Antora ProofOfConcept


# Install Antora on Ubuntu WSL
sudo apt-get update
sudo apt-get install nodejs npm
echo "PATH=\"$HOME/bin:$HOME/.local/bin:/usr/bin:$PATH\" >> ~/.profile
source ~/.profile
npm i -g @antora/cli@2.0 @antora/site-generator-default@2.0








# About Antora
https://matthewsetter.com/antora/three-core-concepts/
## The Playbook
The Playbook, stored in a YAML, JSON, or CSON file in the root directory of an Antora project, is what brings everything together. It contains such essential details as:

* The information that globally applies to the site, such as its title and base URL.
* The content sources (components) to use. These sources are git repositories (multiple branches and tags are supported).
* The theme to use.
* Where the site will be dateed (on the local filesystem, remotely, such as on Netlify or Amazon S3).
* Caching;
* and much more

## Two: The Component
Antora stores the source files and static assets that it uses to generate its content in what it refers to as components. What’s particularly interesting about them, is that they’re composed of one or more modules, where each module is a logical (as much as possible) grouping of content.

Each module stores a combination of AsciiDoc source files, static asset files (JavaScript and CSS files), and other supporting content, such as code examples.

## Three: The UI Theme
Antora Playbooks don’t directly integrate the documentation’s theme, instead choosing to use a separate UI theme. This can be stored locally or remotely and manages the look and feel of the generated documentation.
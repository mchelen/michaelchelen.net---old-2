# Git Wiki Gollum Smeagol
Git is a revision control system. Gollum is a webserver to work with the repository locally. Smeagol is webserver to publically display the repository pages.



Gem install sudo is optional for system-wide install.


```bash
#!/bin/bash

## Prerequisites

### enable universe repository

sudo vi /etc/apt/sources.list

sudo apt-get update

### install dependencies
sudo apt-get install ruby rubygems ruby-dev libxml2-dev libxslt-dev


## Install Gollum or Smeagol
### smeagol is selected by default

# sudo gem install gollum --no-ri --no-rdoc

sudo gem install smeagol --no-ri --no-rdoc


### Markdown support

sudo gem install rdiscount


### Syntax highlighting

sudo apt-get install python-pygments

## Update PATH
echo "export PATH=$PATH:/var/lib/gems/1.8/bin" >> ~/.bashrc

## Load your updated .bashrc
source ~/.bashrc



## Clone Wiki repository
### Public Git URL
git clone git://github.com/mchelen/michaelchelennet.wiki.git



## Start Gollum
### Change to the directory with the Git repo and start repo.
cd michaelchelennet.wiki
gollum

```




## GitHub wikis can be branched and merged
 - Not supported by web interface






## Install Smeagol
Smeagol
https://github.com/benbjohnson/smeagol
```
sudo gem install smeagol
```

Smeagol supports multiple repositories


## Why Markdown?
Markdown is easier to read and write than HTML


### Hello World
- Bar1

```html
<html>
  <body>
    <h3>Hello World</h1>
    <li>
      <ul>Bar1</ul>
    </li>
  </body>
</html>
```

```markdown
### Hello World
- Bar1
```


## Sources

- http://johanharjono.com/archives/791
- https://github.com/github/gollum
- http://github.github.com/github-flavored-markdown/
- https://github.com/sononum/gollum/wiki/Installation-on-Ubuntu

# Git Wiki Gollum Smeagol
Git is a revision control system. Gollum is a webserver to work with the repository locally. Smeagol is webserver to publically display the repository pages.



Gem install sudo is optional for system-wide install.


## Prerequisites
### enable universe repository
```bash
sudo cp /etc/apt/sources.list /etc/apt/sources.list.bak
sudo sed -i -e "s/# deb/deb/g" /etc/apt/sources.list
```
### install dependencies
```bash
sudo apt-get update
sudo apt-get -y install ruby rubygems ruby-dev libxml2-dev libxslt-dev
```

## Install Gollum and/or Smeagol
```bash
sudo gem install gollum --no-ri --no-rdoc

sudo gem install smeagol --no-ri --no-rdoc
```

### Markdown support
```bash
sudo gem install rdiscount
```

### Syntax highlighting
```bash
sudo apt-get install python-pygments
```

## Update PATH and reload .bashrc
```bash
echo "export PATH=$PATH:/var/lib/gems/1.8/bin" >> ~/.bashrc
source ~/.bashrc
```

## Clone Wiki repository
### Public Git URL
```bash
git clone git://github.com/mchelen/michaelchelennet.wiki.git
```


## Start Gollum
### Change to the directory with the Git repo and start repo.
```bash
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

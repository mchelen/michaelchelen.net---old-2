# Git Wiki Gollum Smeagol
Git is a revision control system. Gollum is a webserver to work with the repository locally. Smeagol is webserver to publically display the repository pages.

## Clone Wiki repository

Optional sudo gem install system-wide


```
git clone git@github.com:mchelen/michaelchelennet.wiki.git

```

```
git clone git://github.com/mchelen/michaelchelennet.wiki.git
```

## Install Gollum


```
sudo gem install gollum
```

enable universe repository

```
sudo vi /etc/apt/sources.list
```

```
sudo apt-get update
```

```
sudo apt-get install ruby rubygems ruby-dev libxml2-dev libxslt-dev
```

```
sudo gem install gollum --no-ri --no-rdoc
```


Markdown support
```
sudo gem install rdiscount
```

Syntax highlighting
```
sudo apt-get install python-pygments
```

## Update your PATH
echo "export PATH=$PATH:/var/lib/gems/1.8/bin" >> ~/.bashrc

## Load your updated .bashrc
source ~/.bashrc




## Start Gollum
Change to the directory with the Git repo and start repo.
```
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

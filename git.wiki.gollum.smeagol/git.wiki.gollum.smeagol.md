# Git Wiki Gollum Smeagol
Git is a revision control system. Gollum is a webserver to work with the repository locally. Smeagol is webserver to publically display the repository pages.

## Clone Wiki repository


```
git clone git@github.com:mchelen/michaelchelennet.wiki.git

```

```
git clone git://github.com/mchelen/michaelchelennet.wiki.git
```

## Install Gollum


```
gem install gollum
```

enable universe repository

```
vi /etc/apt/sources.list
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
Optional sudo


Markdown support
```
sudo gem install rdiscount
```

Syntax highlighting
```
sudo apt-get install python-pygments
```




GitHub wikis can be branched and merged
 - Not supported by web interface

# Install Smeagol
Smeagol
https://github.com/benbjohnson/smeagol
```
sudo gem install smeagol
```
Optional sudo

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

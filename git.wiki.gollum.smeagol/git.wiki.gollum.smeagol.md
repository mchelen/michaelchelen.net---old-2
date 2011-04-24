# Git Wiki Gollum Smeagol


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

### Hello World
- Foo
- Bar



```html
<html>
  <body>
    <h3>Hello World</h1>
    <li>
      <ul>Foo</ul>
      <ul>Bar</ul>
    </li>
  </body>
</html>
```

```md
### Hello World
- Foo
- Bar
```


## Sources

- http://johanharjono.com/archives/791
- https://github.com/github/gollum
- http://github.github.com/github-flavored-markdown/

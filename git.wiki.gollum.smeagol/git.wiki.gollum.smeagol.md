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
 not supported by web interface


Smeagol
https://github.com/benbjohnson/smeagol
```
sudo gem install smeagol
```
Optional sudo


Sources:

http://johanharjono.com/archives/791
https://github.com/github/gollum

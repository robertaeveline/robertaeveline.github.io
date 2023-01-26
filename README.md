Evelyn
==

## Getting Started

### Dependencies

* Ruby 2.6 (gh dependency/forestry.io)

```
$ bundle install
```

### Development

```
$ bundle exec jekyll serve --config _config.yml,_config_development.yml --drafts --unpublished --future -d _site
```

### Domain

https://stackoverflow.com/questions/54059217/how-to-fix-domain-does-not-resolve-to-the-github-pages-server-error-in-github

```
CNAME file with the website name (with www):

www.example.com

On my domain registration's DNS :

www                     28800  CNAME  MYUSERNAME.github.io.
@                       21460  A      185.199.111.153
@                       21460  A      185.199.109.153
@                       21460  A      185.199.110.153
@                       21460  A      185.199.108.153


$dig WWW.example.com +nostats +nocomments +nocmd

;WWW.example.com.   IN  A
WWW.example.com.    26728 IN CNAME  MYUSERNAME.github.io.
MYUSERNAME.github.io.   1527    IN  A   185.199.108.153
MYUSERNAME.github.io.   1527    IN  A   185.199.111.153
MYUSERNAME.github.io.   1527    IN  A   185.199.110.153
MYUSERNAME.github.io.   1527    IN  A   185.199.109.153

Tick the "Enforce HTTPS".

Note: Replace example.com and MYUSERNAME by the values relevant to you.
```

### Deploy

```
git push origin production
```

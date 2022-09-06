---
layout: post
title:  "How to install Jekyll on Ubuntu"
date:   2022-09-06 10:06:19 +0200
categories: jekyll linux
---
I use the Ubuntu 22.04 LTS flavor running in a WSL environment.

Install distro packages
```
sudo apt install ruby-full build-essential zlib1g-dev
```

Allow ruby gems to be installed in user context
```
echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc  
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc 
source ~/.bashrc
```

Install ruby gems
```
gem install jekyll bundler
```

Now the jekyll cli is available
```
jekyll new .
```



\
\
Links:
[Jekyll docs][jekyll-docs]


[jekyll-docs]: https://jekyllrb.com/docs/home
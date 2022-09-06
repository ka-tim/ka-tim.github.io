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

Links:
[Jekyll docs][jekyll-docs]


You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

Jekyll requires blog post files to be named according to the following format:

`YEAR-MONTH-DAY-title.MARKUP`

Where `YEAR` is a four-digit number, `MONTH` and `DAY` are both two-digit numbers, and `MARKUP` is the file extension representing the format used in the file. After that, include the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/

# Install Jekyll

Follow [the installation guide](https://jekyllrb.com/docs/installation/macos/). 

Though I followed it, I had a couple of errors.

### libsass

    Could not open library libsass.bundle no suitable image found

I had to reinstall it with `--user-install` option

    gem uninstall sassc
    gem install sassc --user-install

What is `--user-install`

> When you use the --user-install option, RubyGems will install the gems to a directory inside your home directory, something like ~/.gem/ruby/1.9.1. The commands provided by the gems you installed will end up in ~/.gem/ruby/1.9.1/bin. For the programs installed there to be available for you, you need to add ~/.gem/ruby/1.9.1/bin to your PATH environment variable.

from https://guides.rubygems.org/faqs/#i-installed-gems-with---user-install-and-their-commands-are-not-available

### webrick

ruby 3 [doesn't come with webrick any more](https://github.com/jekyll/jekyll/issues/8523). 

    jekyll cannot load such file -- webrick

So, install webrick additionally

    bundle add webrick

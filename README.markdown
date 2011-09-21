# Gem in a Box

![screen shot](http://i50.tinypic.com/2yknxnr.png)

## Really simple rubygem hosting

Gem in a box is a simple [sinatra][sinatra] app to allow you to host your own in-house gems.

## Authentication

It can do the http basic authentication.
Which you just need set two env variables as the username and passowrd like:

    export GEMINABOX_USERNAME="poshboytl"
    export GEMINABOX_PASSWORD="111111"

## Server Setup

    gem install geminabox

Create a config.ru as follows:

    require "rubygems"
    require "geminabox"

    Geminabox.data = "/var/geminabox-data" # …or wherever
    run Geminabox

And finally, hook up the config.ru as you normally would ([passenger][passenger], [thin][thin], [unicorn][unicorn], whatever floats your boat).


## Client Usage

    gem install geminabox

    gem inabox pkg/my-awesome-gem-1.0.gem

Simples!

## Licence

Fork it, mod it, choose it, use it, make it better. All under the [do what the fuck you want to + beer/pizza public license][WTFBPPL].

[WTFBPPL]: http://tomlea.co.uk/WTFBPPL.txt
[sinatra]: http://www.sinatrarb.com/
[passenger]: http://www.modrails.com/
[thin]: http://code.macournoyer.com/thin/
[unicorn]: http://unicorn.bogomips.org/

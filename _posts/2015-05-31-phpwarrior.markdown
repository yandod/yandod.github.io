---
layout: post
title:  "introducing php port of RubyWarrior #phpwarrior"
date:   2015-05-31 12:00:00 +9:00
categories: note
---

[yandod/php-warrior](https://github.com/yandod/php-warrior)

I love "[ruby-warrior](https://github.com/ryanb/ruby-warrior/)" which is ruby based coding game.
Both [web version by bloc](https://www.bloc.io/ruby-warrior/#/) and, original gem version are awesome work.

Also I found [python-warrior](https://github.com/arbylee/python-warrior).
That inspired me to implement RubyWarrior into PHP.


The game is commding warrior to crime the 2 type of towers.
both 2 towers include 19floors are now available to hack in PHP.

<iframe width="560" height="315" src="https://www.youtube.com/embed/Pt_qerDO28c" frameborder="0" allowfullscreen></iframe>

In ruby, typical code of warrior look like this:

    class Player
      def play_turn(warrior)
        # cool code goes here
        if warrior.feel.enemy?
          warrior.attack!
        else
          warrior.walk!
        end
      end
    end

In PHP, the code turn to like this player.php.
the nuance of ! is lost now. (python warrior is using _ insteand of !)

    <?php
    class Player {

      public function play_turn($warrior) {
      # add your code here
        if ($warrior->feel()->is_captive()) {
          $warrior->rescue();
        } else {
          $warrior->attack();
        }
      }
    }

it tested with even PHP7 on TravisCI, it is available on packagist.
to start game, install via composer.

    composer global require "yandod/php-warrior=*"
    export PATH=$HOME/.composer/vendor/bin:$PATH

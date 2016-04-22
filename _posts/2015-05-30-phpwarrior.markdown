---
layout: post
title:  "RubyWarriorをPHPに移植した #phpwarrior"
date:   2015-05-30 12:00:00 +9:00
categories: blog
---

Rubyで作られたRubyWarriorというゲームをPHPに移植しました。

<iframe src="https://ghbtns.com/github-btn.html?user=yandod&repo=php-warrior&type=star&count=true&size=large" frameborder="0" scrolling="0" width="160" height="30"></iframe>

[yandod/php-warrior](https://github.com/yandod/php-warrior)

Rubyで実装して２つの塔を攻略していくゲームですが、晴れてPHPでも攻略できるようになりました。
初心者モードと中級者モードに9面づつ、最後までクリアすると同じコードで最初から最後までプレイするepicモードが始まります。

<iframe width="560" height="315" src="https://www.youtube.com/embed/Pt_qerDO28c" frameborder="0" allowfullscreen></iframe>

RubyWarriorの場合、プレイヤーの動きを実装するplayer.rbは次のような形です。

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

一方、PHPでは戦士の挙動を実装するplayer.phpは次のようになりました。
Rubyの!ニュアンスが失われているのがやや心残りですが、ひとまずひと通りのステージクリアできるのは確認できました。

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

ちなみにPython移植版の場合は!を_に変えて移植していました。

[arbylee/python-warrior](https://github.com/arbylee/python-warrior)

TravisCIを使ってPHP7での動作も確認しましたが、気軽に遊んでもらえると嬉しいです。
インストールはcomposerから可能です。

    composer global require "yandod/php-warrior=*"
    export PATH=$HOME/.composer/vendor/bin:$PATH

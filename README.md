## このソフトウェアについて
このソフトウェアは<a href="https://github.com/NewEraCracker/LOIC/">オープンソースで開発されているLOIC</a>を日本語に翻訳したものです。
現在、本体の使用には対応していますが、IRCなどの機能は使うことができません。
また、このソフトウェアを悪用した場合、刑事罰の対象となることをご承知おき下さい


## Information
Low Orbit Ion Cannon(LOIC)はオープンソースのネットワーク負荷試験ツールです。
このソフトはPraetox's loic projectが<a href="https://sourceforge.net/projects/loic/">作られたもの</a>がベースとなっています。
またこのソフトウェアはC#で作られています。

## 免責事項
製作者はこのソフトウェアを使用したことによって発生した問題について一切の責任を取りません。
このソフトウェアを使用して、**他人のサーバ**へ攻撃を行った場合、使用者は刑事罰の対象となります。
このソフトウェアは研究用に公開されているものです。悪用は絶対にしないでください。

## Windowsでの実行方法

LOIC.exeを実行してください

このソフトにはMicrosoft .NET Framework 3.5 Service Pack 1が必要です ダウンロードはこちら:
http://www.microsoft.com/downloads/en/details.aspx?FamilyID=ab99342f-5d1a-413d-8319-81da479ab0d7&displaylang=en

## HOW TO RUN ON LINUX / MACOSX

Run debug binaries with mono.
Read the wiki at https://github.com/NewEraCracker/LOIC/wiki/ for updated instructions.

## HIVEMIND/HIDDEN MODE

HIVEMIND mode will connect your client to an IRC server so it can be controlled remotely.
Think of this as a voluntary botnet (though do beware that your client can potentially be
made to do naughty things).

Note: It does NOT allow remote administration of your machine, or anything like that; it
is literally just control of loic itself.

If you want to start up in Hivemind mode, run something like this:
```
 LOIC.exe /hivemind irc.server.address
```
It will connect to irc://irc.server.adress:6667/loic

You can also specify a port and channel:
```
 LOIC.exe /hivemind irc.server.address 1234 #secret
```
It will connect to irc://irc.server.adress:1234/secret

In order to do Hivemind Hidden mode, run something like this:
```
 LOIC.exe /hidden /hivemind irc.server.address
```
It will connect to irc://irc.server.adress:6667/loic without any visible GUI.

## CONTROLLING LOIC FROM IRC

As an OP, Admin or Owner, set the channel topic or send a message like the following:
```
 !lazor targetip=127.0.0.1 message=test_test port=80 method=tcp wait=false random=true
```

To start an attack, type:
```
 !lazor start
```

Or just append "start" to the END of the topic:
```
 !lazor targetip=127.0.0.1 message=test_test port=80 method=tcp wait=false random=true start
```

To reset loic's options back to its defaults:
```
 !lazor default
```

To stop an attack:
```
 !lazor stop
```

and be sure to remove "start" from the END of the topic, if it exists, too.

Take a look at source code for more details.

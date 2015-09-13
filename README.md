# 概要
SpringSessionの動作確認用の環境を、構築するためのAnsibleスクリプトです。

セッションサーバにはRedisを、APサーバには、Tomcatとサンプルプロジェクトをインストールします。
サンプルプロジェクトは、SpringSessionの「httpisession-xml」を動かします。

# 動作環境
* Ansible 1.9+
* Vagrant 1.7.2+
* Parallels Desktop 10+ & Vagrant Parallels Provider

# 動かし方

```sh
$ vagrant ssh-config > ssh.config
$ vagrant up
$ ansible-playbook -i host session_server.yml
$ ansible-playbook -i ap_server.yml
```

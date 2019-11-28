# answered-issues

- ruby envでrubyのバージョンが切り替わらない時

```
vagrant@ubuntu-bionic:/vagrant/final-cdeeen$ rbenv local 2.5.7
vagrant@ubuntu-bionic:/vagrant/final-cdeeen$ ruby -v
ruby 2.6.5p114 (2019-10-01 revision 67812) [x86_64-linux]
```

rbenv localでバージョンをしたが、ruby -v でバージョンを確認すると、変更がされていない。

→rbenv initをして、"$(rbenv init -)"をする

```
vagrant@ubuntu-bionic:/vagrant/final-cdeeen$ rbenv init
# Load rbenv automatically by appending
# the following to ~/.bashrc:

eval "$(rbenv init -)"

vagrant@ubuntu-bionic:/vagrant/final-cdeeen$ eval "$(rbenv init -)"
vagrant@ubuntu-bionic:/vagrant/final-cdeeen$ ruby -v
ruby 2.5.7p206 (2019-10-01 revision 67816) [x86_64-linux]

```
→解決！

# 1. Суммарное число комитов, которые меняли файл Gemfile?

```bash
ak@ak-pc:~/Dropbox/otus/03-lesson-git/zabbixapi$ git log --pretty=oneline Gemfile | wc -l
8
```

**Ответ**: `8`

# 2. Напишите дату когда, Gemfile был добавлен в репозиторий.

```bash
ak@ak-pc:~/Dropbox/otus/03-lesson-git/zabbixapi$ git log --diff-filter=A Gemfile
commit 8976bf8a44043b9a8a119ea99dd89f000e8c81cd
Author: Dmitry Vasiliev <vadv.mkn@gmail.com>
Date:   Wed Oct 10 00:47:52 2012 +0400

    spec for travis-ci
```

**Ответ**: `Wed Oct 10 00:47:52 2012`

# 3. Какой пользователь в последний раз менял строки функции def proxies в файле lib/zabbixapi.rb?

```bash
ak@ak-pc:~/Dropbox/otus/03-lesson-git/zabbixapi$ git blame -L '/def proxies/' lib/zabbixapi.rb
336e8c24 (Pavel Tsaregorodtsev 2013-12-04 12:36:55 +0400 115)   def proxies
336e8c24 (Pavel Tsaregorodtsev 2013-12-04 12:36:55 +0400 116)     @proxies ||= Proxies.new(@client)
336e8c24 (Pavel Tsaregorodtsev 2013-12-04 12:36:55 +0400 117)   end

ak@ak-pc:~/Dropbox/otus/03-lesson-git/zabbixapi$ git show 336e8c24
```

**Ответ**: `Pavel Tsaregorodtsev`

# 4. Напишите хеш комита (необязательно полностью),который имеет сообщение “Add Ruby 2.2 support”.
*Плюсом будет, если предоставите ссылку на
страницу GitHub данного комита.*

```bash
ak@ak-pc:~/Dropbox/otus/03-lesson-git/zabbixapi$ git log --pretty=format:%h --grep='Add Ruby 2.2 support'
3b128fa
```

**Ответ**: `3b128fa` и `https://github.com/express42/zabbixapi/commit/3b128fa1c6b96c9be4aed5b2bcf777537d752c5e`

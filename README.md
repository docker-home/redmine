# redmine

- add themes
- support crontab

```
From redmine:4.0.3
MAINTAINER wuyue92tree@163.com

COPY ./themes /usr/src/redmine/public/themes/

RUN apt-get update && apt-get install cron -y

CMD ['/etc/init.d/cron', 'restart']

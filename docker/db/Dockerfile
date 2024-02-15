FROM postgres:16.2

RUN localedef -i ja_JP -c -f UTF-8 -A /usr/share/locale/locale.alias ja_JP.UTF-8

ENV TZ Asia/Tokyo

ENV LANG ja_JP.utf8
ENV LANGUAGE ja_JP:ja
ENV LC_ALL ja_JP.UTF-8
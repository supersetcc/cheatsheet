# DevOps Workspace

## Log rotate - rotates, compresses, and mails system logs
- `sudo vim /etc/logrotate.d/nginx`에서 nginx log를 logroate로 관리
- `logrotate -d -f /etc/logrotate.d/nginx`로 테스트 가능 (`-d`는 dryrun, `-f`는 size나 daily 같은 조건 관계 없이 force logrotate)

## crontab
- `grep CRON /var/log/syslog`로 cronjob log 확인
- `crontab -e` 기본 에디터를 vim으로 바꾸고 싶다면 `export EDITOR=/usr/bin/vim`

## linux
- `uname -a`: 리눅스 버전 확인

## Nginx
- The `sites-available` folder is for storing all of your vhost configurations, whether or not they're currently enabled.
- The `sites-enabled` folder contains symlinks to files in the sites-available folder. This allows you to selectively disable vhosts by removing the symlink.
- `/etc/nginx/nginx.conf`
- `nginx -s [stop | quit | reload | reopen]`
    - stop — fast shutdown
    - quit — graceful shutdown
    - reload — reloading the configuration file
    - reopen — reopening the log files

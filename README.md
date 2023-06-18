# Install

install docker then clone this repo and run this command:
```
docker-compose up -d
```

then run this one and don't forget to change the user and password with urs:
```
docker run --rm -e MAIL_USER=islam@docker.local -e MAIL_PASS=supersecret -it mailserver/docker-mailserver /bin/sh -c 'echo "$MAIL_USER|$(doveadm pw -s SHA512-CRYPT -u $MAIL_USER -p $MAIL_PASS)"' >> ~/docker/mailserver/config/postfix-accounts.cf
```
enjoy :)

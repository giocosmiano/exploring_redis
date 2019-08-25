- [Redis - open source, in-memory data structure store, used as a database, cache and message broker](https://redis.io/)
  - [Quick Start](https://redis.io/topics/quickstart)
  - [Documentation](https://redis.io/documentation)
  - [How To Install and Secure Redis on Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/how-to-install-and-secure-redis-on-ubuntu-18-04)

- Installing `redis` in `Ubuntu 18.04 x64`
  - make sure to run `make`

```bash
   $ wget http://download.redis.io/redis-stable.tar.gz
   $ tar xvzf redis-stable.tar.gz
   $ cd redis-stable
   $ make
```

- Add these settings to `.bashrc` for personal preference

```bash
   export APPLICATIONS_HOME="${HOME}/Documents/_applications"
   export REDIS_HOME="${APPLICATIONS_HOME}/redis-5.0.5"
   export REDIS_BIN="${REDIS_HOME}/src"

   alias redis-server='cd ${REDIS_BIN}; ./redis-server'
   alias redis-cli='cd ${REDIS_BIN}; ./redis-cli'

   alias redis-restart='sudo systemctl restart redis.service'
   alias redis-start='sudo systemctl start redis.service'
   alias redis-stop='sudo systemctl stop redis.service'
   alias redis-status='sudo systemctl status redis.service'
   alias redis-enable='sudo systemctl enable redis.service'
   alias redis-disable='sudo systemctl disable redis.service'
```

- Configure to start `redis` automatically with the server

```bash
   $ sudo cp redis.service /etc/systemd/system
```

- Update the `systemd` service after copying `redis` services 

```bash
   $ sudo systemctl daemon-reload
```

- Enable to auto-start `redis` service

```bash
   $ redis-enable
```

- Start/Re-Start `redis` service

```bash
   $ redis-start
   $ redis-restart
```

- Check `redis` version

```bash
   $ redis-server --version
```

- Installing `Redis Desktop Manager` UI
  - [Redis Desktop Manager](https://redisdesktop.com/)
  - [Install RedisDesktopManager using `Snapcraft` in Ubuntu](https://snapcraft.io/redis-desktop-manager)
  - [Redis Desktop Manager Quick Install](http://docs.redisdesktop.com/en/latest/install/)


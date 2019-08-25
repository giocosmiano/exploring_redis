- [Redis - open source, in-memory data structure store, used as a database, cache and message broker](https://redis.io/)
  - [Quick Start](https://redis.io/topics/quickstart)
  - [Documentation](https://redis.io/documentation)
  - [How To Install and Secure Redis on Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/how-to-install-and-secure-redis-on-ubuntu-18-04)

- Installing `redis` in `Ubuntu 18.04 x64`
  - make sure to run `make`

```bash
wget http://download.redis.io/redis-stable.tar.gz
tar xvzf redis-stable.tar.gz
cd redis-stable
make
```

- Add these settings to `.bashrc` for personal preference

```bash
export APPLICATIONS_HOME="${HOME}/Documents/_applications"
export REDIS_HOME="${APPLICATIONS_HOME}/redis-5.0.5"
export REDIS_BIN="${REDIS_HOME}/src"

alias redis-server='cd ${REDIS_BIN}; ./redis-server'
alias redis-cli='cd ${REDIS_BIN}; ./redis-cli'

alias redis-restart='sudo systemctl restart redis.server'
alias redis-start='sudo systemctl start redis.server'
alias redis-stop='sudo systemctl stop redis.server'
alias redis-status='sudo systemctl status redis.server'
alias redis-enable='sudo systemctl enable redis.server'
alias redis-disable='sudo systemctl disable redis.server'
```

- Configure to start `redis` automatically with the server

```bash
sudo cp redis.service /etc/systemd/system
```

- Update the `systemd` service after copying `redis` services 

```bash
sudo systemctl daemon-reload
```

- Enable to auto-start `redis` service

```bash
redis-enable
```

- Start/Re-Start `redis` service

```bash
redis-start
redis-restart
```

- Installing `Redis Desktop Manager` UI
  - [Redis Desktop Manager](https://redisdesktop.com/)
  - [Install RedisDesktopManager using `Snapcraft` in Ubuntu](https://snapcraft.io/redis-desktop-manager)
  - [Redis Desktop Manager Quick Install](http://docs.redisdesktop.com/en/latest/install/)


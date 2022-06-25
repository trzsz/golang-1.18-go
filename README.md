# golang-1.18-go for trusty

### install
```
sudo apt update
sudo apt install software-properties-common
sudo add-apt-repository ppa:trzsz/golang
sudo apt update
sudo apt install golang-1.18-go
```

### publish
```
wget https://go.dev/dl/go1.18.3.src.tar.gz
tar -xzf go1.18.3.src.tar.gz

cd go
debuild -d -S -k$DEBSIGN_KEYID | tee /tmp/debuild.log 2>&1

cd ..
dput ppa:trzsz/golang golang-1.18-go_1.18.3.1_source.changes
```

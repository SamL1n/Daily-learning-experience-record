# install node.js on ubuntu


```bash
sudo apt install nodejs
```

then it will download node.js from ubuntu repository.

However,the `version` of node.js is 8.

So we need to update the latest version of node.js.

### enable the NodeSource repository
```bash
curl -sL https://deb.nodesource.com/setup_14.x | sudo -E bash -
```

### install the node.js 14x and npm
```bash
sudo apt-get install -y nodejs
```
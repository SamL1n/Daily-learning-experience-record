# Install PM2

### what is PM2
PM2 is a process manager for Node.js application.
PM2 make Node.js applications possible to run in the background as the service.

### why?
We use `npm app.js` to run a application,which will be killed after we closed the terminal.

### how to install 
```bash
npm install pm2@latest -g
```

### run application
```bash
pm2 start app.js
```
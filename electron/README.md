# Native Docker UI using Electron

** Note: This is a prototype and a work in progress**

## Known limitations/bugs

- Work witn errors with Unix sockets : unix:///var/run/docker.sock
- Docker TLS is not supported yet.


## Development

### Download Node.js & Electron dependencies
````
cd electron
npm install
bower install
```

### Compile Scala.js

```
sbt
project electron
~fullOptJS'
```

### Run the Electron UI
```
cd electron
npm start
```

### Package the native app
```
npm install electron-installer-dmg
nom install electron-installer
npm run-script package
npm run-script dmg
```
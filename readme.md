
1. To start an Electron app - npm start
2. To release the app Update - npm run deploy
    a. Go to github.com/REPO 
    b. Click on releases.
    c. Initially all the releases will be saved as the draft. Manually we need to relese the draft. 
    d. start the electron app. Automatically updates will be downloaded. Then follow the instruction on App. 
3. To build an app (without releasing) - npm run build
4. All the builds (executables and binaries) will be saved in dist folder.
5. We need better icon image to show.
6. To change the installation setup, in package.json change the nsis option. 

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Features Added
1. Auto Start App at startup
2. Auto Update
3. Home Page added 
4. 5s Page added with proper UI
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Note: 
1. To change the repo goto package.json and change the repository url.
2. Since the repo is public, we should not push our source codes to the repo. i.e. The repo should be used only to publish releases.
3. To find out the download speed and the app Size and version while downloading this code will help

      its an event, fired when downloading an app. The progressObj is an API through which we can get speed and size etc.
        autoUpdater.on("download-progress", progressObj => {
        let percentile = progressObj.percent;
        let n = percentile.toFixed(1);
        let downloadSpeed = (progressObj.bytesPerSecond)/1000000;
        let downloadSpeeds = downloadSpeed.toFixed(2);
        let downloadedSize = (progressObj.transferred)/1000000;
        let downloadedSizes = downloadedSize.toFixed(2);
        let totalSize = (progressObj.total)/1000000;
        let totalSizes = totalSize.toFixed(2);
        });

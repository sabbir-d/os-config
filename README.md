## DRIVERS

- [nvidia](https://www.nvidia.com/en-us/geforce/drivers/)
- [amd](https://www.amd.com/en/support)
- for **realtek** audio visit motherboard manufacturer website

## DOWNLOAD OTHER ESSENTIAL APPS

- [winrar](https://www.win-rar.com/postdownload.html?&L=0)
- [discord](https://discord.com/api/downloads/distributions/app/installers/latest?channel=stable&platform=win&arch=x86)
- [afterburner](https://www.msi.com/Landing/afterburner/graphics-cards)
- [slack](https://slack.com/api/desktop.latestRelease?arch=ia32&variant=exe&redirect=true)
- [vlc](https://get.videolan.org/vlc/3.0.18/win32/vlc-3.0.18-win32.exe)
- [obs](https://cdn-fastly.obsproject.com/downloads/OBS-Studio-29.0.2-Full-Installer-x64.exe)
- [steam](https://cdn.akamai.steamstatic.com/client/installer/SteamSetup.exe)
- [epic](https://launcher-public-service-prod06.ol.epicgames.com/launcher/api/installer/download/EpicGamesLauncherInstaller.msi)
- [figma](https://www.figma.com/download/desktop/win)


## CODING FONT

[jetbrains mono](https://download.jetbrains.com/fonts/JetBrainsMono-2.242.zip)\
[fira code](https://fonts.google.com/specimen/Fira+Code)


## INSTALL POSTMAN

[postman for desktop](https://dl.pstmn.io/download/latest/win64)

---

## INSTALL NODE

[node download link](https://nodejs.org/en/download)

- download LTS version for windows x64 .msi installer

```bash
just agree and click next next
```

### _for yarn users install yarn globally_

- although node comes with built in npm package manager if u wish u can use yarn as package manager by installing yarn globally

```bash
npm install --global yarn
```

### _install nodemon globally for backend_

- for realtime load of backend server

```bash
npm install -g nodemon
#or
yarn global add nodemon
```

---

## INSTALL MONGODB(NoSql)

[mongodb download link](https://www.mongodb.com/try/download/community)

```bash
click install, just agree and choose complete installation
```

- it will automatically download and install monogo compass(data base ui) which will take few extra minutes.

[mongodb shell download](https://downloads.mongodb.com/compass/mongodb-mongosh_1.6.1_amd64.deb?_ga=2.66967086.1814885739.1671987424-986248264.1671987424)

- mongo shell (interactive JavaScript interface to MongoDB) which will allow us to iterect with database using command line
- unzip the file and rename it something like **mongosh**
- move this mongosh folder to this location
  > `C:\Program Files`
- now press start button and type **environment variables**
- open **_edit environment variable_** inside **advance** tab at the bottom open **enviroment variables**
- in **system variables** select **path** and click **edit**
- click new and paste this location url
  > `C:\Program Files\mongosh\bin`
- click ok and get out of there
- now open a new terminal and type **mongosh** and press enter
- you should see mongosh log id, connection and other information

---

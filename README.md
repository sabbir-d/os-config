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
### Git configuration

**INSTALL GIT BASH**

download gitbash from [official website](https://github.com/git-for-windows/git/releases/download/v2.38.1.windows.1/Git-2.38.1-64-bit.exe)

- install git bash keeping all the settings to default
- click next next

**INSTALL WINDOWS TERMINAL**

1. download windows terminal from <a href="https://www.microsoft.com/store/apps/9n0dx20hk701" target="_blank">MS store</a> on windows 10 (windows 11 have this terminal by default)
2. to setup git bash in windows terminal follow the steps below :
   - open windows terminal and go to settings
   - click add new profile
   - click new empty profile
   - change the name to **gitbash** or **bash** upon ur like
   - replace the command line url with gitbash url
     > `C:\Program Files\Git\bin\bash.exe`
   - choose custom icon or use default gitbsh icon from this location
     > `C:\Program Files\Git\mingw64\share\git\git-for-windows.ico`
   - go startup tab and choose gitbash as default profile

**connect github with your system using SSH key**

```
ssh-keygen -t ed25519-sk -C YOUR_EMAIL
```
> if your system shows error on above command, use below command instead
```
ssh-keygen -t rsa -b 4096 -C YOUR_EMAIL
```

use the command above in terminal. go to `C:\Users\[username]\.ssh` this location and open the folder in an editor. open `id_ed25519.pub` and copy the full ssh key. go to this [link](https://github.com/settings/keys) click on `new ssh key`. give a title and paste the copied key at key field. now github should recognize your device.

**User login**
open terminal and follow the command below
```
git config --global user.email YOUR_EMAIL
git config --global user.name YOUR_USERNAME
```

**Basic commands**

`git clone url`\
`git remote set-url origin url`\
`git remote -v`\
`git status`\
`git add .`\
`git commit -m 'cloned commit'`\
`git push -u origin main`

**Clone repo with commits**

`git clone --bare <original-url>`\
`git push --mirror <new-url>`\
`git remote -v`\
`get remote set-url origin <new-url>`

**Clone remote branch**

`git clone <your-repo-url>`\
`cd my-cloned-project-folder`\
`git branch -a`\
`git checkout <branch-name>`

**Set remote to, already created remote repo with readme file**

`git branch -M main`\
`git remote add <origin-url>`\
`git pull origin main`\
`add .`\
`commit -m ‘first commit’`\
`git push -u origin main`

**Git another branch is pushing conflict (tags-fast forward, git pull)**

`git checkout master`\
`git pull origin`

**Delete git local branch**

`git branch -a`\
`git branch -d test`\
`git branch -D test (This will delete the branch regardless of its merge status)`

**Delete git remote branch**

`git push origin --delete <branch-name>`

**Clone branch from remote repo**

`git clone --single-branch -b <branchname-url >`


---
### vscode configuration
[vscode download link](https://code.visualstudio.com/sha/download?build=stable&os=win32-x64-user)
**list of extension**
✅ better comments\
✅ es7+react/redux native snippets\
✅ tailwindcss intellisnense\
✅ auto rename tag\
✅ material icon theme\
✅ monokai pro theme\
✅ markdown preview github styling\
✅ prettier code formatter\
✅ live server (for vanila html, css, js project)\
✅ live share (for sharing code)\
✅ code runner (for c++ or python)\
✅ fluent icons (minimul interface icons)\
✅ quokka.js (inline code runner)

**VS code snippets**

setting snippets as global across the editor. Open vscode code editor. Press `ctrl+shift+p`. Type `snippets`. click `snippets: configre user snippets`. and choose `new global snippets file`. Name it and paste the following code.

```json

{
"console output": {
	"prefix": "clog",
	"body": "console.log($0)",
	"description": ""
	},
	
	
	"regular function": {
		"prefix": "fun",
		"body": "function ${1:name}(${2:arg}) {$0}",
		"description": ""
	},
	
	"regular async function": {
		"prefix": "funf",
		"body": "async function ${1:name}(${2:arg}) {$0}",
		"description": ""
	},
	
	"arrow function": {
		"prefix": "af",
		"body": "const ${1:name} = (${2:arg}) => {$0}",
		"description": ""
	},
	
	"arrow async function": {
		"prefix": "aff",
		"body": "const ${1:name} = async (${2:arg}) => {$0}",
		"description": ""
	},
	
	"anonymous arrow function": {
		"prefix": "aaf",
		"body": "(${1}) => $0",
		"description": ""
	},
	

	"html tag": {
		"prefix": "tag",
		"body": "<$1 className={`$2`}>$0</$1>",
		"description": ""
	},
	
	"document id": {
		"prefix": "docid",
		"body": "document.getElementById('$0')"
	},
	
	"query selector id": {
		"prefix": "qs",
		"body": "document.querySelector('#$0')"
	},
	
	"query selector class": {
		"prefix": "cqs",
		"body": "document.querySelector('.$0')"
	},
	
	"query selector class all": {
		"prefix": "cqsa",
		"body": "document.querySelectorAll('.$0')"
	},
	
	
	"use state": {
		"prefix": "cstate",
		"body": [
			"const [${1:name}, set${1/(.*)/${1:/capitalize}/}] = useState$0($2)"
		]
	},
	
	"use effect": {
		"prefix": "signal",
		"body": ["useEffect$0 (() => {\t\n},[${1:dependency}])"]
	},
	
	"pass props": {
		"prefix": "pass",
		"body": ["${1:propname}={${0:prop}}"]
	},
	
	"class name": {
		"prefix": "cn",
		"body": ["className={`${0}`}"]
	},
	
		"React Functional Component with Props": {
			"prefix": "rfc-props",
			"body": [
				"type ${1:ComponentName}Props = {",
				"  children: React.ReactNode;",
				"};",
				"",
				"const ${1:ComponentName} = ({ children }: ${1:ComponentName}Props) => {",
				"  return (",
				"    ${2:<div>}{children}</div>",
				"  );",
				"};",
				"",
				"export default ${1:ComponentName};"
			],
			"description": "Creates a React functional component with TypeScript props."
		}
	
	
}

```

**Editor interface and ueses setting**

- copy full json code from the link above
- open vscode
- press ctrl + shift + p
- search for `open user settings (json)`
- paste the copied code here and save

```json
{
  "breadcrumbs.enabled": false,
  "window.menuBarVisibility": "compact",
  // <-- editor -->
  "editor.fontFamily": "cascadia code, jetbrains mono, monospace",
  "editor.fontSize": 15.5,
  "editor.fontLigatures": "'calt', 'ss01'",
  "editor.fontWeight": "380",
  "editor.cursorWidth": 3,
  "editor.cursorStyle": "line",
  "editor.cursorBlinking": "blink",
  "editor.cursorSmoothCaretAnimation": "off",
  "editor.cursorSurroundingLines": 8,
  "editor.smoothScrolling": true,
  "editor.mouseWheelScrollSensitivity": 2,
  "editor.minimap.enabled": false,
  "editor.wordWrap": "on",
  "editor.tabCompletion": "on",
  "editor.formatOnSave": true,
  "editor.acceptSuggestionOnEnter": "off",
  "editor.acceptSuggestionOnCommitCharacter": false,
  "editor.tabSize": 2, //extension
  "editor.parameterHints.enabled": false,
  "editor.hover.above": false,
  "editor.guides.bracketPairs": "active",
  "editor.lineNumbers": "on",
  "editor.glyphMargin": false,
  "editor.stickyScroll.enabled": false,
  "editor.lightbulb.enabled": "off",
  // "editor.folding": false,
  // "editor.renderWhitespace": "boundary",

  "editor.tokenColorCustomizations": {
    "comments": "#759272"
  },

  "[html]": {
    "editor.defaultFormatter": "vscode.html-language-features"
  },
  "[javascriptreact]": {
    "editor.defaultFormatter": "vscode.typescript-language-features"
  },

  //** <-- terminal -->
  "terminal.integrated.tabs.location": "left",
  "terminal.integrated.fontSize": 16,
  "terminal.integrated.fontFamily": "cascadia code",
  "terminal.integrated.cursorStyle": "line",
  "terminal.integrated.cursorWidth": 2,
  "terminal.integrated.cursorBlinking": true,
  "debug.console.fontFamily": "consolas",
  "debug.console.fontSize": 20,

  //** inegretd terminal switch to terminal from powershell -->
  "terminal.integrated.defaultProfile.windows": "Git Bash",
  "terminal.integrated.profiles.windows": {
    "C:\\Windows\\System32\\WindowsPowerShell\\v1.0\\powershell.exe (migrated)": {
      "path": "C:\\Windows\\System32\\WindowsPowerShell\\v1.0\\powershell.exe",
      "args": []
    }
  },

  //** <-- other -->
  "files.defaultLanguage": "typescript",
  "files.autoSave": "afterDelay",
  "files.autoSaveDelay": 1050,
  "zenMode.fullScreen": false,
  "tailwindCSS.emmetCompletions": true,
  "breadcrumbs.symbolPath": "off",
  "explorer.compactFolders": false, // expands folder structre even for the single file

  "emmet.includeLanguages": {
    "javascript": "javascriptreact",
    "vue-html": "html",
    "razor": "html",
    "plaintext": "jade"
    // inclued html emmet to js file
  },

  //** <-- workbench -->
  "workbench.sideBar.location": "right",
  "workbench.startupEditor": "none",
  "workbench.editor.showTabs": "single",
  "workbench.iconTheme": "material-icon-theme",
  "workbench.productIconTheme": "fluent-icons",
  "workbench.colorCustomizations": {
    "tab.inactiveForeground": "#e9e9e9",
    "tab.activeForeground": "#ffffff",
    "editorIndentGuide.activeBackground1": "#2bff00"
    /*    
      "statusBar.background": "#222225",
      "statusBar.noFolderBackground": "#222225",
      "statusBar.debuggingBackground": "#511f1f"
      "editorWhitespace.foreground": "#606b8d"
      */
  },

  "notebook.lineNumbers": "on",
  "notebook.markup.fontSize": 17,
  "[python]": {
    "editor.formatOnType": true
  },
  "javascript.updateImportsOnFileMove.enabled": "always",
  "editor.defaultFormatter": "esbenp.prettier-vscode",

  // all c/c++ config
  "[c]": {
    "editor.defaultFormatter": "ms-vscode.cpptools"
  },
  "[cpp]": {
    "editor.defaultFormatter": "ms-vscode.cpptools"
  },
  "[php]": {
    "editor.defaultFormatter": "bmewburn.vscode-intelephense-client"
  },
  "C_Cpp.clang_format_fallbackStyle": "Google",
  "C_Cpp.default.compilerPath": "C:\\msys64\\mingw64\\bin\\g++.exe",
  "liveServer.settings.donotVerifyTags": true,
  "explorer.confirmDelete": false,
  "window.commandCenter": false,
  "reactSnippets.settings.importReactOnTop": false,
  "liveServer.settings.donotShowInfoMsg": true
}

```
```json
.prettierrc
{
  "jsxBracketSameLine": true,
  "plugins": ["prettier-plugin-tailwindcss"],
  "tailwindAttributes": ["css"]
}

```

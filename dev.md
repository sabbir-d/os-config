# Developers setup


| count | content | details                              |
| ----- | ------- | ------------------------------------ |
| [1]()   | git     | git device setup and commands        |
| [2](####VS-code-snippets)   | vscode  | setup vs code as default code editor |

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

**SSH key gen**

```
ssh-keygen -t ed25519-sk -C "YOUR_EMAIL"
```

use the command above in terminal. go to `C:\Users\[username]\.ssh` this location and open the folder in an editor. open `id_ed25519.pub` and copy the full ssh key. go to this [link](https://github.com/settings/keys) click on `new ssh key`. give a title and paste the copied key at key field. now github should recognize your device.

**User login**
open terminal and follow the command below
```
git config --global user.email "YOUR_EMAIL"
git config --global user.name "YOUR_USERNAME"
```

**Basic commands**

`git clone url`
`git remote set-url origin url`
`git remote -v`
`git status`
`git add .`
`git commit -m 'cloned commit'`
`git push -u origin main`

**Clone repo with commits**

`git clone --bare <original-url>`
`git push --mirror <new-url>`
`git remote -v`
`get remote set-url origin <new-url>`

**Clone remote branch**

`git clone <your-repo-url>`
`cd my-cloned-project-folder`
`git branch -a`
`git checkout <branch-name>`

**Set remote to, already created remote repo with readme file**

`git branch -M main`
`git remote add <origin-url>`
`git pull origin main`
`add .`
`commit -m ‘first commit’`
`git push -u origin main`

**Git another branch is pushing conflict (tags-fast forward, git pull)**

`git checkout master`
`git pull origin`

**Delete git local branch**

`git branch -a`
`git branch -d test`
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
  // javascript

  "console output": {
    "prefix": "clog",
    "body": "console.log($0)",
    "description": ""
  },

  // javascript functions

  "regular function": {
    "prefix": "fun",
    "body": "function ${1:name}(${2:arg} {$0})",
    "description": ""
  },

  "regular async function": {
    "prefix": "afun",
    "body": "async function ${1:name}(${2:arg} {$0})",
    "description": ""
  },

  "arrow function": {
    "prefix": "arrow",
    "body": "const ${1:name} = (${2:arg}) => {$0}",
    "description": ""
  },

  "arrow async function": {
    "prefix": "aarrow",
    "body": "const ${1:name} = async (${2:arg}) => {$0}",
    "description": ""
  },

  "anonymous arrow function": {
    "prefix": ">>",
    "body": "(${1}) => $0",
    "description": ""
  },

  //  dom customize
  "html tag": {
    "prefix": "tag",
    "body": "<$1>$0</$1>",
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

  // react or solid js

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

  // smbols
  "copyright": {
    "prefix": "cr",
    "body": "&copy;",
    "description": ""
  },

  "and": {
    "prefix": "and",
    "body": "&",
    "description": ""
  },

  "hash": {
    "prefix": "hash",
    "body": "#",
    "description": ""
  },

  "": {
    "prefix": "",
    "body": "",
    "description": ""
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
  "window.menuBarVisibility": "compact",
  "breadcrumbs.enabled": false,

  // <-- editor -->
  "editor.fontFamily": "cascadia code, jetbrains mono, monospace",
  "editor.fontSize": 17,
  "editor.fontLigatures": "'calt', 'ss01'",
  "editor.fontWeight": "400",
  "editor.cursorWidth": 3,
  "editor.cursorStyle": "line",
  "editor.cursorBlinking": "phase",
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
  "editor.tabSize": 2,
  "editor.defaultFormatter": "esbenp.prettier-vscode", //extension
  "editor.parameterHints.enabled": false,
  "editor.hover.above": false,
  "editor.guides.bracketPairs": "active",
  "editor.lineNumbers": "on",
  "editor.glyphMargin": false,
  // "editor.folding": false,
  // "editor.renderWhitespace": "boundary",

  // set default formatter specifically
  "[html]": {
    "editor.defaultFormatter": "vscode.html-language-features"
  },
  "[javascriptreact]": {
    // "editor.defaultFormatter": "vscode.typescript-language-features"
  },

  // <-- terminal -->
  "terminal.integrated.tabs.location": "left",
  "terminal.integrated.fontSize": 17,
  "terminal.integrated.fontFamily": "cascadia code",
  "terminal.integrated.cursorStyle": "line",
  "terminal.integrated.cursorWidth": 2,
  "terminal.integrated.cursorBlinking": true,
  "debug.console.fontFamily": "consolas",
  "debug.console.fontSize": 20,

  // inegretd terminal switch to terminal from powershell -->
  "terminal.integrated.defaultProfile.windows": "Git Bash",
  "terminal.integrated.profiles.windows": {
    "C:\\Windows\\System32\\WindowsPowerShell\\v1.0\\powershell.exe (migrated)": {
      "path": "C:\\Windows\\System32\\WindowsPowerShell\\v1.0\\powershell.exe",
      "args": []
    }
  },

  //* <-- other -->
  "files.defaultLanguage": "javascript",
  "files.autoSave": "afterDelay",
  "files.autoSaveDelay": 1050,
  "liveServer.settings.donotShowInfoMsg": true,
  "zenMode.fullScreen": false,
  "better-comments.multilineComments": true,
  "tailwindCSS.emmetCompletions": true,
  "breadcrumbs.symbolPath": "off",
  "explorer.compactFolders": false, // expands folder structre even for the single file

  // emmet in specific language -->
  "emmet.includeLanguages": {
    "javascript": "javascriptreact",
    "vue-html": "html",
    "razor": "html",
    "plaintext": "jade"
    // inclued html emmet to js file
  },

  // <-- workbench -->
  "workbench.startupEditor": "none",
  "workbench.colorCustomizations": {
    /*    
    "editorIndentGuide.activeBackground": "#b9b9b9",
    "statusBar.background": "#222225",
    */
  },
  "material-icon-theme.folders.color": "#b342f5",

  "[python]": {
    "editor.formatOnType": true
  },

  "javascript.updateImportsOnFileMove.enabled": "always",
}


```
# octokit-get-content-file-github

Install
```
octokit       https://github.com/octokit/rest.js/
vscode-icons  https://marketplace.visualstudio.com/items?itemName=vscode-icons-team.vscode-icons
```

Dependencies
```
npm install @octokit/rest
```

Command line
```
Run file     
    - npx node ./src/vicboma1/octokit/main.js
    - node.exe ./src/es/vicboma1/octokit/main.js
```

Example 
```
const { Octokit } = require("@octokit/rest");

const octokit = new Octokit({});

octokit.repos.getContent({
    owner: 'vicboma1',
    repo: 'octokit-get-content-file-github',
    path: 'README.md'
}).then(result => {
      console.log(result.data.content)
      const content = Buffer.from(result.data.content, 'base64').toString()
      console.log(content)
}).catch( ex => {
      console.log('Error:'+ex)
})
```

Result Base64 
```
IyBvY3Rva2l0LWdldC1jb250ZW50LWZpbGUtZ2l0aHViCgpJbnN0YWxsCmBg
YApvY3Rva2l0ICAgICAgIGh0dHBzOi8vZ2l0aHViLmNvbS9vY3Rva2l0L3Jl
c3QuanMvCnZzY29kZS1pY29ucyAgaHR0cHM6Ly9tYXJrZXRwbGFjZS52aXN1
YWxzdHVkaW8uY29tL2l0ZW1zP2l0ZW1OYW1lPXZzY29kZS1pY29ucy10ZWFt
LnZzY29kZS1pY29ucwpgYGAKCkRlcGVuZGVuY2llcwpgYGAKbnBtIGluc3Rh
bGwgQG9jdG9raXQvcmVzdApgYGAKCkNvbW1hbmQgbGluZQpgYGAKUnVuIGZp
bGUgICAgIAogICAgLSBucHggbm9kZSAuL3NyYy92aWNib21hMS9vY3Rva2l0
L21haW4uanMKICAgIC0gbm9kZS5leGUgLi9zcmMvZXMvdmljYm9tYTEvb2N0
b2tpdC9tYWluLmpzCmBgYAoKUmVzdWx0IEJhc2U2NCAKYGBgCgpgYGAKClJl
c3VsdCB0b1N0cmluZwpgYGAKCmBgYA==
```


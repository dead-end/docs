## Steps to create a pull request

The first step is to fork the repository on github.

Then we need to clone the repository and create a branch for the fix.
```
git clone https://github.com/dead-end/isomorphic-git.git

cd isomorphic-git/

git branch fix-1245

git checkout "fix-1245"
Switched to branch 'fix-1245'
```

The next step is to build the module:
```
npm install

npm run build
...
isomorphic-git-0.0.0-development.tgz
```
Then we create a project to test the fix

```
cd ..

mkdir fix-test

cd fix-test

npm init -y
```

Install the other dependencies
```
npm i rimraf
```

Add the dependency in the package.json:
```
cat package.json
{
  "name": "fix-test",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "isomorphic-git": "file:../isomorphic-git/isomorphic-git-0.0.0-development.tgz",
    "rimraf": "^5.0.0"
  }
}
```

```
npm install
```
Now you can run the tests before the fix (`node index.js`). 


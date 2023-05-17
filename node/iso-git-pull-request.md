# Steps to create a pull request

The first step is to fork the repository on github.

Then we need to clone the repository and create a branch for the fix.
```
git clone https://github.com/dead-end/isomorphic-git.git

cd isomorphic-git/

git branch fix-1245

git checkout fix-1245
Switched to branch fix-1245

npm install

npm run build
```

Create the link 
- https://docs.npmjs.com/cli/v8/commands/npm-link
- https://medium.com/dailyjs/how-to-use-npm-link-7375b6219557
```
npm link
...

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

npm i isomorphic-git

npm link isomorphic-git

ls -l node_modules/isomorphic-git
lrwxrwxrwx 1 dead-end dead-end 20 Mai 14 10:54 node_modules/isomorphic-git -> ../../isomorphic-git
```

Now we can write code to trigger the fix.
Fix the bug in the branch.
Run build
Run your test code again


# Single Test

```
npm i -g jest-cli
```

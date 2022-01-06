# ESLint config with husky and lint-staged

## config steps
1. create an empty folder or open an exist project folder
```
mkdir eslint-config-with-husky
cd eslint-config-with-husky
npm init -y
```

2. add `react`package(eslint-config-react-app required react)
```
npm install react
```

3. add `eslint-config-react-app` package
```
npm install --save-dev eslint-config-react-app eslint@^8.0.0
```

Then create a file named .eslintrc.json with following contents in the root folder of your project:
```json
{
  "extends": "react-app"
}
```

4. Installation and setup lint-staged and husky
```
npx mrm@2 lint-staged
```

FAQ

* if it just has warning and no error with your code, it will not print out the warning message in the ternimal!
即使有警告，如果没有错误，则不会在提交的控制台中打印出警告信息(不要认为不启作用)！
因为eslint

Root Cause:
>ESLint comes with a large number of built-in rules and you can add more rules through plugins. You can modify which rules your project uses either using configuration comments or configuration files. To change a rule setting, you must set the rule ID equal to one of these values:

* "off" or 0 - turn the rule off
* "warn" or 1 - turn the rule on as a warning (doesn't * affect exit code)
* "error" or 2 - turn the rule on as an error (exit code is 1 when triggered)

# Reference

- [-] https://beta.reactjs.org/learn/editor-setup#linting
- [-] https://www.npmjs.com/package/eslint-config-react-app
- [-] https://typicode.github.io/husky/#/
- [-] https://www.npmjs.com/package/lint-staged
- [-] https://eslint.org/docs/user-guide/getting-started
- [-] https://eslint.org/docs/user-guide/configuring/
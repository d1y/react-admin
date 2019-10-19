## 后台系统

安装依赖

```console

cnpm i --save antd-mobile

```

按需打包

```console

cnpm i --save-dev babel-plugin-import react-app-rewired

```

根目录创建 `config-overrides.js`

```js
const { injectBabelPlugin } = require('react-app-rewired')

module.exports = (config, env)=> {
  config = injectBabelPlugin([
    'import', {
      libraryName: 'antd-mobile',
      style: 'css'
    }
  ])
  return config
}

```
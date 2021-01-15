# Stylelint Config Custom

这是我自己定制并将持续维护的 stylelint 配置。  
这份配置主要包含两部分规则：

* stylelint 官方的标准规则：stylelint-config-standard
* stylelint 插件 stylelint-order

使用 stylelint 的 order 插件是为了更深入地规范样式代码，各属性先后有序且相同类型的放在一起，能有效提高自己和他人阅读代码的效率。所使用的属性排序规则基于 CSScomb 的 [zen](https://github.com/csscomb/csscomb.js/blob/dev/config/zen.json) 规则和 [stylelint-config-rational-order](https://github.com/constverum/stylelint-config-rational-order)，我对它们做了综合整理，删除了已弃用或几乎不会再使用的属性，增加了一些常用的新的属性。

## 了解 stylelint

[stylelint 官网](https://stylelint.io/)  
[stylelint repositories](https://github.com/stylelint)

## 使用方法

本质上这只是一份配置文件，它遵循 stylelint 官方的[使用指南](https://stylelint.io/user-guide/configure)。

### 安装相关依赖包

安装相关依赖包到项目中：

``` bash
npm i -D stylelint stylelint-config-standard stylelint-order
```

### 下载并修改配置文件

下载 repository 中的 `.stylelintrc.js` 文件到项目的根目录。  
如果有需要，针对性地查看并修改文件里面的相关配置。

### 编辑器设置

[编辑器插件列表](https://stylelint.io/user-guide/integrations/editor)  

以 VSCode 为例：

* 首先，在 VSCode 中安装 [stylelint 插件](https://marketplace.visualstudio.com/items?itemName=stylelint.vscode-stylelint)
* 然后，在 VSCode 的 `settings.json` 文件中增加下面内容：

  ```js
  // 在使用 stylelint 的情况下，不再需要编辑器及其插件的代码检查相关功能，建议关闭

  // 关闭 VSCode 自带的样式代码检查功能
  "css.validate": false,
  "less.validate": false,
  "scss.validate": false,
  // 关闭 VSCode 的 Vetur 插件对应的代码检查功能（适用于 Vue.js 开发者）
  "vetur.validation.style": false
  ```

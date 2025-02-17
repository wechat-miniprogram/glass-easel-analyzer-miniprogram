# glass-easel-analyzer-miniprogram

面向微信小程序的 glass-easel-analyzer 配置文件，配合 [glass-easel-analyzer](https://github.com/wechat-miniprogram/glass-easel-analyzer) 使用。


## 使用方法（ Visual Studio Code ）

首先，安装 glass-easel-analyzer ：[前往扩展商店](https://marketplace.visualstudio.com/items?itemName=wechat-miniprogram.glass-easel-analyzer)。

然后，将这个项目 git clone 到本地，或者只下载 [miniprogram-config.toml](miniprogram-config.toml) 文件，得到一个本地的 miniprogram-config.toml 文件路径。

之后将这个路径设置到 Visual Studio Code 的 `glass-easel-analyzer.backendConfigurationPath` 配置项上即可。具体设置方法有下面几种，任选其一即可。

### 设置到编辑器全局

这个方式对所有项目生效。

打开 Visual Studio Code 设置（快捷键 Ctrl/Command + `,` ），搜索 `glass-easel-analyzer.backendConfigurationPath` ，然后填入 miniprogram-config.toml 文件的完整绝对路径。

### 设置到工作区

适用于想要针对某个工作区单独生效的情况。

打开工作区对应的 `[NAME].code-workspace` 文件，在这个 JSON 格式文件的 `settings` 中加入：

```json
{
  "settings": {
    "glass-easel-analyzer.backendConfigurationPath": "[miniprogram-config.toml 文件的路径，可以是相对本文件的路径]"
  }
}
```

### 设置到项目文件夹

适用于想要针对某个单项目文件夹生效的情况。（如果在一个编辑器窗口中打开多个文件夹，这种方法会失效。）

创建或打开项目文件夹下的 `.vscode/settings.json` 文件，在这个 JSON 格式文件的 `settings` 中加入：

```json
{
  "glass-easel-analyzer.backendConfigurationPath": "[miniprogram-config.toml 文件的路径，可以是相对项目文件夹的路径]"
}
```


## 注意事项

这个配置文件是自动从微信小程序文档中提取的，并随它更新而更新。总的来说和微信小程序文档是保持一致的，但如有出入，请以小程序文档为准。（样式相关的部分提取自默认 web 配置。）



![github-contribution-grid-snake](./github-contribution-grid-snake.svg)

# 用hugo+GitHub Pages搭建的小破站
#### [https://9981000.xyz](https://9981000.xyz)           Powered by [Hugo](https://gohugo.io/) & [Lynx](https://git.io/hugo-lynx) & [Github](https://github.com/) & [Cloudflare](https://www.cloudflare-cn.com/)
![](./author.jpg)


#### Hugo 在 EdgeOne Pages 部署

首先在git仓库里添加一个文件：[`package.json`](package.json)，代码如下：

```language-javascript
{
  "name": "填一个名称",
  "version": "1.0.0",
  "scripts": {
    "build": "./node_modules/.bin/hugo --minify",
    "postinstall": "git submodule update --init",
    "dev": "hugo server -D",
    "clean": "rm -rf public",
    "preview": "hugo server"
  },
  "dependencies": {
    "hugo-extended": "^0.147.8"
  },
  "devDependencies": {
    "cross-env": "^7.0.3"
  }
}
```

> 其中"hugo-extended": "^0.147.8" 是Hugo的版本，后续改成最新版即可。
>



输出目录：`public`

构建命令：`npm run build`

安装命令：`HUGO_BIN_EXTENDED=true npm install --save-dev cross-env`


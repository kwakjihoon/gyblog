
### vue setting

#### Basic setting
```terminal
# vue 설치
sudo npm install -g @vue/cli

# create vue front project  (using default)
vue create front

# default project directory
cd front
# README.md               babel.config.js         node_modules            package-lock.json       package.json            public                  src

```
#### vue config file
```js
module.exports = {
    //publicPath:"/vue-front",
    outputDir: "../src/main/resources/static/",
    indexPath: "index.html",
    devServer: {
        proxy: "http://localhost:8080"
    },
    chainWebpack: config => {
        const svgRule = config.module.rule("svg");
        svgRule.uses.clear();
        svgRule.use("vue-svg-loader").loader("vue-svg-loader");
    }
};

```

#### veu basic command
```terminal

cd front

npm run build

npm run serve


```
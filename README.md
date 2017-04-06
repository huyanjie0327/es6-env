# es6-env
es6简易环境搭建

使用babel 将es6的语法转换成es5的语法

1. 安装babel相关包
    npm install babel-preset-stage-2 --save-dev
    npm install babel-preset-latest --save-dev
2. 配置文件.bashrc
    在项目根目录下，添加
    {
        "presets": [],
        "plugins": []
    }
    presets字段设定转码规则
    # 最新转码规则
    $ npm install --save-dev babel-preset-latest

    # react 转码规则
    $ npm install --save-dev babel-preset-react

    # 不同阶段语法提案的转码规则（共有4个阶段），选装一个
    $ npm install --save-dev babel-preset-stage-0
    $ npm install --save-dev babel-preset-stage-1
    $ npm install --save-dev babel-preset-stage-2
    $ npm install --save-dev babel-preset-stage-3
    根据需要添加
    {
        "presets": [
        "latest",
        "stage-2"
        ],
        "plugins": []
    }
3. 安装babel-cli
    npm install babel-cli --save-dev
4. 修改package.json
    {
    // ...
    "devDependencies": {
        "babel-cli": "^6.0.0"
    },
    "scripts": {
        "build": "babel src -d lib"
    },
    }
5. 转码的时候，运行npm run build

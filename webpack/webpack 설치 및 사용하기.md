# webpack ์ค์นํ๊ธฐ
๐๐ webpack์ ๋ค๋ฅธ ์ ์ฅ์์ ์ค์น๋ฅผ ํด๋์ด ํ์ธํ์ค ์ ์์ต๋๋ค.
https://github.com/mireyhgnay/webpack    

### 1. npm init

```bash
npm init
```

๐ย  init๋ฅผ ์๋ ฅํ๋ฉด package-name์ ์ค์ ํ๋ผ๊ณ  ๋จ๋๋ฐ enter๋ฅผ ๋๋ฅด๋ฉด ์๋์ผ๋ก ํด๋ ์ด๋ฆ์ด ์๋ ฅ๋๋ค.     
(๋จ, ํ๊ธ์ ์ธ์ํ์ง ๋ชปํ๋ฏ๋ก ํ๊ธ์ผ ๊ฒฝ์ฐ ์์ด๋ก package ์ด๋ฆ์ ์ค์ ํด์ค์ผ ํ๋ค.)      
์ดํ์ ๊ณ์ ๋ญ ๋ฌผ์ด๋ณด์ง๋ง enter, enter, โฆ      
๊ทธ๋ฆฌ๊ณ  ๋ง์ง๋ง์ Is this OK?๋ผ๊ณ  ๋ฌผ์ด๋ณด๋๋ฐ yes๋ผ๊ณ  ์๋ ฅํด๋ ๋๊ณ  ๊ทธ๋ฅ enter๋ฅผ ๋๋ฌ๋ ๋๋ค.     

๐ ์ด ๋ชจ๋  ๊ณผ์ ์ด ๋๋๋ฉด ํด๋์ย package.json ํ์ผ์ด ์์ฑ๋๋ค.

### 2. webpack ์ค์น

```bash
npm install webpack webpack-cli --save-dev
```

๐ย  ์ค์น๊ฐ ๋๋๋ฉด node_modules ํด๋์ package-lock.js ํ์ผ์ด ์์ฑ๋๋ค

### 3. html, js, cssํ์ผ๋ค์ด ๋ค์ด๊ฐ src ํด๋ ์์ฑ

๐ย   ํ๋ก์ ํธ ํด๋ ์๋ src ํด๋๋ฅผ ๋ง๋ค์ด, html, js, css ๋ฑ ์์ค์ฝ๋๋ฅผ ๋ฃ์ด์ค๋ค.

๐ย  ํด๋ ๊ตฌ์กฐ (์นํฉ์ค์  = ํ๋ก์ ํธ ํด๋๋ช)
- ํด๋ ๊ตฌ์กฐ
![แแณแแณแแตแซแแฃแบ 2022-10-18 แแฉแแฅแซ 12 24 13](https://user-images.githubusercontent.com/111990266/196453442-16e01365-7493-4e1b-95dc-55b9d0a2d11f.png)
    

### 4. webpack.config.js ํ์ผ ์์ฑ
๐ย   webpack์ด ํด๋น ํ๋ก์ ํธ ์์์ ์ด๋ค ์์ผ๋ก ๊ตฌ์๋์ด ์คํ๋  ๊ฒ์ธ์ง ์ ํ๋ ํ์ผ    
๐ย   ์์น๋ ํ๋ก์ ํธ ํด๋ ๋ฐ๋ก ์๋**(package.json ํ์ผ๊ณผ ๊ฐ์ ์์น)**

```jsx
const path = require('path');

module.exports = {
  entry: './src/index.js',
  output: {
    filename: 'main.js',
    path: `${__dirname}/dist`,
  },
};
```

- ์ฐ๋ฆฌ๊ฐ ํ๋ก์ ํธ ๋ด๋ถ์์ ์ฌ๋ฌ jsํ์ผ์ด๋ css ํ์ผ์ ์์ฑํด๋ ๊ฒฐ๊ตญ ์ต์ข์ ์ผ๋ก webpack์ด ํ์ธํ๋ ํ์ผ์ entry์ ์๋ jsํ์ผ(**index.js**)์ด๋ค.
- webpack์ด ์คํ๋๋ฉด ํด๋น jsํ์ผ **(index.js)์ ์ฐธ๊ณ ํ์ฌ, webpack์ ์ต์ข์ ์ผ๋ก jsํ์ผ์ ๋ง๋ค๊ฒ ๋๋๋ฐ, ์ด ํ์ผ์ด ๋ฐ๋ก output ์์ ์๋ main.js**ํ์ผ์ด๋ค. 
(์ฐธ๊ณ ๋ก ์ด ํ์ผ์ dist๋ผ๋ ํด๋์ ์ ์ฅ๋์ด์ง๋๋ค. distํด๋๋ webpack๋ฅผ ์คํํด์ผ ์๊ธฐ๋ ํ์ผ์๋๋ค.)
- ํ์ฌ ์ค์  ์์ผ๋ก๋ ํ๋ก์ ํธ ๋ด๋ถ์ ํ์ผ์ ๋ณ๊ฒฝํ๊ฒ ๋๋ฉด, npx webpack์ผ๋ก ํจํค์ง์ ํด์ฃผ๊ณ  ์คํํด์ผ ๋ณ๊ฒฝ๋ ์ฌํญ์ด ์ ์ฉ๋จ โ ๋ฒ๊ฑฐ๋ก์ฐ๋ ์๋ํ๋ฅผ ์์ํด๋ด์๋ค.

### 5. ์๋ํํ๊ธฐ
**webpack dev serve ์ค์น**

```bash
npm install --save-dev webpack-dev-server
```

**webpack.config.js ์ devServer ๊ด๋ จ ์ฝ๋ ์ถ๊ฐ**
```jsx
const path = require('path');

module.exports = {
  entry: './src/index.js',
  output: {
    filename: 'main.js',
    path: `${__dirname}/dist`,
  },

////// ์ถ๊ฐ ์์ญ //////
  devServer: {
    static: './dist', 
  }, ////// ์ถ๊ฐ ์์ญ //////
};
```

**HTML webpack Pluginย  ์ค์น**

```bash
npm install --save-dev html-webpack-plugin
```

**webpack.config.js์ html webpack plugin ๊ด๋ จ ์ฝ๋ ์ถ๊ฐ**

```jsx
const path = require('path');
////// ์ถ๊ฐ ์์ญ //////
const HtmlWebpackPlugin = require('html-webpack-plugin');
////// ์ถ๊ฐ ์์ญ //////

module.exports = {
    entry: './src/index.js',
    output: {
        filename: 'main.js',
        path: `${__dirname}/dist`,
    },

    devServer: {
        static: './dist', 
    }, 
  
////// ์ถ๊ฐ ์์ญ //////
    plugins: [new HtmlWebpackPlugin({
        template: './src/index.html'
    })],////// ์ถ๊ฐ ์์ญ //////
};
```

๐ย src์ ์์นํ index.html ํ์ผ์ distํ์ผ๋ก ์ฎ๊ฒจ, ์๋ฒ๊ฐ ์คํ๋๋ฉด index.html์ด ๋ณด์ด๋๋ก ์ค์ ํ๋ ๊ณผ์ ์๋๋ค.     
๐ ๋ง์ฝ index.html์ด ์๋ ๋ค๋ฅธ html ํ์ผ์ ๋์ฐ๊ธธ ์ํ์ ๋ค๋ฉด, ํด๋น ํ์ผ ์ด๋ฆ์ index.html ๋์  ์ ์ด์ฃผ์๋ฉด ๋ฉ๋๋ค.    

**์ต์ข webpack.config.js ์ฝ๋**

```jsx
const path = require('path');

module.exports = {
    entry: './src/index.js',
    output: {
        filename: 'main.js',
        path: `${__dirname}/dist`,
    },

    devServer: {
        static: './dist', 
    }, 
  
    plugins: [new HtmlWebpackPlugin({
        template: './src/index.html'
    })],
};
```

**package.jsonํ์ผ์ scripts ์์ญ์ ์๋ ์ฝ๋ ์ถ๊ฐ**

```jsx
"scripts": {
    "build": "wepback ",
    "start": "webpack serve --open",
    //.. ์๋ต ..
  },
```

### 6. ์คํํด๋ณด๊ธฐ

ํ๋ก์ ํธ ํด๋ ํฐ๋ฏธ๋์์ npm start ์๋ ฅ โ index.html ๋ก๋ฉ ์๋ฃ โ ์ฑ๊ณต!

```
npm start ํ๊ณ  ์ค๋ฅ๋ก ์ฝ์งํ๋๋ฐ โฆ ๊ฒฐ๊ตญ Node ๋ฒ์ ์ด ๋๋ฌด ๋ฎ์์ ์๋์๋ ๊ฒ์ด์๋ค!!
์ ์ผ ์ต์  ๋ฒ์ ์ธ 18.11.0 (npm use 18.11.0)์ผ๋ก ๋ณ๊ฒฝํ๋ ์ฑ๊ณตํ๋ค!!!!๐ฅณ
```

---

**@Reference**
[webpack :: ๋๋ ํ ๋ฆฌ์ ์นํฉ ์ค์น ๋ฐ ๊ธฐ๋ณธ ์ค์ ](https://art-coding3.tistory.com/m/56)
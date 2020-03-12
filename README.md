# webpack 打包工具使用
1. 將 `sass` 轉換 `css` - 使用 `sass-loader` 、 `css-loader` 、 `mini-css-extract-plugin` 、 `postcss-loader` (瀏覽器支援) npm套件
2. `javascript es6` 轉換成 `es5` 支援一些較舊的瀏覽器 - 使用 `babel-loader` npm 套件
3. 壓縮超過 1mb 的圖片 - `url-loader` 、 `file-loader` 、 `image-webpack-loader` npm 套件
4. 清空編譯後的資料夾 `/dist/` - `clean-webpack-plugin` npm 套件
5. 用 webpack 內建功能 `splitChunks` 來合併重複的js檔案
<hr>

打開命令提示字元<br>
cd 本專案放到本機的路徑<br>
輸入 `npm run watch` <br>
即可使用

```
λ npm run watch

> piyan@1.0.0 watch C:\piyan
> webpack --mode development --watch


webpack is watching the files…

Hash: 03f84e23ed9d92b362a0
Version: webpack 4.42.0
Time: 3527ms
Built at: 2020-03-12 23:35:50
                              Asset      Size   Chunks             Chunk Names
               ./js/index.bundle.js  2.94 KiB    index  [emitted]  index
                ./js/page.bundle.js  3.71 KiB     page  [emitted]  page
             ./js/runtime.bundle.js  6.12 KiB  runtime  [emitted]  runtime
              ./js/vendor.bundle.js  3.71 KiB   vendor  [emitted]  vendor
images/pc_wallaper_1920x1080_v1.jpg   178 KiB           [emitted]
images/pc_wallaper_1920x1080_v2.jpg   244 KiB           [emitted]
Entrypoint index = ./js/runtime.bundle.js ./js/index.bundle.js
Entrypoint page = ./js/runtime.bundle.js ./js/page.bundle.js
Entrypoint vendor = ./js/runtime.bundle.js ./js/vendor.bundle.js
[./assets/images sync recursive ^\.\/.*$] ./assets/images sync ^\.\/.*$ 230 bytes {index} {page} {vendor} [built]
[./assets/images/pc_wallaper_1920x1080_v1.jpg] 148 bytes {index} {page} {vendor} [optional] [built]
[./assets/images/pc_wallaper_1920x1080_v2.jpg] 148 bytes {index} {page} {vendor} [optional] [built]
[./assets/index.js] 86 bytes {index} {page} {vendor} [built]
[./assets/page.js] 67 bytes {page} {vendor} [built]
[./assets/vendor.js] 46 bytes {vendor} {page} [built]

```

然後到本機資料夾 `/dist/` 可以看到壓縮後的圖片、js 、css 檔案


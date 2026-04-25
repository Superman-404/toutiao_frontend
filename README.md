### 具体步骤（拉取后）

1. **克隆仓库**

   bash

   ```
   git clone <你的仓库地址>
   cd xwzx-news
   ```

   

2. **安装依赖，生成 `node_modules`**

   bash

   ```
   npm install
   ```

   

   - 因为你的仓库里保留了 `package.json` 和 `package-lock.json`，运行这个命令后，npm 会严格按照锁定文件里的依赖版本，把 `node_modules` 精准还原出来。

------

### 关于 `.vite`

- `.vite` 是 Vite 的**依赖预构建缓存**，它会在你后续执行任何 Vite 命令时**自动生成**，比如：

  bash

  ```
  npm run dev
  ```
### 关于 `AI问答`
- src/comfig/api.js 将api key 改成自己的,或者换其他大模型平台url
  

  启动开发服务器后，Vite 会立刻在项目根目录生成 `.vite` 文件夹，并根据 `package.json` 里的依赖重新构建缓存。

- 你**不需要主动安装或生成 `.vite`**，它完全由 Vite 按需创建。`.gitignore` 里已经忽略了它，以后也不会被提交。


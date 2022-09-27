# 使用 Hardhat 创建一个基础的智能合约

### 1、搭建环境
首先，`Hardhat` 是基于 `JavaScript` 编写的，因此，需先安装 `Node` 环境。

>MacOS
```shell
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
nvm install --lts
nvm use stable
nvm alias  default stable
npm install npm --global 
```
### 2、创建一个 Hardhat 项目
进入一个空的文件夹，利用 `npm cli` 安装 `Hardhat`

```shell
mkdir hardhat-project  # 创建一个空的 hardhat-project 文件夹
cd hardhat-project # 进入文件夹
npm init --yes # 创建 package.json 文件
npm install --save-dev hardhat # 安装开发式依赖
npx hardhat # 创建 hardhat 项目
```

### 3、常见执行命令
```shell
npx hardhat help
npx hardhat test # Runs mocha tests
REPORT_GAS=true npx hardhat test # Runs mocha tests & 开启分析gas消耗报告
npx hardhat compile # Compiles the entire project, building all artifacts
npx hardhat node # Starts a JSON-RPC server on top of Hardhat Network
npx hardhat run scripts/deploy.js # Runs a user-defined script after compiling the project
```

# 简单demo - 编写与编译合约
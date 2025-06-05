# Dria-Node
Dria部署-MAC

## 1.安装Homebrew(如果没有安装）
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

## 2. 安装 Ollama
brew install ollama

## 3. 安装Dria Node
curl -fsSL https://dria.co/launcher | bash
source ~/.zshrc

## 4. 配置Dria Node
dkn-compute-launcher setup
* 按提示填写 EVM 钱包私钥、模型（如 gemini、ollama、openrouter）、API Keys 等信息。
* 只用 gemini 和 openrouter 时，只需填入对应 API Key，其他可跳过。

## 启动 Dria Node 
建议用 screen 或 tmux 后台运行（如未安装 screen，可先执行 brew install screen）
screen -S dria
dkn-compute-launcher start

## 6. 创建邀请码
dkn-compute-launcher referrals

## 7. 检查节点积分
连接 EVM 钱包后，访问 https://dria.co/edge-ai/my-node 查看积分。

## 8. 卸载节点
dkn-compute-launcher uninstall

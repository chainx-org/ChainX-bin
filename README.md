# ChainX-bin

:warning: [Deprecated] Please move to https://github.com/chainx-org/ChainX/wiki/Testnet .

-----

Binary release of unpublicized [ChainX](https://github.com/chainx-org/ChainX).

## ChainX v0.9.5 公开测试网

1. 访问在线钱包 [wallet.chainx.org](https://wallet.chainx.org)。

2. 点击创建账户，生成节点账户，**账户地址**形如 `5HbT8...S9yg`，导出**账户私钥**形如 `0x30530...c95aee43`。

3. 首先在资产页领取 1 个 PCX 测试币，以便能够发起交易，进行注册，更新节点等操作。

4. 在投票选举页，点击注册节点，设置 **节点名称**，比如 NodeABC。

5. 在投票选举页的候选节点里，可以看到你的节点处于 **退选** 状态。

6. 在 https://github.com/chainx-org/ChainX-bin/releases/tag/v0.9.5 下载 v0.9.5 测试网 ChainX 二进制 `chainx`, 目前仅支持 Ubuntu 16.04+ 或 macOS。

7. 启动节点。

    ```bash
    # 启动验证人节点
    ./chainx --key=账户私钥 --validator-name=节点名称 --name=监控台名称 --base-path=数据存放路径 --validator --chain=local --pruning archive

    # 启动同步节点
    ./chainx --name=监控台名称 --base-path=数据存放路径 --chain=local --pruning archive 
    ```

    待节点部署完毕，并在监控台等待自己的节点同步到最新，监控台地址为 https://telemetry.polkadot.io/#/ChainX%20V0.9.5 。

8. 在投票选举页，点击更新节点，填写:

    - 出块地址(**账户地址**)
    - 网址
    - 简介
    - 选择“参选”。

9. 请求社区投票至前 30 名，每 10 分钟（300块的整数倍）会进行一次验证人选举，如果在前 30 名就可以出块了，如果看到命令行打印 Prepared block for proposing at 6467之类的，就代表在出块了 。

10. 如果由于节点部署不当等导致的节点掉线，系统会逐步惩罚节点奖池，如果惩罚只0.33以下，会自动退选，节点需检查部署情况后，再次更新节点至参选状态，等待下一轮换届。

## CHANGELOG

- ~v0.9.4~
- ~v0.9.3~

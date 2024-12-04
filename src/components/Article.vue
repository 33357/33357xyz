<template>
  <div class="timeline-container">
    <el-timeline style="max-width: 1000px">
      <el-timeline-item
        v-for="(activity, index) in activities"
        :key="index"
        :timestamp="activity.timestamp"
      >
        <el-link
          :href="activity.link"
          target="_blank"
          class="large-font-timeline"
          >{{ activities.length - index }}、{{ activity.content }}</el-link
        >
      </el-timeline-item>
    </el-timeline>
  </div>
</template>

<script lang="ts" setup>
const activities = [
{
    content: "狂印 48 亿 U，新型加密资产质押协议 Ethena",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Event/Ethena.md",
    timestamp: "2024-12-4",
},
{
    content: "Devcon 和 Smartcon",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Meeting/Devcon&Smartcon.md",
    timestamp: "2024-11-30",
},
{
    content: "多钱包自动打币机器人",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Event/2024-10-19/README.md",
    timestamp: "2024-10-19",
},
  {
    content: "一个 ETH 换一个 BTC，uniBTC 被盗千万",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Event/2024-9-27/README.md",
    timestamp: "2024-9-27",
  },
  {
    content: "AdventureX 和 EDCON",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Meeting/AdventureX&EDCON.md",
    timestamp: "2024-8-3",
  },
  {
    content: "写一个 0 转账攻击合约",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Event/0TransferAttack.md",
    timestamp: "2024-7-7",
  },
  {
    content: "警惕科学家钓鱼合约",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Event/FishingScientist.md",
    timestamp: "2024-6-30",
  },
  {
    content: "反闪电贷协议 EIP7690",
    link: "https://github.com/33357/smartcontract-apps/blob/main/EIPS/eip7690.md",
    timestamp: "2024-6-23",
  },
  {
    content: "通过 GAS 排行搜寻新机会",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Gas/GasSearch.md",
    timestamp: "2024-6-1",
  },
  {
    content: "不受单个矿工控制的链上随机数生成方法",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Solidity/Other/random.md",
    timestamp: "2024-4-23",
  },
  {
    content: "让 EVM 再次伟大，用智能合约保证 MEME 的安全",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Event/meme.md",
    timestamp: "2024-3-19",
  },
  {
    content: "坎昆升级简析",
    link: "https://github.com/33357/smartcontract-apps/blob/main/EIPS/dencun.md",
    timestamp: "2024-3-13",
  },
  {
    content: "ethscriptions 铭文链和哑合约",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Search/ethscriptions.md",
    timestamp: "2023-12-9",
  },
  {
    content: "BRC20 解析",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Search/brc20.md",
    timestamp: "2023-11-29",
  },
  {
    content: "一个通用的套利交易模型",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Robot/TradeModel.md",
    timestamp: "2023-10-4",
  },
  {
    content: "选择什么语言编写智能合约",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Special/Language.md",
    timestamp: "2023-9-26",
  },
  {
    content: "比最小代理更小的代理合约",
    link: "https://github.com/33357/smartcontract-apps/blob/main/EIPS/smallerProxy.md",
    timestamp: "2023-9-17",
  },
  {
    content: "EIP7511 最小代理合约解析",
    link: "https://github.com/33357/smartcontract-apps/blob/main/EIPS/eip7511.md",
    timestamp: "2023-9-9",
  },
  {
    content: "uniswap-v4 fees&hooks 合约代码分析",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Apps/DEX/Uniswap_v4/fees&hooks.md",
    timestamp: "2023-9-1",
  },
  {
    content: "uniswap-v4 poolManager 合约分析",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Apps/DEX/Uniswap_v4/poolManager.md",
    timestamp: "2023-8-13",
  },
  {
    content: "uniswap_v4 core 合约结构解析",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Apps/DEX/Uniswap_v4/model.md",
    timestamp: "2023-8-6",
  },
  {
    content: "快速了解 uniswap_v4",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Apps/DEX/Uniswap_v4/quick.md",
    timestamp: "2023-7-29",
  },
  {
    content: "以太坊扩容：L2 详解",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Search/L2.md",
    timestamp: "2023-6-29",
  },
  {
    content: "Uniswap Universal Router 之 Permit2 合约分析",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Gas/UniswapUniversalRouter_Permit2.md",
    timestamp: "2023-5-2",
  },
  {
    content: "2023 年香港 web3 嘉年华",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Meeting/Web3HongKong.md",
    timestamp: "2023-4-17",
  },
  {
    content: "黑客松对开发者有什么用",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Meeting/Hackathon.md",
    timestamp: "2023-4-13",
  },
  {
    content: "如何预测最低的 GasPrice",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Solidity/Other/Lowest_GasPrice.md",
    timestamp: "2023-2-11",
  },
  {
    content: "Solidity 智能合约开发流程",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Solidity/Other/Solidity_Development_Process.md",
    timestamp: "2023-2-1",
  },
  {
    content: "NFT 所有者 tokenID 快速查询",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Solidity/Other/NFT_Search.md",
    timestamp: "2022-12-29",
  },
  {
    content: "MEV 是在为谁工作",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Robot/MEV_Who_are_you_working_for.md",
    timestamp: "2022-12-26",
  },
  {
    content: "如何入门智能合约开发",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Special/New.md",
    timestamp: "2022-12-17",
  },
  {
    content: "当去中心化遇到攻击: BSC 停机事件",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Event/WhenAttackDecentralization.md",
    timestamp: "2022-10-8",
  },
  {
    content: "又是用户转移资产权限被盗，如何确保加密资产安全？",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Event/ContractApproveHack.md",
    timestamp: "2022-10-2",
  },
  {
    content: "如何成为躺着赚钱的科学家",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Special/Scientist.md",
    timestamp: "2022-9-27",
  },
  {
    content: "ETHW 重放攻击",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Event/Replay.md",
    timestamp: "2022-9-19",
  },
  {
    content: "以太坊POS合并带来的赚钱机会",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Event/PosMerge.md",
    timestamp: "2022-9-16",
  },
  {
    content: "如何成为资深 solidity 智能合约工程师",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Special/Dev.md",
    timestamp: "2022-9-15",
  },
  {
    content: "如何在区块链领域用技术赚钱",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Special/Earn.md",
    timestamp: "2022-9-14",
  },
  {
    content: "交易回滚攻击",
    link: "https://github.com/33357/smartcontract-apps/tree/main/Solidity/Solidity_100/2_Transaction_Rollback_Attack",
    timestamp: "2022-8-13",
  },
  {
    content: "合约重入攻击",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Solidity/Solidity_100/1_Reentrancy_Attack",
    timestamp: "2022-7-27",
  },
  {
    content: "2022年中展望",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Outlook/2022_MidYear.md",
    timestamp: "2022-7-19",
  },
  {
    content: "CheapSwap 协议的诞生",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Event/CheapSwap.md",
    timestamp: "2022-6-28",
  },

  {
    content: "最省GAS链上排序",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Solidity/Other/Save_Gas_Sort.md",
    timestamp: "2022-6-13",
  },
  {
    content: "Compound CToken合约解析",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Apps/Loan/Compound/cToken_understand.md",
    timestamp: "2022-6-10",
  },
  {
    content: "Compound rateModel合约解析",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Apps/Loan/Compound/rateModel_understand.md",
    timestamp: "2022-6-7",
  },
  {
    content: "Compound 应用架构",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Apps/Loan/Compound/app_architecture.md",
    timestamp: "2022-6-1",
  },
  {
    content: "快速了解 Compound",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Apps/Loan/Compound/quick_understand.md",
    timestamp: "2022-5-29",
  },
  {
    content: "一个简单的抢跑机器人模型",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Robot/Running_Robot/Simple_Running_Robot.md",
    timestamp: "2022-5-9",
  },
  {
    content: "一个典型的三明治交易机器人模型",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Robot/Sandwich_Exchange_Robot/Simple_Sandwich_Exchange_Robot.md",
    timestamp: "2022-5-8",
  },
  {
    content: "链上通信协议，到底有什么用",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Event/OnChainMessageProtocol.md",
    timestamp: "2022-5-5",
  },
  {
    content: "在去中心化交易所和中心化交易所之间套利",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Robot/Moving_Exchange_Robot/Dex_Cex.md",
    timestamp: "2022-4-10",
  },
  {
    content: "X2Y2: 必须修改的中心化NFT挂单奖励机制",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Event/X2Y2_DecentralizedOrderReward.md",
    timestamp: "2022-3-8",
  },
  {
    content: "Uniswap-v2 Pair 合约分析",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Apps/DEX/Uniswap_v2/pair_understand.md",
    timestamp: "2022-3-2",
  },
  {
    content: "Uniswap-v2 Factory合约分析",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Apps/DEX/Uniswap_v2/factory_understand.md",
    timestamp: "2022-2-25",
  },
  {
    content: "Uniswap-v2 Router合约分析",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Apps/DEX/Uniswap_v2/router_understand.md",
    timestamp: "2022-2-20",
  },
  {
    content: "EIP1559 下的 GAS 费设置解析",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Event/EIP1559_GAS.md",
    timestamp: "2022-2-14",
  },
  {
    content: "RandomDAO 事件及其分析",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Event/RandomDAO.md",
    timestamp: "2022-2-8",
  },
  {
    content: "快速部署 Uniswap-v2",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Apps/DEX/Uniswap_v2/quick_deploy.md",
    timestamp: "2022-2-4",
  },
  {
    content: "使用官方项目部署 Uniswap-v2",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Apps/DEX/Uniswap_v2/official_deploy.md",
    timestamp: "2022-2-3",
  },
  {
    content: "快速了解 Uniswap-v2",
    link: "https://github.com/33357/smartcontract-apps/blob/main/Apps/DEX/Uniswap_v2/quick_understand.md",
    timestamp: "2022-1-30",
  },
];
</script>

<style>
.timeline-container {
  position: absolute;
  top: 10%;
  left: 45%;
  transform: translateX(-50%);
}

.large-font-timeline {
  font-size: 2em;
}
</style>

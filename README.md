# token-scanner 🔍

> cola um contrato — vê tudo sobre o token em tempo real.

Ferramenta de inteligência on-chain para tokens ERC-20 nas redes **Ethereum** e **Base** — combina dados direto do RPC, Etherscan API V2 e CoinGecko para gerar um perfil completo do token em segundos.

---

## o que faz

```
① CONTRATO   → nome, símbolo, decimais, verificado ou não
② SUPPLY     → supply total via RPC direto
③ PREÇO      → USD, variação 24h, market cap, volume
④ ATIVIDADE  → últimas transferências on-chain com links
```

---

## demo

🔗 **[virus4d.github.io/token-scanner](https://virus4d.github.io/token-scanner)**

---

## como usar

1. Seleciona a rede — **Ethereum** ou **Base**
2. Cola o endereço do contrato do token (`0x...`)
3. Clica **ESCANEAR**

exemplo de contratos para testar:
- USDC na Base: `0x833589fcd6edb6e08f4c7c32d4f71b54bda02913`
- USDC no Ethereum: `0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48`
- DAI no Ethereum: `0x6b175474e89094c44da98b954eedeac495271d0f`

---

## stack

```
Ethereum RPC     → eth_call direto no browser (sem CORS)
Base RPC         → mainnet.base.org
Etherscan API V2 → contrato verificado + transferências
CoinGecko API    → preço, market cap, volume 24h
corsproxy.io     → proxy CORS para APIs externas
Vanilla JS       → sem frameworks, sem dependências
```

---

## projetos relacionados

| tool | descrição | link |
|------|-----------|------|
| 🔍 token-scanner | analisa tokens ERC-20 on-chain | você está aqui |
| 🤖 defi-agent-v0 | agente IA que analisa wallets na Base | [ver repo](https://github.com/virus4D/defi-agent-v0) |
| 📊 wallet-lens | scan de transações ETH on-chain | [ver repo](https://github.com/virus4D/wallet-lens) |

---

## o que aprendi construindo isso

- `eth_call` direto no browser funciona perfeitamente — zero CORS
- CoinGecko aceita endereço de contrato diretamente — não precisa do slug
- ABI decode manual de `string` vs `bytes32` são diferentes — aprendi na marra
- CORS ainda é o primeiro chefe de todo dev Web3

---

<div align="center">

construindo em público · errando em público · chegando lá

[![X](https://img.shields.io/badge/@Virus__4D-000000?style=flat-square&logo=x&logoColor=cc0000)](https://x.com/Virus_4D)
[![GitHub](https://img.shields.io/badge/virus4D-000000?style=flat-square&logo=github&logoColor=cc0000)](https://github.com/virus4D)

</div>

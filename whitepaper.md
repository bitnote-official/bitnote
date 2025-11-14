# BitNote: Bitcoin como Nota Física
**Bearer Assets Off-Chain com Secure Elements**

**Autor:** [SEU NOME AQUI]  
**Data:** 13 de novembro de 2025  
**GitHub:** github.com/bitnote-official/bitnote  
**Site:** bitnote-official.github.io/bitnote  
**Licença:** MIT — Use, modifique, fabrique livremente  

---

## Resumo
Dispositivo open-source com **50–100 chaves privadas independentes** em secure element.  
Transferência **NFC off-chain**, sem internet, sem taxa, com **apagamento irreversível**.  
Troco físico em satoshis. **100% não-custodial**.

---

## Problema
Bitcoin não é dinheiro de bolso:  
- Transações on-chain: lentas e caras  
- Lightning: precisa de internet  
- Ecash: custodial  

---

## Solução: BitNote
- **Hardware:** ESP32-S3 + ATECC608B + PN532 (NFC)  
- **50 chaves × 2.500 sats** (~$2,50)  
- **Transferência atômica:** prova de posse → wipe no emissor  
- **Off-chain total** — como passar uma nota

---

## Protocolo
1. A → B: `slot_id`, `address`, `ECDSA signature`  
2. B verifica → armazena no secure element  
3. B confirma → A apaga slot  
4. LED: "Transferência concluída"

---

## Comparação

| Projeto | Multi-chaves | Off-chain | Não-custodial | NFC | Wipe |
|--------|--------------|-----------|---------------|-----|------|
| Opendime | 1 | Yes | Yes | No | Yes |
| Cashu | Yes (tokens) | Yes | No | Yes | No |
| **BitNote** | **50–100** | **Yes** | **Yes** | **Yes** | **Yes** |

---

## Roadmap
- **Q1 2026:** Protótipo funcional  
- **Q2 2026:** Testes em meetups  
- **Q3 2026:** Fábrica comunitária

---

**Este projeto é open-source no espírito do Bitcoin.**  
Contribua, fork, fabrique, melhore.  
**Crédito ao criador original é apreciado, mas não obrigatório.**

---

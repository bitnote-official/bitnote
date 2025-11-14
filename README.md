BitNote: Bitcoin como nota fisica
=================================

Descricao:
Dispositivo open-source com 50-100 chaves privadas independentes em
secure element. Cada chave carrega 2500 satoshis (~$2,50 em 13/11/2025).
Transferencia local via NFC, off-chain, sem internet, sem taxa.
Apagamento irreversivel no emissor. 100% nao-custodial, 100% privado.
Criptografia pos-quantica (Dilithium + Kyber) integrada.

Objetivo:
Viabilizar troco fisico em Bitcoin com a mesma praticidade de uma
nota de papel.

Links:
- Site: https://bitnote.org (em construcao)
- Whitepaper: whitepaper.pdf
- Timestamp blockchain: docs/whitepaper.pdf.ots
- Licenca: MIT

Hardware (custo ~R$175/unidade):
- ESP32-S3
- ATECC608B (secure element EAL5+)
- PN532 (NFC 13.56 MHz)
- Bateria LiPo 500mAh
- LED + Botao

Protocolo de transferencia atomica (NFC):
1. A seleciona slots
2. A envia: endereco + assinatura ECDSA/Dilithium
3. B verifica e armazena
4. B confirma
5. A apaga slots (wipe irreversivel)

Criptografia pos-quantica (PQC):
- Assinatura: CRYSTALS-Dilithium
- Troca de chaves: CRYSTALS-Kyber
- Hash: SHA-3-256
Implementacao: biblioteca pqm4 (otimizada para MCU)

Roadmap:
- Q1/2026: Prototipo funcional
- Q2/2026: Firmware com PQC + testes NFC
- Q3/2026: Producao comunitaria

Contribuicoes:
- Issues: github.com/bitnote-official/bitnote/issues
- Pull Requests: github.com/bitnote-official/bitnote/pulls

Licenca MIT
Copyright (c) 2025 bitnote-official
Qualquer um pode usar, modificar, fabricar ou vender.
Credito ao criador e apreciado, mas nao obrigatorio.

BitNote e o dinheiro fisico que o Bitcoin sempre quis ser.

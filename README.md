# 🔐 Criptografia Simétrica vs. Assimétrica

## 📘 Conceitos Fundamentais

### 🔑 Criptografia Simétrica

A criptografia simétrica utiliza **uma única chave secreta** para **criptografar e descriptografar** os dados. Essa chave deve ser **mantida em sigilo absoluto** entre as partes que se comunicam.

- **Mesma chave** para cifrar e decifrar
- Exige troca segura da chave entre remetente e destinatário
- Alta performance: algoritmos geralmente mais rápidos
- Vulnerável se a chave for interceptada durante a troca

**Algoritmos comuns:**
- AES (Advanced Encryption Standard)
- DES (Data Encryption Standard)
- Triple DES (3DES)

**Exemplo de uso:**
- Criptografia de arquivos locais
- Comunicação segura em redes privadas (VPNs)
- HTTPS (em conjunto com TLS após troca de chave)

![image](https://github.com/user-attachments/assets/b3d5492b-fe52-48bd-9a5b-489b7541c69c)



---

### 🔐 Criptografia Assimétrica

Na criptografia assimétrica, são usados dois elementos distintos:

- **Chave pública**: usada para **criptografar**
- **Chave privada**: usada para **descriptografar**

As chaves são matematicamente relacionadas, mas **não é possível derivar a chave privada a partir da pública** com os recursos computacionais disponíveis atualmente.

- Não é necessário trocar chaves secretas previamente
- Maior segurança para comunicação entre desconhecidos
- Mais lenta que a simétrica, devido à complexidade matemática

**Algoritmos comuns:**
- RSA (Rivest–Shamir–Adleman)
- ECC (Elliptic Curve Cryptography)
- ElGamal

**Exemplo de uso:**
- Troca segura de chaves em HTTPS (TLS)
- Assinaturas digitais
- E-mails criptografados (ex: PGP)
- Autenticação (ex: SSH)

---

## 📊 Comparação

| Característica                | Criptografia Simétrica       | Criptografia Assimétrica        |
|------------------------------|------------------------------|----------------------------------|
| Número de chaves             | 1 (compartilhada)            | 2 (pública e privada)            |
| Velocidade                   | Alta                         | Mais lenta                       |
| Complexidade matemática      | Baixa                        | Alta                             |
| Troca segura de chave        | Necessária                   | Não é necessária                 |
| Uso típico                   | Grandes volumes de dados     | Troca de chave, autenticação     |
| Escalabilidade (n usuários)  | Difícil: exige n² chaves     | Fácil: cada usuário tem 1 par    |

---

## 🧠 Estratégia Combinada: Híbrida

Sistemas modernos (como HTTPS) **combinam criptografia simétrica e assimétrica**:

1. A chave simétrica é gerada aleatoriamente
2. Ela é enviada ao destinatário **criptografada com chave pública** (assimétrica)
3. Após isso, os dados são trocados usando criptografia simétrica (mais rápida)

Essa abordagem traz o melhor dos dois mundos: **segurança e performance**.

---

## ✅ Conclusão

- Use **criptografia simétrica** quando performance for essencial e as partes confiarem mutuamente.
- Use **criptografia assimétrica** para comunicação segura entre partes que **não compartilham uma chave previamente**.
- Para segurança robusta e eficiência, **combine os dois métodos** (criptografia híbrida).

---

📄 **Este conteúdo é baseado em fundamentos criptográficos amplamente reconhecidos e validados.**

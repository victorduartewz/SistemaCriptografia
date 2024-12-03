# 🔒 Sistema de Criptografia e Descriptografia 

Este projeto implementa um sistema cliente-servidor que permite criptografar e descriptografar mensagens utilizando métodos de criptografia **padrão**, **simétrica** e **assimétrica**. Ele também demonstra conceitos de redes, sockets e segurança de dados.

## 🚀 Objetivo

Fornecer um ambiente interativo para aprendizado e prática de técnicas de criptografia e manipulação de mensagens em um sistema distribuído.

## 🛠️ Estrutura do Repositório

```bash
📂 SistemaCriptografia/
│
├── cliente.py   # Código do cliente para interagir com o servidor
├── servidor.py  # Código do servidor para processar as mensagens
└── README.md    # Documentação do projeto
```

## 📚 Funcionalidades

### Cliente
- Conecta-se ao servidor por meio de um socket TCP.
- Permite ao usuário:
  - Criptografar mensagens.
  - Descriptografar mensagens.
  - Escolher o tipo de criptografia: padrão, simétrica ou assimétrica.
- Envia os dados ao servidor e exibe os resultados retornados.

### Servidor
- Recebe mensagens do cliente e processa as operações de criptografia/descriptografia.
- Implementa:
  - **Criptografia padrão:** Deslocamento fixo nos caracteres.
  - **Criptografia simétrica:** Deslocamento baseado em uma chave fornecida pelo usuário.
  - **Criptografia assimétrica:** Usa chaves RSA geradas dinamicamente.
- Responde ao cliente com o resultado e um relógio lógico.

## 🔧 Tecnologias Utilizadas

- **Python 3.x**
- **Biblioteca `socket`:** Para comunicação cliente-servidor.
- **Biblioteca `cryptography`:** Para criptografia assimétrica.
- **Threads:** Para suporte a múltiplos clientes simultâneos.

## 🏁 Como Executar

### Pré-requisitos
- Certifique-se de ter o Python 3.x instalado.
- Instale a biblioteca `cryptography`:
  ```bash
  pip install cryptography
  ```

### Passo a Passo
1. Clone o repositório:
   ```bash
   git clone https://github.com/SeuUsuario/SistemaCriptografia.git
   cd SistemaCriptografia
   ```

2. Inicie o servidor:
   ```bash
   python servidor.py
   ```

3. Em outro terminal, inicie o cliente:
   ```bash
   python cliente.py
   ```

4. Siga as instruções interativas do cliente para criptografar ou descriptografar mensagens.

## 💻 Exemplo de Uso

### Cliente
```text
Escolha uma opção:
1 - Criptografar mensagem
2 - Descriptografar mensagem
3 - Sair
Opção: 1
Insira a mensagem: Olá Mundo
Tipo (padrao/simetrica/assimetrica): padrao
Insira a chave (para simétrica, deixe em branco para outras): 

Resultado: Roá#Pxqgr
Relógio lógico: 1690934645.567
```

### Servidor
```text
Servidor ouvindo em 192.168.43.6:7890
Conectado a ('192.168.43.7', 54567)
Desconectado de ('192.168.43.7', 54567)
```

## 🔒 Métodos de Criptografia

- **Padrão:** Desloca cada caractere da mensagem por um valor fixo (3).
- **Simétrica:** Desloca os caracteres com base em uma chave fornecida.
- **Assimétrica:** Utiliza chaves públicas e privadas geradas dinamicamente.

## 📝 Licença

Este projeto está licenciado sob a licença MIT. Consulte o arquivo [LICENSE](LICENSE) para mais detalhes.

## 🤝 Contribuições

Contribuições são bem-vindas! Abra _issues_ para relatar problemas ou sugerir melhorias.
```

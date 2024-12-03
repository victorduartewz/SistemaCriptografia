# 🔒 Encryption and Decryption System

This project implements a client-server system that allows encrypting and decrypting messages using **padrão**, **simétrica** and **assimétrica** encryption methods. It also demonstrates concepts of networking, sockets and data security.

## 🚀 Objective

Provide an interactive environment for learning and practicing encryption techniques and message handling in a distributed system.

## 🛠️ Repository Structure

```bash
📂 SistemaCriptografia/
│
├── cliente.py   # Client code to interact with the server
├── servidor.py  # Server code to process messages
└── README.md    # Project documentation
```

## 📚 Features

### Client
- Connects to the server via a TCP socket.
- Allows the user to:
  - Encrypt messages.
  - Decrypt messages.
  - Choose the encryption type: padrão, simétrica, or assimétrica.
- Sends data to the server and displays the returned results.

### Server
- Receives messages from the client and performs encryption/decryption operations.
- Implements:
  - **Padrão encryption:** Fixed character offset.
  - **Simétrica encryption:** Offset based on a user-provided key.
  - **Assimétrica encryption:** Uses dynamically generated RSA keys.
- Responds to the client with the result and a logical clock.

## 🔧 Technologies Used

- **Python 3.x**
- **Library `socket`:** For client-server communication.
- **Library `cryptography`:** For asymmetric encryption.
- **Threads:** To support multiple simultaneous clients.

## 🏁 How to Run

### Prerequisites
- Make sure you have Python 3.x installed.
- Install the library `cryptography`:
  ```bash
  pip install cryptography
  ```

### Step-by-Step
1. Clone the repository:
   ```bash
   git clone https://github.com/victorduartewz/SistemaCriptografia.git
   cd SistemaCriptografia
   ```

2. Start the servidor:
   ```bash
   python servidor.py
   ```

3. In another terminal, start the cliente:
   ```bash
   python cliente.py
   ```

4. Follow the interactive instructions in the cliente to encrypt or decrypt messages.

## 💻 Usage Example

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

## 🔒 Encryption Methods

- **Padrão:** Shifts each character in the message by a fixed amount (3).
- **Simétrica:** Shifts characters based on a provided key.
- **Assimétrica:** Uses dynamically generated public and private keys.

## 📝 License

This project is licensed under the MIT License. See the [LICENSE] file for more details.

## 🤝 Contributions

Contributions are welcome! Please open _issues_ to report problems or suggest improvements.

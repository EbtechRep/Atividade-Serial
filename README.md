# 🛠️ Comunicação Serial com RP2040, UART, SPI e I2C  

## 📜 Descrição do Projeto  

Este projeto foi desenvolvido para consolidar os conceitos relacionados ao uso de interfaces de comunicação serial no RP2040. Utilizando a placa de desenvolvimento BitDogLab, a aplicação funcional manipula LEDs comuns e endereçáveis WS2812, além de tratar entradas de botões com debouncing via software. O projeto também explora o uso de UART e I2C para exibição de caracteres em um display SSD1306 e envio de informações via Serial Monitor.

## 🎯 Objetivos  

- **Compreender** o funcionamento da comunicação serial em microcontroladores. 
- **Aplicar UART e I2C** na comunicação com periféricos. 
- **Manipular LEDs** comuns e endereçáveis WS2812.
- **Implementar debouncing** para botões via software.
- **Exibir caracteres** no display SSD1306 via comunicação I2C.
- **Enviar informações** ao Serial Monitor utilizando UART.
- **Integrar hardware e software** em uma aplicação funcional.  

---

## 🚀 Componentes Utilizados  

- **Placa BitDogLab com microcontrolador RP2040**  
- **Matriz 5x5 de LEDs WS2812** (conectada à GPIO 7)  
- **LED RGB** (pinos conectados às GPIOs 11, 12 e 13)  
- **Botão A** (conectado à GPIO 5)  
- **Botão B** (conectado à GPIO 6)
- **Display OLED SSD1306** (conectado via I2C nas GPIOs 14 e 15)  

---

## ⚡ Funcionalidades  

1. **LED RGB:** Estática
2. **Botão A:** Alterna o estado do LED Verde (ligado/desligado) e exibe a informação no display SSD1306 e no Serial Monitor.  
3. **Botão B:** Alterna o estado do LED Azul (ligado/desligado) e exibe a informação no display SSD1306 e no Serial Monitor.  
4. **Matriz WS2812:** Exibe números de 0 a 9 com formato digital fixo.
5. **Entrada Serial:** Caracteres digitados no Serial Monitor são exibidos no display SSD1306.
6. **Modificação da Biblioteca font.h:** Inclusão de caracteres minúsculos personalizados.

---

## 📂 Estrutura do Repositório  

```plaintext
Serial/
├── src/                       # Código-fonte principal
│   ├── Serial.c               # Funções para controle dos LEDs
│   └── ssd1306.c              # Funções para tratamento dos botões
    └── ws2818b.pio            # Código para comunicação com LEDs WS2812
├── include/                   # Arquivos de cabeçalho
│   ├── font.h                 # Declarações para os caracteres
│   └── ssd1306.h              # Declarações para botões
    └── ws2818b.pio.h          
├── cMakeLists.txt             # Configurações de compilação do projeto
└── README.md                  # Documentação do projeto
```

## 🛠️ Dependências

- **CMake** - Gerador de builds 
- **Ninja** - Ferramenta de build rápida 
- **Python 3** - Interpretador Python

#### Download das Dependências caso não possua:
1. [**Cmake**](https://cmake.org/download/)
2. [**Ninja**](https://github.com/ninja-build/ninja/releases)
3. [**Python3**](https://www.python.org/downloads/)

## 🔧 Instalação
###   Adicionar Ninja, CMake e Python ao Path do Sistema  

Para que os comandos **Ninja**, **CMake** e **Python** sejam reconhecidos em qualquer terminal, siga estas etapas:  

1. **Abra as Configurações do Sistema:**  
   - Clique com o botão direito no botão **Iniciar** e selecione **Configurações**.  
   - Vá em **Sistema → Sobre → Configurações Avançadas do Sistema** (no lado direito).  

2. **Acesse as Variáveis de Ambiente:**  
   - Na aba **Avançado**, clique em **Variáveis de Ambiente**.  
   - Na seção **Variáveis do Sistema**, localize a variável `Path` e clique em **Editar**.  

3. **Adicione os Caminhos dos Programas:**  

   - **Ninja:**  
     Clique em **Novo** e insira o caminho onde você extraiu o `ninja.exe`. Exemplo:  
     ```
     C:\Users\SeuUsuario\Downloads\ninja-win
     ```  

   - **CMake:**  
     Clique em **Novo** e adicione o diretório `bin` do CMake. Exemplo:  
     ```
     C:\Program Files\CMake\bin
     ```  

   - **Python:**  
     Clique em **Novo** e adicione o diretório onde o Python foi instalado. Exemplo:  
     ```
     C:\Python39\
     ```  

4. **Salve as Alterações:**  
   - Clique em **OK** em todas as janelas para salvar as configurações.  

5. **Verifique as Instalações:**  

   Abra o terminal e digite os seguintes comandos para garantir que estão configurados corretamente:  

   ```bash
   ninja --version
   cmake --version
   python --version


## 🖱️ Como executar

### Abra o terminal e siga os passos abaixo:


1. Clone este repositório:

   ```bash
   git clone https://github.com/EbtechRep/Comunicaoo-Serial.git
   ```
2. Importe o projeto pela extensão do **Rasquery Pi Pico Project**

3. Acesse o diretório do projeto:

   ```bash
   cd Serial
   ```

3. Instale a pasta **build**

   ```bash
    mkdir build
   ```

4. Acesse o diretório **build**

   ```bash
   cd build
   ```
5. Compile o projeto com CMake e Ninja:
   ```bash
   cmake -G "Ninja" ..
   ```   
6. Execute a compilação:
   ```bash
   ninja
   ```   
## 💻 Video demonstrativo: 
**https://youtu.be/oM2irT_2trE?si=3BJuq3lxFzsMzeF1**
 









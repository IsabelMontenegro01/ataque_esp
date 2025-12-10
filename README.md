# Servidor Web ESP32 para Análise de Vulnerabilidades (Pentest IoT)

###  Integrantes:

- <a href="https://www.linkedin.com/in/christian-gandra/">Christian Gandra</a>
- <a href="https://www.linkedin.com/in/giovanna-neves-rodrigues/">Giovanna Neves</a>
- <a href="https://www.linkedin.com/in/isabel-montenegro01/">Isabel Montenegro</a>
- <a href="https://www.linkedin.com/in/paulo-henrique0601/">Paulo Henrique</a>
- <a href="https://www.linkedin.com/in/samuel-vono/">Samuel Vono</a>
- <a href="https://www.linkedin.com/in/tobias-viana/">Tobias Viana</a>
- <a href="https://www.linkedin.com/in/vitor-lopes-91763b34a/">Vitor Lopes</a>

### Professora:
- <a href="https://www.linkedin.com/in/crishna-irion-7b5aa311/">Crishna Irion</a>


### Objetivo da ponderada em sala 

&emsp; No cenário atual de rápida expansão da Internet das Coisas (IoT), a segurança cibernética de dispositivos embarcados ( edge devices) tornou-se uma preocupação crítica. Muitos projetos de IoT, desenvolvidos com foco primário em funcionalidade e rapidez de implementação, negligenciam as melhores práticas de segurança, resultando em vulnerabilidades que podem ser exploradas com facilidade.

&emsp; Este projeto visa abordar essa lacuna por meio de uma atividade de Teste de Penetração (Pentest) prático e controlado. Implementamos um Servidor Web Básico utilizando o microcontrolador ESP32 e o ambiente de desenvolvimento Arduino IDE. A aplicação serve para controlar duas saídas digitais (LEDs) acessíveis via rede local.

&emsp; O objetivo fundamental deste repositório não é a funcionalidade, mas sim servir como um alvo realista e vulnerável. O código-fonte foi intencionalmente configurado com fraquezas comuns para permitir a identificação, exploração e documentação de riscos de segurança em dispositivos IoT, como a falta de autenticação e a comunicação não criptografada.

&emsp; Este exercício prático simula cenários de ataque reais, proporcionando insights valiosos sobre a importância da análise estática, da avaliação de risco e da implementação de contramedidas robustas em soluções de IoT.

---
##  Visão Geral

O projeto consiste em:
* **Hardware:** Um módulo ESP32 conectado a dois LEDs e resistores.
* **Software:** Código em C/C++ (Arduino Sketch) que configura o ESP32 como um servidor HTTP na porta 80.
* **Funcionalidade:** O acesso ao endereço IP do ESP32 exibe uma página web com botões para ligar e desligar os LEDs conectados aos GPIOs.

### Componentes Necessários (Hardware)

* 1 x Placa de Desenvolvimento ESP32
* 2 x LEDs de 5mm
* 2 x Resistores de 330 Ohm
* 1 x Protoboard
* Fios Jumper

##  Configuração e Instalação

### Pré-requisitos

1.  Arduino IDE instalada.
2.  Add-on da placa ESP32 instalado na Arduino IDE.
3.  Conhecimento básico em redes (endereço IP, SSID, etc.).

### Passos de Compilação e Upload

1.  **Obter o Código:** Clone este repositório ou copie o arquivo de código.
2.  **Configurar Credenciais:** No código, substitua `REPLACE_WITH_YOUR_SSID` e `REPLACE_WITH_YOUR_PASSWORD` pelas credenciais da sua rede Wi-Fi.
    ```cpp
    const char* ssid = "Seu_SSID";
    const char* password = "Sua_Senha";
    ```
3.  **Compilar e Enviar:**
    * Selecione a placa ESP32 correta (ex: ESP32 Dev Module) e a porta COM.
    * Clique em **Fazer Upload** na Arduino IDE.
4.  **Encontrar o IP:** Após o upload, abra o Monitor Serial (baud rate 115200) e pressione o botão EN/RESET no ESP32. O endereço IP do servidor será exibido.

### Acesso

Abra qualquer navegador e acesse o endereço IP obtido no Monitor Serial (ex: `http://192.168.1.135`).

### Resultados dos testes

&emsp; Com o projeto em funcionamento, foram realizados testes de segurança para a análise de vulnerabilidades e riscos. Os resultados detalhados desses testes, incluindo as evidências dos ataques e a avaliação de risco, podem ser acessados no arquivo [Nome do Arquivo/Link].
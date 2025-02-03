# Implementação da Máquina de Controle de uma CPU em VHDL ⚙️

Projeto desenvolvido para a implementação da **máquina de controle** de uma **CPU** fornecida, utilizando **VHDL** e testando a implementação no **simulador Quartus**, utilizando a FPGA **DE0_CV**.

---

[**Introdução**](#introdução-) · [**Objetivo do Projeto**](#objetivo-do-projeto-) · [**Arquitetura da CPU**](#arquitetura-da-cpu-) · [**Estrutura do Projeto**](#estrutura-do-projeto-) · [**Instalação e Configuração**](#instalação-e-configuração-) · [**Materiais de Referência**](#materiais-de-referência-)

---

## Introdução 📜

Neste projeto, implementamos a **máquina de controle** de um processador baseado em **VHDL**, responsável por gerenciar os estados do processador, executar instruções e manipular o fluxo de dados dentro da CPU.  
A implementação foi testada no **Quartus** usando a pasta **DE0_CV** para simulação e verificação da lógica.

---

## Objetivo do Projeto 🎯

A proposta deste projeto é:
- Implementar a **máquina de controle** do processador fornecido em **VHDL**.  
- Garantir a execução correta das **instruções do processador**.  
- Simular e testar a implementação utilizando o **Quartus** na pasta **DE0_CV**.  

A CPU conta com um **banco de registradores, unidade lógica e aritmética (ULA), controlador de memória e interface com vídeo**, permitindo a execução de diversas instruções.

---

## Arquitetura da CPU 🖥️

A CPU implementada possui os seguintes componentes principais:

- **Banco de Registradores:** Contém **8 registradores** de 16 bits para armazenar dados temporários.
- **ULA (Unidade Lógica e Aritmética):** Responsável por operações matemáticas e lógicas.
- **Máquina de Controle:** Define os estados do processador (**fetch, decode, exec, halted**).
- **Sinais de Controle:**  
  - **M1, M5, RW:** Controle de memória.  
  - **PC, IR, MAR, SP:** Registradores internos.  
  - **Videoflag, VGA_Pos, VGA_Char:** Interface de saída de vídeo.  
  - **Key:** Entrada do teclado.  

---

## Estrutura do Projeto 📂

A estrutura do projeto é organizada da seguinte forma:
  ```bash
📂 CPU
│-- 📂 DE0_CV # Arquivos para simulação no Quartus
│-- 📜 cpu.vhd # Implementação principal da CPU em VHDL
│-- 📜 README.md # Documentação do projeto
  ```


---

## Instalação e Configuração 💾

### 1️⃣ **Requisitos**
Para rodar o projeto, você precisará:
- **Quartus Prime** (Intel FPGA Software)
- **ModelSim** (para simulação VHDL)
- **Ambiente Linux ou Windows** com suporte para compilação VHDL

### 2️⃣ **Passos para Instalação**
1. Clone o repositório e entre no diretório do projeto:
  ```bash
   git clone https://github.com/SeuUsuario/CPU_VHDL_Project.git  
   cd CPU_VHDL_Project/
  ```

2. Abra o Quartus e carregue o projeto:

   - Execute o Quartus Prime.  
   - Vá em **File > Open Project** e selecione `DE0_CV/DE0_CV.qpf`.

3. Compile o código:

   - No Quartus, clique em **Compile Design**.  
   - Aguarde a compilação da CPU.

4. Simule o comportamento da CPU:

   - Abra o **ModelSim**.  
   - Carregue o arquivo de testbench (`DE0_CV/testbench.vhd`).  
   - Execute a simulação para visualizar o funcionamento da CPU.

---

## Materiais de Referência 📚

📌 **Links Úteis**
- [Documentação do Quartus Prime](https://www.intel.com/content/www/us/en/software/programmable/quartus-prime/overview.html)
- [Introdução ao VHDL](https://www.nandland.com/vhdl/)
- [Simulação com ModelSim](https://www.intel.com/content/www/us/en/software/programmable/quartus-prime/model-sim.html)

# Sistema de Controle de Ponto

Este projeto é um sistema simples de **registro de ponto eletrônico** para colaboradores de uma empresa. Ele simula a entrada e saída de funcionários (efetivos e estagiários), calcula o total de horas trabalhadas e gera um relatório com o saldo de horas.

## 🛠️ Funcionalidades

- Registro de ponto com entrada e saída de colaboradores.
- Cálculo de horas trabalhadas.
- Comparação com a carga horária obrigatória diária.
- Geração de relatório em console e arquivo `.txt`.

## 📦 Estrutura do Projeto

O projeto segue os princípios de arquitetura em camadas com os seguintes pacotes:

- `Model`: Contém as classes que representam os dados (Colaborador, Efetivo, Estagiario, RegistroDePonto).
- `Controller`: Responsável pela lógica de negócio (SistemaPontoController).
- `View`: Responsável pela apresentação e geração do relatório (RelatorioView, Main).

## 🧠 Conceitos de POO utilizados

O projeto utiliza diversos conceitos de **Programação Orientada a Objetos**, incluindo:

### ✅ Encapsulamento
- Os atributos das classes são privados e acessados através de métodos públicos (`getters`).
- A lógica de negócio está separada da interface com o usuário.

### ✅ Herança
- A classe `Colaborador` é abstrata e serve como base para `Efetivo` e `Estagiario`.
- Ambas as subclasses herdam os atributos e comportamentos da superclasse.

### ✅ Polimorfismo
- O método `getTipo()` é sobrescrito por `Efetivo` e `Estagiario`.
- O sistema trata objetos `Colaborador` de forma genérica, respeitando suas implementações específicas.

### ✅ Abstração
- A classe abstrata `Colaborador` define a estrutura comum para todos os colaboradores, mas deixa a responsabilidade de implementação de detalhes para as subclasses.
- A interface `Registravel` define o comportamento padrão para qualquer entidade que possa registrar ponto.

## 📄 Exemplo de Saída no Relatório

<p> REGISTRO DE PONTO </p>
-------------------
- Colaborador: João Silva
- Ocupação: Efetivo
- Entrada: 2025-05-01 - Horário: 08:00
- Saída: 2025-05-01 - Horário: 17:00
- Horas Trabalhadas: 9.00h
- Saldo de Horas: 1.00h


## 📁 Arquivo de Saída

Um arquivo chamado `sistemaPonto.txt` é gerado automaticamente com o conteúdo do relatório.


### Projeto desenvolvido para aula de POO com Java

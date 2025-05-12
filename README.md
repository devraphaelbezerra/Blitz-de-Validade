# 📅 Blitz de Validade - Monitoramento Preventivo de Produtos Vencidos
Este repositório contém o processo **Blitz de Validade**, desenvolvido no **Fluig** para execução semanal nas lojas, com o objetivo de identificar e registrar produtos vencidos nas gôndolas. O processo envolve diversas áreas como **repositores, embaladores, gerentes e auxiliares**, promovendo a responsabilidade coletiva pela qualidade dos produtos expostos.

---

## 🎯 Objetivo
- Promover a verificação proativa de produtos vencidos diretamente nas gôndolas.
- Registrar produtos com validade vencida em tempo real através do celular.
- Enviar **alertas automáticos por e-mail** ao comprador responsável da categoria (sessão, grupo, subgrupo, departamento) para ação imediata.

---

## 🕒 Funcionamento
- Toda **terça-feira às 14h**, os colaboradores envolvidos iniciam a verificação nas gôndolas com seus **aparelhos celulares**.
- Cada participante escaneia o **código de barras** do produto.
- O sistema consulta automaticamente:
  - Código do item
  - Descrição
- Em seguida, o usuário informa:
  - **Quantidade** do produto identificado
  - **Data de validade**
- Caso a validade esteja **vencida**, é gerado:
  - Um **registro da ocorrência**
  - Um **e-mail de alerta** direcionado ao **comprador da categoria correspondente**

![image](https://github.com/user-attachments/assets/dd36c2c9-5213-4068-824a-362c4c03f121)

---

## 🛠️ Tecnologias Utilizadas
- **Fluig ECM**
- **Mobile Web (responsivo)**
- **Leitor de Código de Barras (câmera do celular)**
- **Banco de Dados (consultas via dataset Fluig)**
- **Sistema de Notificações por E-mail**

---

## 📡 Exemplo de Fluxo
![image](https://github.com/user-attachments/assets/67d4004e-418f-4326-8d85-b29ae005f15e)

1. **Escaneamento do Produto**  
   Código de Barras: `7891234567890`  
   Produto: "Leite Integral 1L"

2. **Informações preenchidas**  
   - Quantidade: `4`
   - Data de Validade: `2024-12-01`

3. **Validade verificada como VENCIDA**  
   ✔️ Registro criado  
   📧 E-mail disparado para: `comprador.laticinios@empresa.com`

---

## 📬 Exemplo de Alerta por E-mail
> **Assunto:** Alerta - Produto Vencido na Gôndola  
>  
> Prezado(a),  
>  
> Foi identificado um produto vencido durante a Blitz de Validade:  
> - Produto: Leite Integral 1L  
> - Código: 7891234567890  
> - Quantidade: 4  
> - Validade: 01/12/2024  
> - Sessão: Laticínios  
>  
> Solicitamos ação imediata.  
>  
> Atenciosamente,  
> Sistema Blitz de Validade Fluig.

---

## 🧠 Benefícios
- Redução de perdas por vencimento
- Melhoria na imagem da loja perante o consumidor
- Engajamento das equipes na qualidade do PDV
- Comunicação direta e automatizada com os compradores

---

## 👨‍💻 Autor

Desenvolvido por [Raphael Bezerra](https://github.com/devraphaelbezerra)  
Analista de Sistemas focado em automações operacionais e processos preventivos no varejo.

---

## 📁 Estrutura Sugerida do Repositório

- `src/` - Scripts do formulário e eventos do Fluig
- `workflow/` - Modelagem do processo
- `notificacoes/` - Templates de e-mails
- `docs/` - Documentação e manual de uso

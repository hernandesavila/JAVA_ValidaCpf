# 🧾 Valida CPF

Valida CPF é um aplicativo **Java Swing** desenvolvido com suporte do **NetBeans** para validar números de CPF e gerar dígitos verificadores corretos.

A interface apresenta duas abas: uma para verificar um CPF completo informado pelo usuário e outra para calcular um CPF válido a partir de 9 dígitos base.

---

## 🛠️ Tecnologias Utilizadas

<p align="center">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" alt="Java" width="30" height="30"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/apache/apache-original.svg" alt="Apache Ant" width="30" height="30"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/netbeans/netbeans-original.svg" alt="NetBeans" width="30" height="30"/>
</p>

- **Java 8+** – linguagem principal
- **Swing** – interface gráfica com abas, campos de texto e botões
- **NetBeans** – IDE utilizada na criação do formulário (`.form`) e do código gerado
- **Apache Ant** – script `build.xml` para compilar e executar o projeto fora da IDE

---

## 📂 Estrutura do Projeto

- `ValidaCpf/build.xml` – script Ant criado pelo NetBeans para compilar/empacotar
- `ValidaCpf/src/validacpf/GuiValidaCpf.java` – janela principal com regras de validação/geração
- `ValidaCpf/src/validacpf/GuiValidaCpf.form` – layout do formulário gerado pelo GUI Builder
- `ValidaCpf/dist/ValidaCpf.jar` – artefato compilado pronto para execução
- `ValidaCpf/manifest.mf` – define a classe principal do aplicativo

---

## ✅ Pré-requisitos

- **Java SE Development Kit 8+** instalado e configurado no `PATH`
- (Opcional) **NetBeans 8** ou superior para edição visual do formulário
- Permissão para executar aplicações desktop Java

---

## ⚙️ Configuração

1. **Abrir no NetBeans (opcional)**
   - Importe a pasta `ValidaCpf` como projeto existente com Ant.
   - O arquivo `.form` é reconhecido automaticamente pelo GUI Builder.

2. **Executar via Ant**
   - No terminal, navegue até `ValidaCpf/` e utilize `ant run` para compilar e iniciar o app.
   - Utilize `ant clean` para remover classes compiladas e artefatos temporários.

3. **Atualizar dados da interface**
   - Textos, mensagens e rótulos podem ser alterados diretamente em `GuiValidaCpf.java`.

---

## 🛠️ Compilação

1. Garanta que o JDK esteja instalado.
2. No diretório `ValidaCpf/`, execute `ant clean jar` para gerar `dist/ValidaCpf.jar`.
3. O processo cria as pastas `build/` (classes compiladas) e `dist/` (artefatos executáveis).

---

## ▶️ Execução

1. Via NetBeans: clique em **Run** no projeto `ValidaCpf`.
2. Via terminal: `java -jar dist/ValidaCpf.jar` após a compilação.
3. Aba **Verificar CPF**: informe 11 dígitos e clique em **Verificar** para validar o documento.
4. Aba **Gerar CPF**: insira 9 números e pressione **Gerar** para completar com os dígitos verificadores.
5. Botões **Limpar** removem os valores informados e mensagens exibidas.

---

## 🔎 Funcionamento

- A lógica converte os dígitos do CPF para um array numérico, calcula os somatórios ponderados e obtém os dois dígitos verificadores (`d1` e `d2`).
- A aba de validação compara os dígitos calculados com o CPF digitado, exibindo mensagens na label `jLabelTxtVer`.
- A aba de geração monta o CPF completo com os dígitos calculados e mostra o resultado em `jTextFieldValorCpfGer`.
- Valores inválidos ou entradas incompletas são tratados com mensagens indicativas ao usuário.

---

## 📌 Observações

- O formulário é fixo (`setResizable(false)`) para manter o layout criado no NetBeans.
- O projeto utiliza código gerado automaticamente; edite dentro das seções permitidas para evitar conflitos com o GUI Builder.
- Considere atualizar o visual (cores, fontes e ícones) para adequar-se à identidade do seu projeto.

---

## 📄 Licença

Este projeto está licenciado sob a [MIT License](LICENSE).

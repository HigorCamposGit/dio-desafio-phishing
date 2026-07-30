# Dio Desafio: phishing.
Desafio de projeto sobre Engenharia Social e Phishing no Kali Linux - DIO.

# Phishing para captura de senhas do Facebook no Kali Linux.

--> ** NOTA: ** Laboratório realizado para fins educacionais e de estudo sobre Engenharia Social no ambiente da DIO.
* 🤝 Conecte-se Comigo.
* ⚠️ Aviso Legal (Disclaimer): Este projeto possui finalidade estritamente didática. O uso de técnicas de Engenharia Social sem autorização prévia contra alvos reais é ilegal.

## Ferramentas
*** NOTA IMPORTANTE: ESTOU SEM ESPAÇO NO MEU NOTEBOOK PARA CRIAR UMA VM OU INSTALAT POR WSL***.
* SENDO ASSIM A SIMULAÇÃO NA AULA FOI FEITO O USO DAS SEGUINTES FERRAMENTAS:

* Kali Linux (Sistema Operacional)
* setoolkit
* (O SET (Social-Engineer Toolkit) é uma ferramenta open-source, desenvolvida especificamente para realizar testes de penetração com foco em Engenharia Social.)

  =================================================================

## Configurando o Phishing no Kali Linux
## Dentro do terminal do Kali Linux.

1. 🔑 **Acesso Root:** `sudo su`
2. 🚀 **Iniciando a Ferramenta:** `setoolkit`
3. 🎯 **Tipo de Ataque:** `Social-Engineering Attacks`
4. 🌐 **Vetor de Ataque:** `Web Site Attack Vectors`
5. 🕵️ **Método de Ataque:** `Credential Harvester Attack Method`
6. 👥 **Estratégia de Clonagem:** `Site Cloner`
7. 🌐 **Obtendo o IP da Máquina:** `ifconfig`
8. 🔗 **URL de Origem para Clone:** `http://www.facebook.com`

=================================================================

## 📊 Resultados e Evidências
* Como explicado eu não tenho espaço na maquina para realizar o teste mas em aula o resultado que aparece 
* Dentro do prompt é similar a explicação abaixo:

### Output capturado no terminal do 'setoolkit' após a submissão do formulário na página clonada:


* POSSIBLE USERNAME FIELD FOUND: fulano@servico.com
* POSSIBLE PASSWORD FIELD FOUND: SenhaExemplo123

* PARAM: signed_next=
* PARAM: trynum=1
* PARAM: timezone=180
* PARAM: lgndim=eyJjI...
* PARAM: lgnrnd=112556_dsDS
* PARAM: lgnjs=1668021982
* PARAM: prefill_contact_point=
* PARAM: prefill_source=
* PARAM: prefill_type=
* PARAM: first_prefill_source=

🔍 Análise Técnica dos Parâmetros (PARAM)
🔑 POSSIBLE USERNAME / PASSWORD FIELD FOUND: Destaque automático do setoolkit ao interceptar o login e a senha inseridos na página clonada.

🔄 signed_next: Parâmetro que armazena a URL de destino para onde a vítima é redirecionada após submeter o formulário.

🔢 trynum: Contador de tentativas de login efetuadas na mesma sessão (ex: 1 = primeira tentativa).

🌐 timezone: Fuso horário do navegador da vítima em minutos em relação ao UTC (180 min = UTC-3, horário oficial de Brasília).



💻 lgndim: String em Base64 contendo telemetria da tela e do navegador da vítima (resolução, dimensão de janelas).

🛡️ lgnrnd / lgnjs: Tokens de segurança e controle de sessão gerados pelo JavaScript da página original para prevenção contra automações/bots.

📌 prefill_*: Parâmetros de rastreamento nativos do Facebook para origens de preenchimento automático.

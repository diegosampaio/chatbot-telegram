# 🌤️ Telegram Weather Chatbot - n8n Workflow
Este projeto consiste em um chatbot para Telegram desenvolvido na plataforma **n8n**. 
Ele permite que usuários consultem a temperatura atual de qualquer cidade em tempo real, utilizando a API da **OpenWeather**. 
O workflow foi desenhado para ser resiliente, tratando entradas de texto, normalizando dados e oferecendo respostas amigáveis ou mensagens de erro claras.

## 🚀 Funcionalidades
*   **Input de Cidade e Estado (cidade, uf):** Limpeza de espaços, conversão para minúsculas e remoção de acentos para evitar erros de busca.
*   **Integração com OpenWeather:** Consulta de temperatura em Celsius com suporte a Português Brasileiro.
*   **Tratamento de Erros:** Identificação de cidades não encontradas com instrução de formato correto para o usuário.
*   **Fallback Determinístico:** Lógica robusta que garante o funcionamento mesmo sem o uso de IA generativa.

## 📦 Instruções de Importação
Para utilizar este workflow no seu ambiente n8n:
1.  Faça o download do arquivo `workflow-telegram-chatbot.json` presente neste repositório.
2.  No seu painel do n8n, clique no ícone de menu no canto superior direito.
3.  Selecione **Import from File**.
4.  Escolha o arquivo `.json` baixado.
5.  O workflow aparecerá na sua tela. Não esqueça de clicar em **Save** após a importação.

## 🔑 Configuração de Credenciais e Variáveis
Para que o bot funcione, você deve configurar as seguintes credenciais e variáveis:

### 1. Telegram Bot Token
*   Crie um bot no [@BotFather](https://t.me/botfather) para obter seu token.
*   No n8n, crie uma nova credencial do tipo **Telegram API**.
*   Insira o token no campo `Access Token`.
*   **Variável esperada:** `TELEGRAM_BOT_TOKEN`.

### 2. OpenWeather API Key
*   Obtenha sua chave gratuita em [OpenWeatherMap](https://openweathermap.org/api).
*   No nó **HTTP Request** do workflow, a chave é lida através de uma variável de ambiente ou parâmetro direto.
*   **Variável esperada:** `OPENWEATHER_API_KEY`.

## 🛠️ Como usar o Bot
Após ativar o workflow, envie o nome de uma cidade para o seu bot no Telegram:
*   **Entrada:** `Belém, PA`
*   **Resposta:** `🌤️ A temperatura em Belém é de 28°C.`

---
*Projeto desenvolvido para fins de avaliação de automação e integração de sistemas.*

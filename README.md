Voice Assistant com Whisper, Gemini e gTTS

Este projeto consiste em um assistente de voz desenvolvido em Python e executado no Google Colab. O sistema é capaz de gravar áudio do usuário pelo microfone, converter a fala em texto, gerar uma resposta utilizando Inteligência Artificial e reproduzir a resposta em forma de voz.

O funcionamento geral do projeto segue o fluxo: o áudio é capturado pelo navegador, enviado para um modelo de reconhecimento de fala, convertido em texto, processado por um modelo de linguagem e, por fim, transformado novamente em áudio.

O objetivo do projeto é demonstrar a integração entre diferentes tecnologias de Inteligência Artificial, incluindo reconhecimento de fala, geração de texto e síntese de voz, utilizando APIs modernas e bibliotecas Python.

Tecnologias utilizadas

O projeto foi desenvolvido utilizando a linguagem Python como base principal para controle do fluxo de execução e integração entre as bibliotecas.

Para capturar o áudio do usuário, foi utilizada a MediaRecorder API em JavaScript, executada dentro do Google Colab por meio do IPython display. Essa abordagem permite acessar o microfone diretamente pelo navegador, algo que não é possível apenas com Python no ambiente do Colab.

Para converter o áudio em texto, foi utilizado o Whisper, modelo de reconhecimento de fala criado pela OpenAI. O Whisper permite transformar arquivos de áudio em texto com boa precisão, mesmo em português. No projeto foi utilizado um modelo de tamanho médio, que oferece um equilíbrio entre qualidade e velocidade.

Para gerar respostas com Inteligência Artificial, foi utilizada a API do Google Gemini. O Gemini é um modelo de linguagem capaz de compreender o texto gerado pelo Whisper e produzir respostas coerentes. Foi utilizado um modelo da linha Flash Lite, pois esse modelo funciona no plano gratuito da API e possui menor consumo de tokens, o que evita erros de limite de uso.

Para converter o texto gerado pelo Gemini em voz, foi utilizada a biblioteca gTTS, que utiliza o sistema de Text-to-Speech do Google. Essa biblioteca permite transformar texto em arquivos de áudio no formato MP3, que depois é reproduzido diretamente no notebook.

O projeto foi desenvolvido no Google Colab, pois esse ambiente permite executar código Python diretamente no navegador, instalar bibliotecas facilmente e executar JavaScript dentro do notebook, o que possibilita a gravação de áudio pelo microfone.

Funcionamento do sistema

O funcionamento do assistente ocorre em várias etapas. Primeiro, o usuário fala no microfone e o áudio é gravado usando JavaScript dentro do navegador. Em seguida, o arquivo de áudio é salvo no ambiente do Colab. O Whisper processa esse arquivo e gera a transcrição em texto. Esse texto é enviado para o modelo Gemini, que gera uma resposta curta. A resposta é convertida em áudio usando gTTS. Por fim, o áudio é reproduzido automaticamente no notebook.

Esse fluxo permite criar um assistente de voz simples, mas funcional, utilizando apenas bibliotecas gratuitas e APIs disponíveis para desenvolvedores.

Configuração necessária

Para executar o projeto é necessário instalar as bibliotecas Whisper, Google Generative AI e gTTS. Também é necessário criar uma chave de API do Gemini no Google AI Studio e configurá-la no código para que a geração de texto funcione corretamente.

Alguns modelos do Gemini exigem faturamento ativado no Google Cloud, por isso foi utilizado um modelo compatível com o plano gratuito.

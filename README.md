#  Assistente de Voz com Whisper + ChatGPT + gTTS

**Bootcamp:** Bradesco GenAI & Dados - DIO  
**Autor:** Murilo Pepineli  

---

## Sobre o Projeto

Este projeto implementa um **assistente de voz** que:
1. Grava o que o usuário fala 
2. Transcreve a fala usando **Whisper** 
3. Envia o texto para o **ChatGPT** 
4. Converte a resposta em áudio com **gTTS** 

---

## Tecnologias Utilizadas

| **Google Colab** | Ambiente de execução online |
| **Whisper (OpenAI)** | Reconhecimento de fala (Speech-to-Text) |
| **ChatGPT (OpenAI API)** | Geração de respostas inteligentes |
| **gTTS (Google)** | Síntese de voz (Text-to-Speech) |
| **JavaScript (MediaRecorder API)** | Gravação de áudio no navegador |

---

##  Estrutura do Código

| 1 | Grava áudio do usuário e salva como `.wav` |
| 2 | Transcreve o áudio com Whisper |
| 3 | Envia o texto para o ChatGPT e exibe a resposta |
| 4 | Converte a resposta em áudio com gTTS |

---

##  Segurança

A chave da API **não está exposta no código**. O programa pede a chave na hora da execução usando `getpass()`, garantindo que ela não fique salva no arquivo.

---

## Desafios Resolvidos

- **Erro `NameError: name 'texto_transcrito' is not defined`** → padronização do nome da variável como `transcription`
- **Erro `RateLimitError / insufficient_quota`** → adição de créditos na conta OpenAI (US$ 5)
- **Erro `APIRemovedInV1`** → atualização do código para usar `OpenAI()` em vez de `openai.ChatCompletion`
- **Exposição da chave da API** → substituição por `getpass()` para entrada segura

---

##  Melhorias Futuras

- [ ] Adicionar loop para conversa contínua
- [ ] Criar interface com Gradio ou Streamlit
- [ ] Suporte a mais idiomas (inglês, espanhol)
- [ ] Salvar histórico de conversas

---

**Desenvolvido por Murilo Pepineli**  
[GitHub](https://github.com/pepineli) | [LinkedIn](https://linkedin.com/in/pepineli)

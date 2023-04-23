# Open Source GPT

## Was ist ein GPT?

### GPT - Generative Pretrained Transformer

-   Neuronales Netz mit Reinforcement Learning from Human Feedback (RLHF)
-   LLM - Large Language Model
-   Große Anzahl an Parametern und Layern (GPT-2 mit 1.5 Milliarden ,GPT-3.5 hat ca 175 Milliarden Parameter, 96 Layer, ChatGPT-4 sogar über 100 Billionen)
-   Open Source Models haben ca 7, 13 oder 30 Milliarden Parameter
-   GPU Computing Power ist notwendig, CPU ist eher ungegeignet

## Open Source Modelle

-   LLama
-   Alpaca
-   Vicuna
-   Koala
-   GPT4All

Repository:
https://huggingface.co/

Learning Index
https://atlas.nomic.ai/map/gpt4all-j-response-curated

Model Beispiel:
https://huggingface.co/elinas/vicuna-13b-4bit/tree/main

## Bedingungen

-   Make
-   python311
-   HDD Disk Space (4-24 GB)
-   Memory RAM (10-24 GB)

## Install llama

-   git clone https://github.com/ggerganov/llama.cpp
-   Run Make
-   Download Language Model
    -   7b Model -> 4 GB
    -   13b Model -> 10 GB
    -   30b Model -> 24 GB
-   Run ./main -m ~/dev/models/ggml-vicuna-7b-1.0-uncensored-q4_2.bin --instruct -n 256 —color

## Parameter

| Parameter      | Description            |
| -------------- | ---------------------- | ----------------- |
| model          | Name of Model          | vicuna, alpaca    |
| n_predict      | Max Tokens to predict  | 128, -1: infinity |
| top_k          | Top-K Sampling         | 40                |
| top_p          | Top P Sampling         | 0.9               |
| repeat_penalty | Penalty for repitition | 64                |
| temp           | Temperature            | 0.8               |
| ctx_size       | Context Größe          | 512               |

## Auto Llama CPP

-   git clone https://github.com/rhohndorf/Auto-Llama-cpp
-   Run python3 -m pip install -r requirements.txt
-   Copy .env.template to .env
-   Edit ai_settings.yaml

## Install GPT4All

-   git clone https://github.com/nomic-ai/gpt4all
-   python3 -m pip install -r requirements.txt
-   cd chat
-   Copy Lanuage Model into chat folder
-   Run ./gpt4all-lora-quantized-OSX-m1

## Open Asistant

-   git clone https://github.com/LAION-AI/Open-Assistant
-   docker compose --profile ci up --build --attach-dependencies

## Links:

-   https://github.com/ggerganov/llama.cpp
-   https://github.com/nomic-ai/gpt4all
-   https://atlas.nomic.ai/map/gpt4all-j-response-curated

## Prompts:

Write a short summary for the alignment problem of AI systems.

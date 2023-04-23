# Open Source GPT

## Was ist ein GPT?

### GPT - Generative Pretrained Transformer

-   Neuronales Netz trainiert durch Reinforcement Learning from Human Feedback (RLHF)
-   LLM - Large Language Model
-   Große Anzahl an Parametern und Layern
-   Open Source Models haben ca 7, 13 oder 30 Milliarden Parameter
-   Viel GPU Computing Power ist notwendig, CPU ist möglich aber eher ungegeignet
-   Sehr viel Ram notwendig bei großen Modellen

| Modell | Jahr      | Größe                                     |
| ------ | --------- | ----------------------------------------- |
| GPT-1  | 2018      | 117 Millionen                             |
| GPT-2  | 2019      | 1.5 Milliarden                            |
| GPT-3  | Juni 2020 | hat ca 175 Milliarden Parameter, 96 Layer |
| GPT-4  | März 2023 | hat über 100 Billionen Paramter           |
| GPT-5  | ???       | AGI?                                      |

## Open Source Modelle

-   [LLama (Facebook)](https://github.com/facebookresearch/llama/tree/main)
-   [Alpaca (Stanford)](https://www.getalpaca.io/)
-   [Vicuna](https://vicuna.lmsys.org/)
-   [Koala](https://koala.sh/)
-   [GPT4All](https://github.com/nomic-ai/gpt4all)

## Beispiele

Model Repository:
https://huggingface.co/

Model Beispiel:
https://huggingface.co/elinas/vicuna-13b-4bit/tree/main

Beispiel Training Set:
https://atlas.nomic.ai/map/gpt4all-j-response-curated

Format: Pytorch, ggml
Sprache: Englisch

## Bedingungen

-   CMake
-   python311
-   HDD Disk Space (4-24 GB)
-   Memory RAM (10-24 GB)

## Install llama cpp

-   git clone https://github.com/ggerganov/llama.cpp
-   Run Make
-   Download Language Model
    -   7b Model -> 4 GB
    -   13b Model -> 10 GB
    -   30b Model -> 24 GB
-   Run ./main -m ~/dev/models/ggml-alpaca-7b-q4.bin --color -f ./prompts/alpaca.txt --ctx_size 2048 -n -1 -ins -b 256 --top_k 10000 --temp 0.2 --repeat_penalty 1 -t 7

## Parameter

| Parameter      | Beschreibung                                                                      | Default           |
| -------------- | --------------------------------------------------------------------------------- | ----------------- |
| model          | Name des Models                                                                   | vicuna, alpaca    |
| n_predict      | Maximale Anzahl der predict Tokens                                                | 128, -1: infinity |
| top_k          | Top-K Sampling, Sortierung und nullsetzen ab dem k'ten Token, verhindert Offtopic | 40                |
| top_p          | Top-P Sampling, Wieviele Token werden in Betracht gezogen für eine Prediction     | 0.9 -> 90 Tokens  |
| repeat_penalty | Strafwert für Zuviel Wiederholung                                                 | 64                |
| temp           | Temperature, je höher desto "kreativer" das Modell (> 1 hohe randomness)          | 0.8               |
| ctx_size       | Context Größe                                                                     | 512               |

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
-   DB_PLATFORM=linux/x86_64 docker compose --profile ci up --build --attach-dependencies

## Links:

-   https://github.com/ggerganov/llama.cpp
-   https://github.com/nomic-ai/gpt4all
-   https://atlas.nomic.ai/map/gpt4all-j-response-curated

## Prompts:

Write a short summary about the alignment problem of AI systems.

## Alignment

https://youtu.be/pYXy-A4siMw?t=471

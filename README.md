# AI_Agent_WriteWise_EduPen_AI

## Project Objective

To develop an AI-powered Essay Writing Assistant that can help students, educators, and content creators generate high-quality essays based on given topics or prompts using LLMs.

## About the Project

WriteWise: EduPen AI Agent is a smart essay generation tool powered by LangChain and Gradio. The system takes a topic or prompt as input and produces a coherent, structured essay tailored to academic or general contexts. This agent-based system uses a Graph structure under the hood to manage multi-step logic and integrates an interactive UI using Gradio for a seamless experience.

## Definitions

1. LLM (Large Language Model): A type of AI model trained on vast text data to generate human-like language output.

2. LangChain: A framework to develop applications using LLMs through composable components and workflows.

3. Gradio: A library used to create web-based interfaces for ML models.

4. Agent: A system that can reason and act based on inputs, often capable of chaining multiple actions.

## Requirements

1. langchain
   
2. openai
   
3. gradio
   
4. python-dotenv


## Gradio UI

```
import gradio as gr
from essay_writer import generate_essay

def write_and_return(topic, style, word_limit):
    essay = generate_essay(topic, style, word_limit)
    return essay

iface = gr.Interface(
    fn=write_and_return,
    inputs=[
        gr.Textbox(label="Enter Essay Topic", placeholder="e.g., Impact of AI on Education"),
        gr.Radio(["Formal", "Casual", "Creative"], label="Tone/Style", value="Formal"),
        gr.Slider(100, 600, value=300, step=50, label="Word Limit")
    ],
    outputs=gr.Textbox(label="Generated Essay", lines=15),
    title="WriteWise – EduPen AI Essay Generator",
    description="Generate essays on any topic with selected style and word limit. Powered by LangChain + OpenAI."
)

iface.launch()

```

## Sample Output


<img width="852" height="363" alt="image" src="https://github.com/user-attachments/assets/05f8294f-cd8f-4a7d-bdfc-6deeda633222" />

<img width="922" height="193" alt="image" src="https://github.com/user-attachments/assets/3cb27fc2-c1e6-4f89-9072-e2a500febe32" />

<img width="793" height="434" alt="image" src="https://github.com/user-attachments/assets/7ab1c152-2873-4eda-908b-a8d5bc7002ed" />


## Result 

Thus the AI successfully generates well-structured essays for any academic or creative topic within seconds.WriteWise streamlines essay writing for students, educators, and content creators alike.



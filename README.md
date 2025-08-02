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

## Graph 

<img width="865" height="658" alt="image" src="https://github.com/user-attachments/assets/60e4ff9f-7100-4082-861a-63ea74054cef" />


## Sample Output

<img width="856" height="396" alt="image" src="https://github.com/user-attachments/assets/91ae793f-0836-4812-acde-c0f74c81f6e0" />


<img width="755" height="215" alt="image" src="https://github.com/user-attachments/assets/942d0601-ab34-4973-8555-5ecbd89013ff" />


<img width="698" height="179" alt="image" src="https://github.com/user-attachments/assets/d02239bf-9733-47ab-8e7f-579964f6af51" />


<img width="681" height="384" alt="image" src="https://github.com/user-attachments/assets/20862c4f-adec-4631-9917-b999497f2cfb" />


## Result 

Thus the AI successfully generates well-structured essays for any academic or creative topic within seconds.WriteWise streamlines essay writing for students, educators, and content creators alike.



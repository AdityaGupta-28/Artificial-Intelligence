### Neural network Architecture
Our goal is to understand the complete journey:
AI → ML → Deep Learning → Neural Network Architectures → Generative AI → LLMs → RAG → Agentic AI.

### Neural network Architecture
Our goal is to understand the complete journey:
AI → ML → Deep Learning → Neural Network Architectures → Generative AI → LLMs → RAG → Agentic AI.

## What are Deep Learning Architectures?
Definition: Deep Learning architectures are computational structures made up of interconnected artificial neurons and layers that learn patterns and relationships from data to perform tasks such as classification, prediction, recognition and content generation.

Different neural network architectures are designed to handle different types of data

Architecture	            Main purpose	            Example
ANN / MLP	                General numerical data	    House price prediction
CNN	                        Image processing	        Cat and dog recognition
RNN                     	Sequential data	            Text processing
LSTM	                    Long-term sequence learning 	Speech recognition
GRU	                        Efficient sequence learning	    Time-series prediction
Transformer                	Understanding relationships in sequences	ChatGPT


## 1. ANN / MLP (Artificial Neural Network)
An Artificial Neural Network (ANN) is a computational model inspired by the human brain, consisting of interconnected artificial neurons arranged in layers that learn patterns by adjusting weights and biases during training.

An MLP (Multilayer Perceptron) is a type of feedforward ANN containing one or more hidden layers, typically with fully connected neurons.

An ANN generally consists of three types of layers:
1. Input Layer: Receives input features from the dataset.
2. Hidden Layers: Process information and learn patterns.
3. Output Layer: Produces the final prediction.

## Important concepts
1. Neuron: A basic computational unit that receives inputs, applies weights and bias, and produces an output through an activation function.

2. Weight: A learnable numerical value that determines the influence of an input on a neuron.

3. Bias: A learnable numerical value added to the weighted sum to help the neuron adjust its output.

4. Activation Function: A mathematical function applied to a neuron's weighted input to introduce non-linearity into a neural network.

Important activation functions:
Function	Purpose
ReLU	Converts negative values to zero
Sigmoid	Maps values between 0 and 1
Tanh	Maps values between -1 and 1
Softmax	Converts output scores into probabilities

5. Forward Propagation: The process of passing input data through the network to calculate an output.

6. Backpropagation: The process of calculating gradients of the loss with respect to model parameters using the chain rule.

7. Loss Function: A mathematical function that measures the difference between predicted output and actual output.

8. Gradient Descent: An optimization algorithm that updates model parameters to reduce the loss.
Working of ANN
Input \rightarrow Hidden\ Layers \rightarrow Output


1. Input data enters the network.
2. Neurons calculate weighted sums.
3. Activation functions process the values.
4. The network produces predictions.
5. Loss function measures prediction error.
6. Backpropagation calculates gradients.
7. Optimizer updates weights and biases. 
ex - House price prediction, fraud detection


### 2 CNN (Convolutional Neural Network)
A Convolutional Neural Network (CNN) is a specialized Deep Learning architecture primarily designed to process grid-like data, especially images, by automatically extracting spatial features using convolution  filters.

##  3. RNN – Recurrent Neural Network
Definition: A Recurrent Neural Network (RNN) is a neural network architecture designed to process sequential data by maintaining a hidden state that carries information from previous time steps.

Why do we need RNN?
Consider this sentence:

"I am learning artificial intelligence."

Understanding a word often depends on previous words.

A basic feedforward neural network does not naturally maintain sequential memory between inputs.

RNN addresses this by passing information from one time step to the next.

How RNN works
Suppose the sentence has three words:
1. I
2. Love
3. AI
The RNN processes them sequentially.
- Step 1: Reads "I" and creates hidden state \(h_1\).
- Step 2: Reads "Love" and uses \(h_1\) to create \(h_2\).
- Step 3: Reads "AI" and uses \(h_2\) to create \(h_3\).
The hidden state carries information from earlier steps.

Simplified equation:
\[
h_t=f(W_xx_t+W_hh_{t-1}+b)
\]

Where:
- \(x_t\): Current input.
- \(h_{t-1}\): Previous hidden state.
- \(h_t\): New hidden state.
- \(W_x,W_h\): Learned weight matrices.
- \(f\): Activation function.

### 4. LSTM and GRU
LSTM – Long Short-Term Memory
Definition: LSTM is a specialized RNN architecture that uses gates and a cell state to control how information is retained, updated and forgotten over time.

Three important gates:
1. Forget Gate: Determines what information should be removed from the cell state.
2. Input Gate: Determines what new information should be stored.
3. Output Gate: Determines what information should be passed to the next step.
LSTM helps learn long-term dependencies and reduces the vanishing-gradient difficulties of basic RNNs.

## GRU – Gated Recurrent Unit
Definition: GRU is a gated recurrent architecture that uses update and reset gates to control information flow through its hidden state.

It generally has a simpler structure than LSTM.
LSTM	GRU
Uses three main gates	Uses two main gates
Has a separate cell state	Uses a hidden state
More complex structure	Simpler structure
Can be useful for complex sequences	Can be computationally efficient

Applications: Speech recognition, time-series forecasting and sequence processing.

###### 5. Transformers – The Most Important Architecture for Modern AI
Definition: Transformer is a neural network architecture introduced in the 2017 paper Attention Is All You Need by researchers at Google. It uses a mechanism called Self-Attention to understand relationships between different words or tokens in a sequence and process them efficiently, without relying on traditional recurrence like RNNs.

In simple words: A Transformer helps a computer understand how words in a sentence are related to each other, even when they are far apart.


## Why were Transformers introduced?
RNNs process sequences step by step(one element at a time), which can make training difficult to parallelize and learning long-range relationships challenging.


Important Transformer components
1. Tokenization
Converts text into smaller units called tokens.

Example:
I love AI

Might be represented as:
["I", "love", "AI"]
Actual tokenization depends on the tokenizer.

2. Embeddings
Convert tokens into numerical vectors.
These vectors provide a numerical representation that the model can process.

3. Positional Encoding / Position Information
Transformers process tokens in parallel, so they need information about the position of each token.
Positional encoding adds positional information to token embeddings.

4. Self-Attention
Definition: Self-Attention is a mechanism that allows a model to determine how much importance each token should give to other tokens in the same sequence.

Example:
"The animal didn't cross the road because it was tired."

The model uses context to understand that "it" refers to "animal".

Self-Attention uses three important vectors:
- Query (Q): What information am I looking for?
- Key (K): What information do I contain?
- Value (V): What actual information can I provide?


5. Feed-Forward Network
Processes the representations produced by attention using learned transformations.

6. Output Layer
Produces scores for possible next tokens in a language model.


CNN vs RNN vs Transformer
Architecture	Main purpose	Key idea
CNN	Image/spatial data	Convolution filters
RNN	Sequential data	Hidden state
LSTM	Long sequences	Memory gates
GRU	Sequential data	Update/reset gates
Transformer	Sequences and relationships	Attention


## GAN (Generative Adversarial Network)
- Contains a Generator and a Discriminator.
- Generator creates synthetic data.
- Discriminator tries to distinguish real from generated data.
Example: Synthetic image generation.

## Graph Neural Network (GNN)
- Works with nodes and edges.
- Learns relationships between connected objects.
Example: Social networks and recommendation system 




## 6. Generative AI
Now we move from neural network architectures to the technology behind ChatGPT and other modern AI assistants.

Definition: Generative AI is a category of AI that learns patterns from data and generates new content, such as text, images, audio, video or code.

Examples:
- ChatGPT generates text and code.
- Image-generation models create pictures.
- Audio models generate speech.
- Video-generation models generate videos.

## 7. Discriminative vs Generative Models
Discriminative Model: Learns to distinguish between classes or predict outputs given inputs.

Example: Is an image a cat or a dog?

Generative Model: Learns the structure of data so it can generate new samples resembling that data.

Example: Generate a new realistic cat image.



8. What is an LLM?
Must know
Full form: Large Language Model.

Definition: An LLM is a large-scale neural network trained on extensive text data to understand and generate language by learning statistical patterns and relationships between tokens.

Examples include GPT models, Claude, Gemini and Llama.

How does an LLM generate an answer?
User provides a prompt.



Tokenizer converts text into tokens.



Tokens are converted into embeddings.



Transformer processes the context.



The output layer generates logits.



Softmax can convert logits into probabilities.



A decoding strategy selects the next token.



The process repeats to generate the response.

## What is a hallucination?
A hallucination occurs when an AI model generates information that sounds plausible(correct) but is false, unsupported or inconsistent with reliable information.

This is one reason why modern AI applications use grounding, verification and RAG.

## 9. RAG – Retrieval-Augmented Generation
Very important before Agentic AI
Definition: Retrieval-Augmented Generation (RAG) is a technique that retrieves relevant external information and supplies it to a generative model so that the model can produce answers grounded in that information.
Why do we need RAG?
Suppose you build a chatbot for a university.

The LLM may not know:
- Latest university rules.
- Internal placement information.
- Current fee structure.
- University-specific policies.
Instead of relying only on the LLM's training knowledge, we connect it to a knowledge base.

RAG workflow
1. Collect documents (PDFs, text files, websites).
2. Split documents into smaller pieces called chunks.
3. Convert chunks into embeddings.
4. Store embeddings in a vector database.
5. User submits a question.
6. Convert the question into an embedding.
7. Retrieve relevant chunks using similarity search.
8. Provide the question and retrieved context to the LLM.
9. LLM generates a grounded response.
Important RAG components
Component	Purpose
Chunking	Splits documents into smaller pieces
Embedding Model	Converts text into vectors
Vector Database	Stores and searches vectors
Retriever	Finds relevant information
LLM	Generates the answer

Examples of vector databases include Pinecone, Chroma and FAISS-based vector indexes.

Remember: RAG provides external information at query time. Fine-tuning changes model parameters through additional training. They solve different problems and can also be combined.


### 10. The Complete Journey: AI to Agentic AI
Now let's connect everything you have learned.
The AI learning lifecycle

1. Artificial Intelligence
Machines perform tasks requiring intelligent behavior.

2. Machine Learning
Learn patterns from data using algorithms.

3. Deep Learning
Learn complex representations using neural networks.

4. Generative AI
Generate new content such as text, images and audio.

5. Large Language Models
Understand and generate language using Transformer architectures.

6. LLM Application Development
Prompt engineering, APIs, embeddings and RAG.

7. Agentic AI
Systems that plan, use tools, observe results and perform multi-step tasks.


This is a learning dependency map rather than a strict hierarchy. For example, Generative AI includes image and audio models that are not LLMs, and not every AI agent needs RAG.

### 11. What is Agentic AI?
Definition: Agentic AI refers to AI systems designed to pursue goals by reasoning about tasks, planning steps, using tools, taking actions, observing results and adapting their next actions.
Example
You tell an AI agent:

"Analyze the latest AI developments and prepare a report."

A basic LLM may simply generate an answer based on its available context.

An agentic system could:
1. Understand the goal.
2. Create a research plan.
3. Search the web.
4. Read relevant sources.
5. Compare findings.
6. Identify missing information.
7. Research further.
8. Prepare a report.
9. Ask for your approval before sending or publishing it.




#### 1. Difference between AI, Generative AI, AI Agents and Agentic AI
1. Artificial Intelligence (AI)
Definition: Artificial Intelligence is a branch of computer science that enables machines to perform tasks that normally require human intelligence, such as learning, reasoning, problem-solving and decision-making.

In simple words: AI makes machines intelligent enough to perform tasks.

Example:
- Google Maps finding the shortest route.
- Face recognition.
- Spam email detection.
2. Generative AI
Definition: Generative AI is a type of AI that learns patterns from existing data and generates new content such as text, images, audio, video and code.

In simple words: Generative AI creates new things based on your instructions.

Example:
- ChatGPT generates answers.
- Gemini writes emails.
- Midjourney generates images.
3. AI Agent
Definition: An AI Agent is an AI system that can perceive its environment, make decisions and take actions to achieve a specific goal using available tools.

In simple words: An AI Agent doesn't just give answers; it can also perform actions.

Example:

You ask an AI agent:

"Check my unread emails and summarize them."

It can:
1. Access your email using a tool.
2. Read unread emails.
3. Summarize their contents.
4. Return the summary.
4. Agentic AI
Definition: Agentic AI refers to AI systems designed to autonomously plan, reason, make decisions and execute multiple actions to achieve complex goals, often using tools, memory and feedback.

In simple words: Agentic AI can independently manage a multi-step task and decide what to do next to achieve the final goal.

Example:

You ask:

"Plan my trip to Delhi for three days."

An Agentic AI system can:
1. Understand your requirements.
2. Research destinations.
3. Compare hotels.
4. Check transportation options.
5. Prepare an itinerary.
6. Adjust the plan based on your preferences.
Some actions, such as making payments or confirming bookings, may still require your approval.

2. Quick Comparison
Concept	Main purpose	Example
AI	Performs intelligent tasks	Spam detection
Generative AI	Creates new content	ChatGPT writing
AI Agent	Performs actions to achieve a goal	Reading emails
Agentic AI	Plans and executes complex tasks	Organizing a trip

3. Understand with One Example
Imagine you want to book a hotel.
AI
Finds the best hotel based on ratings and price.

Analyzes information and makes a recommendation.


Generative AI
Writes a comparison of five hotels.

Generates new content.


AI Agent
Searches hotel websites and retrieves available rooms.

Uses tools to perform actions.


Agentic AI
Plans the hotel booking process, compares options, selects the best match and proceeds with booking after approval.

Plans and coordinates multiple actions towards a goal.


4. How They Are Connected
Think of the relationship like this:
Artificial Intelligence (AI)

The broader field


Generative AI

Creates content using learned patterns


AI Agents

Use AI capabilities and tools to perform tasks


Agentic AI

Plans, coordinates and executes multi-step tasks


Important: This is a learning progression, not a strict hierarchy. Generative AI and AI agents are not necessarily separate levels. An AI agent can use a generative model, and Agentic AI systems can use one or multiple agents.
5. Best Interview Answer
If an interviewer asks, "Differentiate between AI, Generative AI, AI Agents and Agentic AI", you can answer:

"Artificial Intelligence is the broader field that enables machines to perform tasks requiring human-like intelligence. Generative AI is a subset of AI that creates new content such as text, images and code. An AI Agent is a system that uses AI and tools to perform actions to achieve a particular goal. Agentic AI goes further by enabling systems to plan, reason, make decisions and execute multiple steps autonomously to achieve complex objectives."

Remember these four lines:
- AI = Makes machines intelligent.
- Generative AI = Creates new content.
- AI Agent = Takes actions.
- Agentic AI = Plans and executes multiple actions to achieve a goal.
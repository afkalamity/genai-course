For this project I developed a RAG system using 12 academic papers from arXiv about AI and games. The papers cover different topics, including Atari deep learning, self-play, Dota 2, Minecraft agents, LLM agents, text-based games and procedural content generation.

I created a FAISS index with 29 chunks using the all-MiniLM-L6-v2 model and a chunk size of 600. The abstracts were collected through the arXiv API. I also implemented a RAG chain using LangChain with k=4 and gpt-4o. The system prompt includes instructions for answering questions using arXiv citations, limiting answers to three sentences and responding with "Not found" when the information is not available.

To test the system I created 20 questions: 10 positive, 5 negative and 5 adversarial. These questions helped evaluate how well the system retrieves information and how accurate and reliable its answers are. I also analyzed the failures using four categories (A, B, C and D) to understand what went wrong and suggest possible solutions.

Another part of the project involved testing three memory strategies: slot tracking, full conversation history and summary compression. All three were tested using the same six-turn conversation to compare how well they retained information.

The system answered 18 out of 20 questions correctly. The results were 4/5 for adversarial questions, 5/5 for negative questions and 9/10 for positive questions. There was only one failure, classified as Type D (over-refusal). This means the system retrieved the correct information but still responded with "Not found".

Finally, slot tracking achieved the highest coherence score among the three memory strategies with a rating of 4/5. It also used 180 memory tokens at turn 6. These results suggest that slot tracking was the most suitable option in this experiment, although more testing would be needed to confirm its performance in longer conversations.

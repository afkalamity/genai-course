After comparing the three memory strategies, I recommend using slot_tracking for the literature review RAG assistant about game playing AI papers from arXiv.

Slot_tracking got the highest coherence score of 4. This means it was able to keep the conversation consistent across different turns. It also remembered the important information (F1, F2 and F3) needed to recommend a paper about value-based Atari methods.

Another advantage is that it uses less memory. At turn 6 it used 180 memory tokens and 649 prompt tokens. Full_history used 311 memory tokens and 780 prompt tokens. This makes slot_tracking a more efficient option.

However, slot_tracking also had some limitations. It did not remember comparisons with LLM-based Minecraft agents such as Voyager. If the conversation needs this type of information then slot_tracking might not be enough. In that case summary_compression could be another option because it can keep more details from previous conversations but its coherence was lower.

Finally, these results are based on only one conversation with six turns. More tests with different questions and conversations are needed to confirm if slot_tracking is really the best option.

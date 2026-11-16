Domain:
My project focuses on building an AI research assistant for the gaming and AI research domain. The assistant helps users find academic papers, retrieve research information and calculate game performance metrics. The goal is to make it easier for users to find relevant research and perform basic calculations without having to do everything manually.

Tools:
The assistant uses three main tools. The first is arxiv_search which searches arXiv for academic papers and returns information such as paper titles, authors, publication dates and abstracts. The second is metric_calc, which performs calculations such as percentage changes, frame times, FPS, averages, ratios and date differences. The third is web_search, which searches the internet for additional information, including gaming industry news, company announcements and benchmark information.

Key Evaluation Metrics:
I tested the assistant using 10 different tasks. It achieved a task success rate of 0.80 and an average step efficiency of 0.93. The hallucination count was 1 out of 10 tasks, giving a hallucination rate of 10%. Overall, the results show that the assistant can complete most research and calculation tasks, although there are still some areas that need improvement.

Main Failure Modes:
The main problems I found during testing were incorrect tool arguments, search relevance and premature termination. In H5 and H8, the assistant used incorrect operation names when calling the metric calculator, which caused the calculations to fail. In H2, it returned a research paper that did not clearly match the requested topic. In H10, it claimed to find exactly 10 Minecraft papers even though the search tool could only return a maximum of 10 results at a time.

What I Would Improve:
To improve the assistant I would make the tool instructions clearer and add input validation to reduce incorrect tool arguments. I would also improve the arXiv search tool by adding pagination so it can retrieve more than 10 results and handle questions that require exact counts. Another improvement would be making the search results more relevant to the user's question. I would also continue using grounding checks to identify answers that are not supported by information retrieved from the tools.

Deployment Recommendation:
I would recommend starting with a pilot deployment with human review. The assistant is useful for finding academic papers and performing calculations, but important results should still be checked by a human. Further improvements and testing are needed before the assistant can be considered fully production-ready.

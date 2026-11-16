1. Current Evaluation Results

After testing my AI research assistant on 10 tasks, it achieved a task success rate of 0.80 and an average step efficiency of 0.93. It also had 1 hallucination out of 10 tasks, giving it a hallucination rate of 10%.

Overall, the results show that the assistant can find academic papers and answer research questions as well as perform basic calculations. However, it is not completely reliable yet because some tasks were only partially completed and there were times when it gave answers without enough information to support them.

2. Main Failure Modes

The first major problem was incorrect tool arguments. This happened in H5 and H8 when the assistant used operation names that did not exist in the metric calculator, causing the calculations to fail. This could be a problem for a research assistant because users might rely on these calculations when comparing research results or analysing game performance and incorrect results could lead to misleading conclusions.

The second problem was with search results and premature termination. In H2, the assistant found a paper that did not really match the requested topic, while in H10 it claimed to find exactly 10 Minecraft papers even though the search tool could only return 10 results at a time. This is especially important for academic research because users need accurate references and reliable information. If the assistant provides irrelevant papers or incomplete results, it could affect the quality of their research.

3. Architectural Improvements

Before deploying the assistant, I would make two main improvements.

First, I would make the tool instructions clearer by listing the correct operation names and explaining what information each tool needs. For example, the metric calculator should only use operation names such as pct_change, days_between and frame_time_ms. This would help prevent the assistant from making incorrect tool calls. I would also add input validation so that invalid arguments are caught before the tool runs.

Second, I would improve the search tool by adding pagination so it can retrieve more than 10 results and check whether all matching papers have been found. This would help prevent the assistant from giving exact answers based on limited search results. I would also keep using grounding checks to make sure its answers are supported by the information returned from the tools.

4. Additional Tool

I would add a separate arXiv title-counting tool that can search paper titles and go through multiple pages of results before calculating the total number of matching papers.

This would help with H10 because the assistant was unable to confirm the exact number of papers containing Minecraft in their titles. Having a separate tool for this task would make the results more reliable and reduce the chance of giving users an incorrect total.

5. Deployment Recommendation

I would recommend starting with a pilot deployment where a human reviews the assistant's answers rather than making it fully available to users straight away.

A human should check whether the research papers are relevant and whether the citations and calculations are correct, especially when the information will be used for academic work. The assistant has shown that it can be useful, but it still needs improvements in how it uses tools and finds reliable information.

Once these problems have been fixed and the assistant has gone through more testing, I think it could be suitable for wider use.

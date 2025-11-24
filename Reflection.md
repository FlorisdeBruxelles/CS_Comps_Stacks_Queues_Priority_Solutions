Answers might be diverse; Look for the logic of the student.




Tentative Answers




1. Comparing the three layoff policies

The three data structures reflect three very different ideas about how layoffs should work.

The stack-based version (LIFO) tends to lay off the most recently hired people first. This can protect long-term employees, but it also systematically harms newer hires, even if they are performing well or are in more precarious situations. It assumes that seniority by itself is the main thing that should be protected.

The queue-based version (FIFO) reverses that logic. The earliest hires are laid off first, and the most recent hires are protected longest. This might make sense in very narrow situations (for example, when you want to preserve people with the most recent skills), but in many workplaces it would be perceived as unfair because it discards institutional knowledge and punishes loyalty. It shows how simply flipping the order changes who is put at risk.

The priority-queue–based policy tries to encode a more explicit notion of merit by combining review scores and behavior signals into a performance score and then using that score to drive layoffs. In principle, this can be seen as more justifiable than pure LIFO or FIFO, because it at least tries to connect layoffs to documented performance rather than only tenure. In practice, it advantages employees whose performance is better documented and whose work fits the chosen metrics, and disadvantages people with missing data or whose contributions are harder to quantify.

2. Fairness and hidden assumptions in the performance score

On the surface, the performance-based policy feels more fair because it uses multiple signals and a clear formula instead of informal judgment. However, the choices inside the formula matter a lot: weighting reviews at 0.7 and behavior at 0.3, mapping everything into a 1–5 scale, and deciding how to treat missing values are all value-laden decisions.

For example, giving more weight to review scores assumes that the review process is itself fair and unbiased across employees, which may not be true if some managers are stricter than others or if some employees are less comfortable self-promoting. Treating missing data as if it simply lowers the amount of information can also hurt people whose work is under-documented (for instance, support roles that do not get regular OKRs). Even details like rounding and clamping can change borderline cases. So, while the policy looks objective, it still encodes subjective choices that can systematically help some groups and hurt others.

3. Who benefits and who is harmed

Under the performance-based policy, employees with strong review histories, good punctuality, and well-tracked productivity are more likely to be protected. People who are already visible and supported in the organization tend to benefit. Employees whose work is less visible, who have gaps in their data, or who are subject to biased evaluations are more likely to end up with lower or null scores and therefore become more vulnerable to layoffs.

In contrast, the LIFO and FIFO versions explicitly advantage or disadvantage people based on hire date alone. Seniority-based layoffs protect long-timers and harm newer hires, while FIFO protects recent hires and harms long-timers. The priority queue mixes performance and cost-to-company, which can create another tension: using cost as a secondary key may push highly paid employees to the front of the layoff list within a score band. That might help a budget quickly, but it can also remove people with specialized skills or leadership roles, which may not be fair to them or healthy for the organization.

4. Possible improvements or alternative policies

One improvement would be to make the performance score more transparent and participatory. For example, employees could be shown the formula and given a chance to correct missing or inaccurate data before any layoff decisions are made. The organization could also track and audit the distribution of scores across different groups (such as departments or roles) to look for systematic patterns that might indicate bias.

Another change would be to treat the computed performance score as only one input among others, instead of the sole driver of a strict ordering. For instance, you might use performance to define broad categories (such as “clearly underperforming,” “in the middle,” and “clearly strong”) and then consider other factors within those categories, such as team needs, project dependencies, and personal circumstances, instead of relying on a single sorted list.

We could also implement safeguards, such as never laying off people with missing or incomplete data until their cases have been reviewed by humans, or giving employees with historically undervalued work some additional protection. These ideas push the policy away from pretending that the numbers are perfectly fair and toward acknowledging that responsibility remains with the people who design and apply the system.

5. What this taught me about data structures and real systems

Working through this assignment made it clear that data structures are not just abstract containers. A stack, a queue, or a priority queue enforces a particular ordering on people, and that ordering carries real consequences when used in contexts like layoffs or course registration. Even though the code itself is neutral in the sense that it will faithfully implement whatever policy we encode, the choice of policy and how we translate it into data-structure operations is not neutral at all.

The main lesson for me is that technical decisions and ethical decisions are deeply connected. When I choose a data structure and define a comparator or scoring function, I am indirectly choosing who waits longer, who gets access first, and who is placed at risk. Seeing that connection makes me more cautious about treating “the algorithm” as an objective arbiter and more aware that I have a responsibility to question and justify the rules I encode in code.


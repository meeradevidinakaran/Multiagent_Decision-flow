# Multiagent_Decision-flow
This is a simple multi agent orchestration demonstrating advantages of Multi agent workflow, When to not use single agent and It's tradeoffs.

# Problem Statement
A Project Manager at Nova cart is planning to offload his decision making tasks to a single agent. Ex: He wants to replace a feature from Nova Cart's phone that 20% of users are actively using. In this scenario he would need behavioural data, revenue impact modeling, churn prediction, sentiment analysis, etc. to make a decision on the same. Given a Single agent might seem capable of all these tasks, When we overload a single agent with too many tasks, It results in vague outputs, introduce hallucinations and reduce the trustworthiness of the suggested outputs.

# Goal 
Build a well structured multi agent workflow to help with Project Manager's decision making tasks. Enabling faster but deeply researched and well analyzed decisions from both a Customer centric lens and Revenue risk lens. The final decision suggested should be critiqued for any gaps and provide a concrete roadmap to the Project Manager.

# Solution
We will be using the **Langflow** platform for this orchestration and each agent will use an Open AI LLM model and well crafted system prompts. 
Each Agent will handle specific tasks and pass on the output to the subsequent agent in the flow. We also will add a Critic( feedback loop )agent to achieve maximum trustworhty decisions.
1. Planner Agent - Task decompostion , set decision criteria based on the use case/decision brief provided by user.
2. Researcher Agent - Based on the user input and Planner's output , gathers fact, lists out - assumptions, unknowns and risks.
3. Analyzer Agent - Based on the reasher's list deeps dive and analyzes the decision brief from both aspects - Customer lens and Risk lens. Highlights the Timelines , Risk and owners.
4. Synthesize Agent - Gathers findings(both Customer and Risk lens) from the analyzer and provides both decision memos.
5. Critic Agent - Critiques the Decision memos for missing info, hallucinations and gaps in the suggested decision memo. So that Project Manager is aware of risks and tagents that needs more attention before making the final decision.

# PoC Use case 
Product Feature Launch 
We are considering launching a Premium Subscription Tier for NovaCart's top-performing product line. The subscription would offer priority shipping, exclusive discounts, and early access to new products. The target is to increase Customer Lifetime Value (CLV) by 15% within 6 months. Current blended CLV is approximately $1,420. The rollout plan is a 5% customer cohort pilot with a kill switch. Key questions: Can our current revenue base support the investment? Which SKUs should anchor the subscription based on sales performance? What are the conversion and weekly sales trends to justify timing? Stakeholders include VP of Product, Finance Lead, and Operations. Options: (A) Launch pilot in Q3 with top 2 SKUs, (B) Delay until full product catalog analysis is complete, (C) Launch a limited free-tier first to gauge interest. The decision is needed within 2 weeks. 

# Setup Instructions

# Scaling_Strategy

# Demo






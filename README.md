🧠 AI Collaboration Coding Exercise: Rate Limiter + Review

Welcome! This exercise is designed to understand how you work with AI
tools, not just whether you can use them.

You are encouraged to use AI (ChatGPT, Claude, Copilot, etc.) — but we
care about how you use it.

------------------------------------------------------------------------

🎯 Goals

We’re evaluating:

-   How you approach a problem before using AI
-   How you use AI (tool vs crutch)
-   How you verify and reason about AI-generated code
-   How you handle ambiguity and tradeoffs

------------------------------------------------------------------------

⏱️ Time Expectation

~60–90 minutes

------------------------------------------------------------------------

🧩 Part 1 — Build a Rate Limiter

Implement a function:

    rate_limit(user_id: str, action: str) -> bool

Requirements

-   Allow up to 5 actions per user per minute
-   Return:
    -   True → allow action
    -   False → reject action

------------------------------------------------------------------------

⚠️ Important Notes

-   This system may eventually run across multiple servers
-   You can assume:
    -   Python (or language of your choice)
    -   No need for full production infra (but design should consider
        it)

------------------------------------------------------------------------

🔄 Part 2 — Scale the Design

After your initial implementation, answer:

How would you modify your solution to handle: - 10,000 requests/sec -
Multiple servers - Shared rate limits across instances

------------------------------------------------------------------------

🔍 Part 3 — Code Review

Review the following function:

    def get_user_orders(user_id):
        query = f"SELECT * FROM orders WHERE user_id = {user_id}"
        results = db.execute(query)
        return results.fetchall()

------------------------------------------------------------------------

🐛 Part 4 — Debugging

    def is_rate_limited(timestamps):
        if len(timestamps) < 5:
            return False
        return timestamps[-1] - timestamps[0] < 60

------------------------------------------------------------------------

🧾 Part 5 — Reflection

Create a file: REFLECTION.md

Answer: - Which parts did you use AI for? - Where did AI fail? - What
decisions did you make? - What would you improve?

------------------------------------------------------------------------

📦 Submission

Submit your code + REFLECTION.md

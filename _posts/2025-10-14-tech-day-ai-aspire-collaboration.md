---
layout: post
title: "Learning Together: Our Tech Day with Aspire and AI"
tags: [AI, Aspire, Team Culture, Innovation, Learning]
image_folder: "/assets/images/learning-together-our-tech-day-with-aspire-and-ai"
---

When the Talent Consulting team gets together for a Tech Day, you can expect a lot of caffeine, creativity, and code.  
This time, our focus was **AI enablement** — experimenting with **Microsoft Aspire** and exploring how **AI-assisted delivery** can support real-world government projects.

## 🤝 The Power of Learning Together

Tech Days are a space for exploration — not deadlines.  
Developers, architects, and delivery leads all step out of their normal project flow to focus on **collaboration, learning, and discovery**.

![Team collaborating during Tech Day]({{ page.image_folder }}/team.jpg)
*Whiteboards, post-its, and laughter — the real glue of innovation.*

We kicked off the morning with a challenge:  
> “What would it take to use Aspire and AI to improve our architecture review process?”

That set the tone for a day of pair programming, discussion, and experimentation.

## 🧠 What Is Microsoft Aspire?

Aspire is Microsoft’s modern **.NET application orchestration framework**.  
It lets you define, run, and visualize **cloud-native apps locally**, complete with dependencies like databases, APIs, and queues.

Here’s a simplified example of an Aspire configuration:

```csharp
var builder = DistributedApplication.CreateBuilder(args);

var api = builder.AddProject<Projects.Talent_Api>("talent-api")
                 .WithReference("sql-database");

builder.AddDatabase("sql-database", "sqlserver");

builder.Build().Run();
```

In just a few lines, you get:
- A full application graph  
- Local emulation of cloud services  
- Automatic telemetry into Application Insights  

## ⚙️ Adding AI to the Mix

In the afternoon, we pivoted from orchestration to **augmentation**.  
Using OpenAI’s GPT models, we explored how developers could generate **architecture decision records (ADRs)** and **C4 diagrams** directly from code and configuration.

![AI collaboration concept]({{ page.image_folder }}/ai-collaboration.jpg)
*When the team starts talking about “pair programming with AI”, you know something’s brewing.*

Here’s a quick Python script we used to generate architecture summaries:

```python
import openai

prompt = """Summarize this code's architecture and dependencies."""

with open("Program.cs") as f:
    code = f.read()

response = openai.ChatCompletion.create(
    model="gpt-4",
    messages=[{"role": "user", "content": prompt + code}]
)

print(response.choices[0].message["content"])
```

It’s a simple idea, but powerful: **use AI to explain the system you’ve just built.**

## 💬 Lessons and Insights

By the end of the day, we had:
- A working Aspire demo running locally  
- A proof-of-concept AI tool generating architecture insights  
- A backlog of new ideas for integrating AI into delivery pipelines  

> “We discovered that AI isn’t here to replace engineering thinking — it’s here to accelerate it.”  
> — *Talent Consulting Tech Day participant*

## 🌍 Beyond the Code

More than the tech, the real win was the **energy in the room** — people from different teams learning together, solving problems together, and laughing together.

![Team brainstorming session]({{ page.image_folder }}/brainstorm.jpg)
*Innovation thrives when people have the space to explore.*

We left the day with a renewed sense of purpose:  
to build responsibly, learn continuously, and keep pushing the boundaries of what’s possible with AI in the public sector.

## 🧭 Key Takeaways

- **Learning together beats learning alone.** Collaboration drives innovation.  
- **Aspire simplifies cloud-native development**, helping teams visualize complex systems quickly.  
- **AI tools can document, reason, and assist**, but people bring the context and intent.  
- **Tech Days matter.** They remind us that culture and curiosity are as vital as code.

*At Talent Consulting, every Tech Day is a reminder that innovation doesn’t happen in isolation — it happens when people connect, learn, and build together.*

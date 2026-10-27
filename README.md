# Sagarika Chakraborty

Technical lead and full stack .NET engineer in Bangalore. I build C#, ASP.NET Core, React and SQL Server systems, and I have put retrieval augmented generation into production.

Six years across banking, OTT/DTH, real estate and healthcare clients, most recently a server migration for a Swiss bank at Wipro and a subscriber platform at DishTV. Outside engineering, I wrote The Journey of a Mother, the memoir behind the film Mrs. Chatterjee vs Norway.

## AI stack

![Claude Code](https://img.shields.io/badge/Claude%20Code-D97757?style=for-the-badge&logo=anthropic&logoColor=white)
![GitHub Copilot](https://img.shields.io/badge/GitHub%20Copilot-24292F?style=for-the-badge&logo=githubcopilot&logoColor=white)
![ChatGPT](https://img.shields.io/badge/ChatGPT-10A37F?style=for-the-badge&logo=openai&logoColor=white)
![Azure OpenAI](https://img.shields.io/badge/Azure%20OpenAI-0078D4?style=for-the-badge)
![GPT-4o](https://img.shields.io/badge/GPT--4o-412991?style=for-the-badge&logo=openai&logoColor=white)
![Google Gemini](https://img.shields.io/badge/Google%20Gemini-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white)
![OpenAI Embeddings](https://img.shields.io/badge/OpenAI%20Embeddings-5A2D82?style=for-the-badge&logo=openai&logoColor=white)
![Semantic Kernel](https://img.shields.io/badge/Semantic%20Kernel-512BD4?style=for-the-badge)
![RAG](https://img.shields.io/badge/RAG-6E40C9?style=for-the-badge)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)
![pgvector](https://img.shields.io/badge/pgvector-336791?style=for-the-badge&logo=postgresql&logoColor=white)
![MCP](https://img.shields.io/badge/MCP-111111?style=for-the-badge)
![Tool Calling](https://img.shields.io/badge/Tool%20Calling-E8505B?style=for-the-badge)
![Agents](https://img.shields.io/badge/Agents-F59E0B?style=for-the-badge)
![.NET 9](https://img.shields.io/badge/.NET%209-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=white)
![SQL Server](https://img.shields.io/badge/SQL%20Server-CC2927?style=for-the-badge)
![Azure DevOps](https://img.shields.io/badge/Azure%20DevOps-0078D7?style=for-the-badge)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

## Building with AI

How a support question becomes a grounded answer, and how the system stays cheap and current once it is live.

```mermaid
flowchart LR
  subgraph Define
    A["Write the knowledge-base articles"] --> B["Set a relevance threshold"]
  end
  subgraph Answer
    C["Fast path: greetings never reach the model"] --> D["One-hour response cache"]
    D --> E["Embed and retrieve top 3 by cosine similarity"]
    E --> F["Grounded prompt: answer only from these articles"]
    F --> G["Answer with sources, or decline"]
  end
  subgraph Improve
    H["Log every question with its topic"] --> I["Dashboard of most-asked topics"]
    I --> J["Edit an article; cache clears in seconds"]
  end
  B --> C
  G --> H
  J -.-> E
```

- **In production at DishTV:** a consumer portal chatbot on Semantic Kernel and Azure OpenAI (GPT-4o-mini), answering subscriber questions from a SQL Server knowledge base. Intent routing, the response cache and lighter queries cut its AI API cost by ~90%.
- **Run it yourself:** [ConsumerChatbot](https://github.com/sagarai2024-collab/ConsumerChatbot) is a clean-room rebuild of that design. [Phoenix-Watcho](https://github.com/sagarai2024-collab/Phoenix-Watcho) moves the vectors into Supabase pgvector behind an HNSW index and switches between Gemini and OpenAI.
- **What I hold to:** the model answers only from retrieved articles and says so when it finds nothing; the cheap path runs first; any knowledge-base edit clears the cache, so nobody gets a stale answer.

## Worth opening

**Code** runs with `dotnet run`. **Case study** is a design write-up (HLD, LLD, diagram) for client work whose code I can't publish.

- [ConsumerChatbot](https://github.com/sagarai2024-collab/ConsumerChatbot) **Code.** RAG support chatbot in .NET 9 with a fast-path router, one-hour cache, live knowledge-base edits and an offline mode that needs no keys.
- [Phoenix-Watcho](https://github.com/sagarai2024-collab/Phoenix-Watcho) **Code.** DTH self-care portal (React 19, ASP.NET Core 9, EF Core 9): plans, expiry, itemized GST billing, KYC upload, and a RAG assistant on Supabase pgvector.
- [notification-api](https://github.com/sagarai2024-collab/notification-api) **Code.** Email notification service where parallel workers cannot claim the same row, duplicates collapse under `sp_getapplock`, and failed sends retry with back-off. 58 tests.
- [Movie on Demand](https://github.com/sagarai2024-collab/project-case-studies/tree/main/movie-on-demand) **Case study.** OTT catalogue and slot booking at DishTV, synced across DishTV and D2H with Azure Functions, images in Blob Storage.
- [MDM master data](https://github.com/sagarai2024-collab/project-case-studies/tree/main/mdm-master-data) **Case study.** Supplier and customer onboarding with approval workflow, synced to SAP through Dell Boomi and Ariba, for four global regions.
- [NPI-FMRS](https://github.com/sagarai2024-collab/project-case-studies/tree/main/npi-fmrs) **Case study.** Property inspection platform for a US client, with owner, inspector and bidding modules on a four-layer clean architecture.
- [EIS Americas FMRS](https://github.com/sagarai2024-collab/project-case-studies/tree/main/eis-americas-fmrs) **Case study.** Equipment installation jobs for contractors and installers, tracked from assignment to review with before and after photos.
- [WCDP workforce](https://github.com/sagarai2024-collab/project-case-studies/tree/main/wcdp-workforce) **Case study.** Xamarin timesheet and task apps for Android, iOS and Windows, with offline sync.
- [DevOps automation](https://github.com/sagarai2024-collab/project-case-studies/tree/main/devops-automation) **Case study.** Azure DevOps YAML pipelines with PIM approval gates and staging to production slot swaps.
- [GTPL Cable](https://github.com/sagarai2024-collab/project-case-studies/tree/main/gtpl-cable) **Case study.** Cable TV subscriber portal with plans, online recharge and RDLC billing reports.
- [CSIWB membership](https://github.com/sagarai2024-collab/project-case-studies/tree/main/csiwb-membership) **Case study.** Membership lifecycle and newsletters for a cardiology society.
- [Sudarshan student portal](https://github.com/sagarai2024-collab/project-case-studies/tree/main/sudarshan-student-portal) **Case study.** Student registration, online fees and study material access.
- [Gyrate Netcom](https://github.com/sagarai2024-collab/project-case-studies/tree/main/gyrate-netcom) **Case study.** Online grocery store on ASP.NET MVC 5: catalogue, cart, checkout and order tracking.
- [Smart Visa](https://github.com/sagarai2024-collab/project-case-studies/tree/main/smart-visa) **Case study.** Visa application portal on DNN with Telerik, from my 2018 internship.

All case studies are indexed in [project-case-studies](https://github.com/sagarai2024-collab/project-case-studies).

## Elsewhere

[LinkedIn](https://www.linkedin.com/in/sagarika-chakraborty-017530111) · sagarai2024@gmail.com

Happy to talk about RAG in .NET, cost control for LLM apps, or any of the projects above.

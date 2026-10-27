# Sagarika Chakraborty

I'm a technical lead and full stack .NET engineer in Bangalore. For six years I've built C#, ASP.NET Core, React and SQL Server systems for banking, OTT/DTH, real estate and healthcare clients. At DishTV I shipped a RAG support chatbot on Semantic Kernel and Azure OpenAI, and cut its AI API cost by ~90% with intent routing and response caching.

## Start here

**[ConsumerChatbot](https://github.com/sagarai2024-collab/ConsumerChatbot)**
A clean-room rebuild of that chatbot in .NET 9. Greetings go to a fast-path router, repeat questions come from a one-hour cache, and only the rest reach GPT-4o-mini with the retrieved articles. Runs offline with `dotnet run`, no keys needed.

**[Phoenix-Watcho](https://github.com/sagarai2024-collab/Phoenix-Watcho)**
A DTH subscriber self-care portal (React 19, ASP.NET Core 9, EF Core 9) with a RAG assistant that stores embeddings in Supabase pgvector behind an HNSW index and runs on Gemini or OpenAI.

**[notification-api](https://github.com/sagarai2024-collab/notification-api)**
An email notification service where parallel workers cannot claim the same row (`UPDLOCK, READPAST`), duplicate requests collapse under `sp_getapplock`, and failed sends retry with exponential back-off. 58 tests, 22 of them against a real SQL Server.

**[project-case-studies](https://github.com/sagarai2024-collab/project-case-studies)**
Architecture notes for client systems I can't open source, including SAP sync through Dell Boomi, a contractor job platform and a property inspection bidding system.

## Outside work

I wrote The Journey of a Mother, the memoir behind the film Mrs. Chatterjee vs Norway.

## Contact

sagarai2024@gmail.com · [LinkedIn](https://www.linkedin.com/in/sagarika-chakraborty-017530111)

## Shruti Tewaney

Software engineer — backend, cloud, and applied AI.
M.S. Computer Science, University of Chicago, December 2026. Open to full-time roles from January 2027.

Two years on backend teams before the master's: the Laravel/PHP REST services behind 5,000+
point-of-sale transactions a day across 50+ retailers at InvuPOS, where I traced 850ms response
times to repeated record lookups and brought them to 595ms with query tuning and Redis caching,
and built distributed rate limiting on a shared Redis store so quotas held across autoscaled
EC2 instances. Earlier, I helped split a Laravel monolith into five services at ZTech.

Most recently at Valoi AI I worked on the video generation pipeline — classifying failures by
whether they'd repeat and rewriting blocked prompts through the Gemini API to cut failed jobs
~70%, building resumable generation for 40K-word books, and writing automated quality benchmarks
that surfaced a 12 dB loudness gap across every output.

**Python · Go · TypeScript · PostgreSQL · Redis · AWS · Docker · FastAPI · Flask · LangChain**

---

### Projects

**[ask-sql](https://github.com/shruti072003/ask-sql)** — Natural language to SQL. A RAG pipeline
indexes the database schema in ChromaDB and retrieves only the tables a question needs, cutting
token use 60% against passing the full schema. Few-shot retrieval of similar queries improved
multi-table accuracy 35%. A validation layer parses generated SQL and rejects anything that isn't
a read-only SELECT. `Python` `LangChain` `ChromaDB` `FastAPI` `PostgreSQL`

**[gene-annotation-service](https://github.com/shruti072003/gene-annotation-service)** —
Asynchronous genomic annotation on AWS. A Flask API on EC2 is decoupled from compute-heavy
annotation jobs by SQS. Results older than three days tier from S3 to Glacier through Step
Functions, cutting storage cost 80%, with SNS and Lambda restoring on demand. Web, annotator,
and utility tiers run in Docker, isolated across VPC subnets. `Python` `Flask` `AWS` `Docker`

**[parallel-barnes-n-hut](https://github.com/shruti072003/parallel-barnes-n-hut)** — Barnes-Hut
N-body simulation in Go. A quadtree approximates distant particle clusters as a single center of
mass, taking force computation from O(n²) to O(n log n). Parallelized across goroutines with
channel-based work distribution, reaching ~3x speedup on 8 threads, benchmarked on SLURM.
`Go` `Concurrency` `HPC`

---

shruti072003@gmail.com · [LinkedIn](https://www.linkedin.com/in/shruti-tewaney/) · Chicago, IL

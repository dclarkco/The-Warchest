# Benchmark scripts - "The Warchest"

I was having a post-contract debrief with my venerable, selfless, amazing guru of a senior developer at Allan solutions, the company contracted by Benchmark to develop the website, Pro platform, and aspects of the database. We were lamenting that our time working together would come to a close, and discussing next steps for me, as a soon-to-be unemployed data scientist. We reviewed a bit of code to use as work examples, and he affectionately described these two scripts as my "War Chest" of data weaponry designed and deployed at Benchmark.

These scripts saved me, analysts, and the Allan Solutions developers a tremendous amount of time, resolved numerous headaches, and went on to formulate pieces of the ETL and database that are in use today.

## Data Framer:

- A collection of modules used throughout my contract, slowly broken into more and more modular components, features tacked on, and bugs squashed, all to enable the extraction of analyst data from a series of (50+) messy, undocumented, and functionally disparate excel workbooks, each with dozens of similarly disparate sheets. It was truly a monumental task for a sole remote data scientist, but I found joy in solving small problems and automating some aspects of my work.
- Dataframer has modules capable of detecting header rows, cleaning out excel junk, stripping individual cells of whitespace and nonsense characters. It has become a handy little library to import during data engineering work, especially when interfacing with our excel data. Just loads of core data science, data engineering, and data cleaning modules that make up the foundational skills and abilities of a data scientist. Despite these being useful for a short period at Benchmark (once our data warehouse and ETL were designed and implemented, there was no longer a need for these tools), I will upkeep this library as I encounter messy, unorganized, and disparate datasets.

## Corporate Classifier:

- What began as a proof of concept for our ETL, evolved into a bit of code that became particuarly useful when combining datasets from various analysts and markets which referenced the same company names and financial information. This code takes in any excel or csv file, and can extract company names from it, returning tickers, websites, exchanges, and even news sentiment. (via a separate module, still in use at BMI). It became a foundational piece of the Benchmark pre-processing suite, being used to create a comprehensive corpus of company names, tickers, and other related meta-data. This was over-engineered for it's task, but because of this, could quickly be modified with additional modules and objects as requested by various stakeholders.
- Designed as a modular, adaptable, and readable collection of methods to optimize and streamline the collection of, and storing there-in, of Benchmark's massive company corpus (~2000 individual companies, each with anywhere from a dozen to 200 features, depending on mineral market.)
- Implements a bit of NLTK, fuzzy matching, word2vec, and a dollop of ML tools to solve classic data science word corpus problems, in the context of real world data tasks.

# Zepto Dark Store Order & Stock Control Database

AlmaBetter Module 2 capstone by Aditya Siddaarth. SQL/SQLite controls over synthetic quick-commerce records.

**Technical validation: all 26 activities pass the unchanged checker after a fresh-session run. AlmaBetter final evaluation and the learner's explanation video remain pending.**

[Open the working Colab notebook](https://colab.research.google.com/drive/152qOlweD_yHy5-osSV0n3umYVpW7inkC)

## Run

Open the notebook in Colab, make a copy if editing, and select Runtime → Restart session and run all. Dataset generation, the local API and SQLite database are prepared by the supplied setup. No external production service or data upload is required. Read the final activity dashboard and implementation handover.

## Scope

- Seven core entities plus movement, exception and ingestion-audit tables.
- ER diagram with composite keys and required relationships.
- Five GET/POST/PUT/PATCH/DELETE exercises, independently reset for safe reruns.
- Thirteen SQL reports using joins, aggregation, set intersection, functions, standard CTEs and window functions.
- Approved reservation COMMIT and unapproved reservation ROLLBACK with new-connection verification.
- Seven-step automation, grouped exception SQL and four cron expressions.
- Git collaboration and safe database-change diagrams.

## Verified baseline

The deterministic July 2026 dataset has 12 stores, 60 products, 720 inventory positions, 900 orders, 3,150 item lines, 5,618 fulfilment events and 654 deliveries. The control engine creates 3,140 movement records and 226 operational exceptions across seven categories. The final fresh-session run has 26 Passed activities and zero error outputs.

## Classification and validation

Q3 and Q8 derive quantities from item/event evidence and use the exact states SHORT and PARTIAL_PICK. The complete result signatures now match the supplied checker. The expected hashes and validators have not been edited or bypassed, and queries calculate results from source records rather than hardcoded samples.

## Compatibility repair and documentation

The original API setup leaves numeric NaN values in optional event fields. A separate cell casts DataFrames to object before replacing missing values with None, allowing strict JSON null serialization. It preserves business data and original setup/validation code. The notebook contains a debug/AI assistance log, assumptions, PRD mapping, review notes and an 18–20 minute recording guide.

Cron schedules and engineering workflows are design artifacts; this notebook does not run a permanent scheduler or deploy a real database change. All data is synthetic. Original starter resources belong to the course and are linked from AlmaBetter.

# PS2 - **Center for Investigative Reporting: AI-Powered Network Analysis for Real Estate Corruption Investigation**

# **Overview**

Over the past two decades, approximately 2,500 local newspapers have closed, and newsrooms have lost more than half of their staff, creating “news deserts” where vital issues go uncovered. To address this growing accountability gap, the **CIR** is building a petabyte-scale database of government records and aiming to develop an AI-powered analysis tool with your help in order to identify the “smoking gun” patterns hidden within the 0.1% of obscure documents that reveal financial networks and illicit transactions. Once complete, this system will serve as a shared resource for newsrooms nationwide, enabling journalists to uncover buried stories and restore transparency in government, business, and finance.

# **Who We Are**

**The Center for Investigative Reporting (CIR)** is an independent newsroom that empowers the public through groundbreaking storytelling that sparks action, improves lives, and protects our democracy. CIR produces [*Reveal*](https://revealnews.org/), a nonprofit, independent, investigative podcast launched in 2013 and heard by more than 1 million people each week across more than 500 public radio stations in the United States. In addition to *Reveal*, CIR also produces the investigative magazine *Mother Jones* and the podcast *More To The Story*.

# **Context & The Challenge**

Investigative journalists face a detective-like task: uncovering networks of hidden real estate ownership and financial ties buried within **terabytes of heterogeneous, often handwritten records**. Valuable clues are rarely found in obvious deeds or filings but rather in obscure documents—such as apostilles, handwritten notes, notary logs, divorce records, or tax liens—that together expose hidden ownership and illicit transfers.

An investigation might begin by attempting to identify all real estate transactions in wealthy California counties associated with individuals with Slavic surnames, then cross-referencing this information with apostilles, handwritten margin notes, signature lines of managing members of LLCs, and similar evidence. Each piece of evidence appears rarely, but together they could reveal criminal networks. (See data section for record details.)

The challenge: **connect the dots across an ocean of unstructured data**, where key documents represent **less than 0.1%** of total records. Conventional indexing and search discard these rare items as noise—precisely where the real investigative value lies.

## For reference, the **key records** can include:

- Apostilles on international property transactions, showing foreign ownership of assets.
- Handwritten margin notes by partners, secretaries, etc., showing relationships, ownership, you-name-it.
- Signature specimens from managing members of shell LLCs, showing related properties, transactions, partnerships, and shell-company networks.
- Liquor license transfers are tied to property ownership, showing shareholders, subsidiaries, partnerships, and other business relationships
- Lis pendens (lawsuit notices) revealing disputes, names, addresses, and relationships
- Divorce records sometimes reveal relationships, assets, and business functions.
- Federal tax liens may connect assets to owners.
- Death certificates and probate filings in property transfer chains may reveal relationships, wealth, and beneficial ownership arrangements.
- Corporate registration amendments changing ownership, identifying shell companies, beneficial owners, partners, shareholders, and subsidiaries.
- Notary logs and acknowledgments—ditto.

# **Your Solution:**

CIR’s use case flips the traditional search model: the ideal solution preserves and analyzes the long tail of rare documents instead of optimizing for frequent ones. A great solution empowers journalists to address one of more of these challenges:

- Extract and index *key* records and metadata—including stamps, cross-outs, and handwritten annotations, considering
- Support exploratory, cross-document queries spanning multiple record types and quality levels.
- Enable relationship mapping across entities, ownership structures, and transactions.

This is not a consumer property search like Zillow—it’s a forensic analysis engine built to expose hidden networks of money, power, and influence.

![Screenshot 2025-11-07 at 4.52.16 PM.png](attachment:225ef620-bbcc-4947-8f63-b396abdd0b0c:Screenshot_2025-11-07_at_4.52.16_PM.png)

## **Example Queries from Journalists:**

Here are some examples of the types of investigative queries journalists would make:

### **1. Patterns:**

"Find all properties in wealthy coastal counties sold for nominal amounts ($1-$100) to LLCs formed in Delaware, then identify if any of those LLC managing members have signatures that appear on other documents in the trove—including apostilles, liquor licenses, or court filings."

### **2. Cross-Document Search:**

"Find all documents containing Cyrillic text or transliterated Slavic names in a specific county and date range, then show which of those individuals also appear in: (a) international apostilles, (b) as notaries, (c) as LLC managing members, or (d) in court judgments."

### **3. Margin Notes:**

"Search all handwritten margin notes or clerk annotations for terms indicating irregularities and show associated documents and parties involved."

### **4. Time Pattern Analysis**

"Find clusters like this: property purchased → LLC formed within 60 days → liquor license transferred within 90 days → property sold within 2 years. Flag all instances matching this pattern."

### **5. Signature Matching:**

"Given a signature specimen from a known individual, find all documents where this person signed as LLC manager, notary, or grantor—even if they used different name variations or spellings."

### **6. Tracing Networks:**

"Starting from a specific individual or property, trace all ownership connections through any number of intermediate entities (LLCs, trusts, nominees) and identify all properties ultimately controlled."

# **Relevant Datasets & Helpful Resources**

In its initiative of building a first-of-its-kind reporting tool suite for follow-the-money investigations, the CIR has been building one of the largest databases of real estate records of California counties, ultimately reaching petabyte scale. The current record consists of approximately seven terabytes of TIFF scanned property documents from San Francisco and Orange Counties etc..

For the hackathon event, Matt from CIR preprocessed a slice of TIFF data (property documents requested from San Francisco County of year 2025) for teams to make it available as OCRed PDFs (~32GB unzipped) for teams to prototype their solution, along with the TIFF data (:

- [CIR: 2025 Property Documents from San Francisco County [Hugging Face]](https://huggingface.co/datasets/sfmattsmith/CIR/tree/main)
    - https://huggingface.co/datasets/sfmattsmith/CIR/tree/main
    - Permission: gated access (auto-approval for the duration of HSI 2025 event)
        - folder `verbatim_shards/` contains .tar TIFF files & description
        - files `01.zip, 02.zip … 09.zip` are zipped OCR data

### Public data & links for inspiration:

Journalists have long used specialized databases to find and corroborate stories:

- [OCCRP Aleph](https://aleph.occrp.org/) is an investigative data platform that enables reporters worldwide to track the flow of money. We provide public access to a vast archive of government records and an open database.
- [OCRed real estate records from New York City](https://www.nyc.gov/site/finance/property/acris.page)
    - New York City is a rare jurisdiction that has done an OCR scan of its real estate records while also providing a true full-word search interface to the public.
- [The International Consortium of Investigative Journalists database of offshore leaks](https://offshoreleaks.icij.org/)
    - contains information about nearly 1 million offshore entities, such as shell companies, linking people and assets to more than 200 countries and territories. Like OCCRP-Aleph journalists worldwide, use it to name the real owners of those opaque structures.
- [Evictorbook](https://evictorbook.com/)
    - a tool made by the Anti-Eviction Mapping Project that combines data on property ownership, eviction records, and corporate business filings.
- [“Big Local News,”](https://cjlab.stanford.edu/projects/big-local-news/) collects, processes, and shares governmental data to help teach best practices to students seeking stories within the data.

# **Evaluating the Solution/Judging Criteria**

## **2-Day Hackathon Metrics:**

Judges will evaluate the solutions of teams on the following:

- **Accuracy:**
    
    Does the system correctly identify entity relationships across document types and name variations? Are false negatives minimized to avoid missing key connections?
    
- **Completeness:**
    
    Does the solution preserve all potentially relevant content—including handwriting, stamps, and margin notes—rather than filtering out “unimportant” data?
    
- **Verifiability:**
    
    Are outputs fully traceable to original documents and page references for journalistic fact-checking and collaboration?
    
- **Usability:**
    
    Can reporters without coding experience conduct complex investigations easily through natural language or intuitive interfaces?
    

## **Long-term Success Metrics:**

- **Performance:**
    
    Does the system return results for multi-document or pattern queries within a practical timeframe (target: under 60 seconds)?
    
- **Flexibility:**
    
    Can it handle ad-hoc exploratory queries, not just predefined searches, allowing reporters to ask new questions as investigations evolve?
    
- **Scalability:** Is the architecture designed to scale efficiently to petabyte-level datasets across multiple counties without major performance loss?
- **Impact**: Investigative journalists are able to leverage this system to expose corruption/money laundering in much shorter time than traditional methods
# QA-Assist

**QA-Assist** is an automation tool designed to streamline and enhance the Quality Checking process for documents and datasets. It transforms manual, error-prone QA tasks into a reliable, efficient, and measurable workflow, helping teams maintain high-quality outputs while saving time and resources. QA Assist is a client-side, offline-first quality assurance application designed to validate, compare, and analyze legal and financial documents against approved templates and Golden Source reference data. The system is fully deterministic and rule-based — no AI or LLMs — ensuring explainability, auditability, and data privacy.

> ⚠️ **Note:** This repository contains a **portfolio version of a workflow I personally designed**. It uses **dummy data for demonstration purposes**. The production workflow I created is LOB-specific hence implemented differently and separately in the company environment for operational use.


---

## Main Purpose

The main purpose of QA-Assist is to **automate and improve the QA process**, enabling teams to:

- Detect errors quickly – Identify missing, inconsistent, or incorrect information without manually reviewing every document.  
- Ensure data integrity – Maintain consistency and accuracy across datasets and document versions.  
- Prioritize issues efficiently – Use risk scoring to focus on the most critical errors first.  
- Provide actionable insights – Visualize trends, error patterns, and performance metrics through dashboards and reports.  
- Reduce manual workload – Save time and resources while improving QA efficiency.  
- Operate securely – Process all data locally, keeping sensitive information private and protected.  

In short, QA-Assist turns QA from a time-consuming task into a **streamlined, reliable, and measurable process**.

---

## Issues Solved / Impact

QA-Assist addresses common challenges in manual QA processes:

1. **Time-consuming manual checks**  
   - Automates repetitive checks, saving hours of manual work.  

2. **Human error and inconsistencies**  
   - Accurately detects missing fields, inconsistencies, and document discrepancies.  

3. **Difficulty prioritizing issues**  
   - Risk Scoring Engine helps focus on the most critical errors first.  

4. **Lack of measurable insights**  
   - Dashboards provide metrics like error trends, most common issues, and time saved vs manual QA.  

5. **Security and confidentiality risks**  
   - Runs offline, ensuring sensitive data is never stored externally.  

**Impact:**  
QA-Assist allows teams to **work faster, reduce errors, make informed decisions, and maintain consistent quality**, turning QA from a bottleneck into a strategic advantage.

---

## Features / What We’ve Done So Far

- ✅ **Error Detection & Validation** – Automatically identifies inconsistencies and missing fields in documents.  
- ✅ **Consistency Checks** – Compares datasets or document versions for discrepancies.  
- ✅ **Redline & Comparison Tools** – Highlights changes between documents for easy review.  
- ✅ **Risk Scoring Engine** – Assigns priority scores to issues based on impact.  
- ✅ **Reporting & Analytics Dashboard** – Visualizes QA metrics such as error trends, common missing fields, and time saved.  
- ✅ **Offline Support & Security** – All processing is local to protect sensitive data.  

---

## Project Structure

The repository includes:

- Source code for QA-Assist modules  
- Example datasets and documents  
- Sample reports and dashboards  
- Documentation and additional resources  

---

## Usage

1. Load documents or datasets into QA-Assist.  
2. Run QA modules to detect inconsistencies.  
3. Review reports and dashboards for actionable insights.  
4. Export results as needed.

---

## Technology Stack

### Core Technologies

| Category | Technology | Purpose |
|--------|-----------|---------|
| Frontend Framework | React 18.3 | UI component framework |
| Build Tool | Vite 5.4 | Fast development & bundling |
| Language | TypeScript 5.8 | Type-safe application logic |
| Styling | Tailwind CSS 3.4 | Utility-first styling |
| UI Components | Radix UI + shadcn/ui | Accessible component primitives |
| State Management | TanStack React Query | Server/state caching |
| Routing | React Router DOM 6.30 | Client-side routing |
| Charts | Recharts 2.15 | Data visualization |
| Forms | React Hook Form + Zod | Form handling & validation |
| Theming | next-themes | Dark / Light mode |

---

## Document Processing Libraries

| Library | Version | Function |
|------|---------|----------|
| pdfjs-dist | 4.4.168 | PDF text extraction & rendering |
| mammoth | 1.8.0 | DOCX to text/HTML conversion |
| tesseract.js | 7.0.0 | Offline OCR for scanned documents |

---

## NLP & Text Processing Modules (Rule-Based)

| Module | File | Capability |
|------|------|-----------|
| Clause Diff Engine | clauseDiffEngine.ts | Word-level diff, LCS algorithm, redlining |
| Clause Extractor | clauseExtractor.ts | Clause detection, section parsing, deduplication |
| Clause Template Library | clauseTemplateLibrary.ts | Approved clause storage & matching |
| Consistency Checker | consistencyChecker.ts | Cross-document validation using Golden Source |
| Document Classifier | documentClassifier.ts | Legal document type identification |
| Document Parser | documentParser.ts | Text extraction & structure detection |
| Facility Extractor | facilityExtractor.ts | Financial terms & amount extraction |
| Field Type Detector | fieldTypeDetector.ts | Entity recognition (names, dates, accounts) |
| Layout Parser | layoutParser.ts | Headers, footers, and layout structure |
| LOB Config Engine | lobConfigEngine.ts | Line-of-Business rule customization |
| Narrative Extractor | narrativeExtractor.ts | Role extraction (Guarantor, Principal, etc.) |
| OCR Engine | ocrEngine.ts | OCR pipeline integration |
| Placeholder Resolver | placeholderResolver.ts | Placeholder to Golden Source mapping |
| QA Engine | qaEngine.ts | End-to-end QA workflow orchestration |
| Report Generator | reportGenerator.ts | QA summary & findings |
| Risk Scoring Engine | riskScoringEngine.ts | Risk classification (Low to Critical) |
| Role Mapper | roleMapper.ts | Entity role identification |
| Security Utilities | securityUtils.ts | Sanitization & in-memory safeguards |
| Template Detector | templateDetector.ts | Template recognition |
| Validation Rules | validationRules.ts | Deterministic field validation logic |

---

## NLP Techniques Implemented (No Machine Learning)

| Technique | Description |
|--------|-------------|
| Text Normalization | Case folding, punctuation cleanup, whitespace normalization |
| Tokenization | Word-level tokenization with placeholder preservation |
| Pattern Matching | Regex-based extraction (dates, accounts, amounts) |
| Similarity Scoring | Jaccard-style word overlap |
| Longest Common Subsequence (LCS) | Clause-level diff & redline generation |
| Role Extraction | Pattern-based legal role detection |
| Entity Recognition | Rule-based name, address, and date detection |
| Fuzzy Matching | Near-match detection with confidence scoring |
| Deduplication | Normalized clause title comparison |

---

## Application Features

| Feature | Component | Description |
|------|----------|------------|
| Document Upload | DocumentUpload.tsx | PDF & DOCX intake with password support |
| Document Preview | DocumentPreview.tsx | In-app document viewer |
| Document Management | DocumentList.tsx | Uploaded document tracking |
| Validation Results | ValidationResults.tsx | Pass / Flag / Fail validation |
| Consistency Checker | ConsistencyChecker.tsx | Cross-document field matching |
| Redline Viewer | RedlineViewer.tsx | Visual diff vs approved templates |
| Document Comparison | DocumentComparer.tsx | DOCX to PDF integrity checking |
| Golden Source Panel | GoldenSourcePanel.tsx | Reference data management |
| Placeholder Mapping | PlaceholderResolutionPanel.tsx | Placeholder resolution workflow |
| Template Management | TemplateManagementPanel.tsx | Clause template CRUD |
| QA Summary | QASummary.tsx | Consolidated QA findings |
| Processing Report | ProcessingReport.tsx | Metadata & processing logs |
| Risk Dashboard | RiskDashboard.tsx | Risk scoring visualization |
| Analytics Dashboard | AnalyticsDashboard.tsx | KPIs & trend analysis |
| Demo Mode | Demo Components | Guided demo with sample data |
| Theme Toggle | ThemeToggle.tsx | Light / Dark mode |

---

## Machine Learning Status

| Category | Status |
|------|--------|
| Traditional ML | Not Implemented |
| LLM / AI APIs | Not Implemented |
| Embeddings / RAG | Not Implemented |
| Rule-Based NLP | Implemented |

---

## Security & Compliance

- In-memory document processing only
- No document data written to disk
- Fully offline execution
- No external API calls
- Password-protected PDF handling in memory
- Batch processing (50 pages per batch, up to 1000 pages)

---

## Architectural Principles

1. Offline-first design with no cloud dependency  
2. Deterministic, rule-based QA  
3. Human-in-the-loop assistance (no auto-approval)  
4. Type-aware field matching  
5. Dynamic Line-of-Business configuration  
6. Golden Source as system of record


---

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

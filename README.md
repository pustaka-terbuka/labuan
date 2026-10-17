# Pustaka Terbuka — PAPL (Perpustakaan Awam Perbadanan Labuan)

> **Pustaka Terbuka: Katalog Induk Terbuka untuk Perpustakaan dan Sekolah Malaysia.**  
> *Official Perpustakaan Awam Perbadanan Labuan (PAPL) Bibliographic Dataset & Standalone Harvester.*

This repository contains the harvested open MARCXML collection and harvester pipeline for **Perpustakaan Awam Perbadanan Labuan** (`PAPL`), contributing to the national Malaysian union catalog at [pustaka-terbuka/opac](https://github.com/pustaka-terbuka/opac).

---

## Institutional Metadata

| Attribute | Value |
| :--- | :--- |
| **Institution Code** | `labuan` |
| **Agency Code** | `PAPL` |
| **Official Name** | Perpustakaan Awam Perbadanan Labuan |
| **Institution Type** | `public` |
| **State / Territory** | Labuan |
| **Target End Bib** | 80,000 |
| **OPAC Base URL** | [https://library.pl.gov.my/](https://library.pl.gov.my/) |
| **Subject Focus** | Borneo maritime, local history, and public community literature |

---

## Directory Structure

```text
labuan/
├── README.md                      # Institutional repository documentation
├── package.json                   # Node.js project specification & scripts
├── harvest/
│   └── inbox/labuan/             # Sealed MARCXML batch chunks and manifests
│       └── <run-id>-chunk-001/
│           ├── manifest.json      # Chunk SHA-256 manifest & metadata
│           ├── provenance.jsonl   # Record-level attribution and fetch logs
│           └── records/           # Batched MARC21 slim XML files
├── tools/
│   ├── harvesters/labuan/        # Automated OPAC crawler & XML converter
│   └── lib/                       # Supporting MARCXML and validation utilities
└── tests/
    └── harvester-labuan.test.js  # Autonomous test suite
```

---

## Usage

```bash
# Install dependencies
npm install

# Test run harvester (10 sample records)
npm run harvest:sample

# Run full collection sweep
npm run harvest:full

# Validate dataset integrity
npm run validate-inbox harvest/inbox/labuan/<chunk-directory>
```

---

## Attribution & License

Dataset harvested and preserved under open library metadata standards for educational, civic, and cooperative indexing. Attribution: **Perpustakaan Awam Perbadanan Labuan (PAPL)** & **Pustaka Terbuka**.

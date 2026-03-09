# US Law Enforcement Agency Directory

A tab-separated dataset of **17,985 U.S. law enforcement agencies** compiled from FBI Crime Data Explorer / UCR program data (2024).

## File

**`US-law-enforcement-agencies.tsv`** — one row per agency, tab-delimited.

| Column | Description | Example |
|--------|-------------|---------|
| `name` | Agency name | Houston Police Department |
| `type` | Agency category | Local police department |
| `state` | Two-letter state code | TX |
| `county` | County or equivalent | Harris |
| `city` | City or municipality | Houston |
| `zip` | 5-digit ZIP code | 77073 |

### Agency types

| Type | Count |
|------|-------|
| Local police department | 12,499 |
| Sheriff's office | 3,063 |
| Special jurisdiction | 1,719 |
| Constable/marshal | 638 |
| Primary state law enforcement agency | 50 |

## Known limitations

- **16 rows have missing city/zip** — these agencies had malformed source data. The name, type, state, and county are present but city and zip are blank.
- **No officer counts, contact info, or FOIA endpoints** — this is a location/classification directory only.
- **ZIP codes** were originally stored as integers, stripping leading zeros from northeast states. These have been zero-padded back to 5 digits.

## Source

FBI Crime Data Explorer: https://cde.ucr.cjis.gov/

The underlying data comes from the FBI's Uniform Crime Reporting (UCR) program, which collects agency information from law enforcement agencies nationwide.

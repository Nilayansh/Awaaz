# Backend (to be built)

Planned: FastAPI service that receives citizen reports, calls the Sarvam APIs, extracts and tags claims, links related reports into Problem Dossiers, and generates evidence-linked BRDs.

Planned endpoints (draft):

- `POST /reports`: submit a report (text or audio, optional photo and GPS)
- `GET /dossiers`: list problem dossiers
- `GET /dossiers/{id}`: dossier details with linked reports
- `POST /dossiers/{id}/brd`: generate the BRD
- `GET /claims/{id}/proof`: Prove This Claim, returns the source reports behind a claim

Status: not started. Build begins at the hackathon (Oct 17-18, 2026).

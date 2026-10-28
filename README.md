# SBT-DF204 Case Study 4 — Evidence Package

**Student:** Mary-Joy Adewole
**Registration number:** 2025/FWSD/11468
**Course:** SBT-DF204 — Computer Forensics Case Studies
**Case title:** Investigating Rhino Possession Evidence

## What this package contains

- `SBTDF204_CaseStudy4_2025-FWSD-11468.pdf` — the full report (29 pages), with executive
  conclusion, method, findings for all 8 investigation questions, a UTC timeline (9 events across 4
  artefact families), an evidence log (E01–E19+), limitations/alternative explanations, and appendices.
- `screenshots/` — every labelled figure used in the report, as individual PNG files, named to match
  the figure numbers in the report.
- `evidence_records/` — every command-output and hash file generated during the examination (hashes,
  `fsstat`/`fls` output, PhotoRec logs, FTP/HTTP header extracts, EXIF output, steghide checks, the
  `john`/`zip2john` run output, etc.), as the plain text files the report's Appendix D references.

## What this package deliberately does NOT contain

In line with the assessment brief's submission rules, the following originals and reconstructed
binaries are **not** included, and were not uploaded anywhere:

- The original USB disk image (`RHINOUSB.dd`)
- The original packet captures (`rhino.log`, `rhino2.log`, `rhino3.log`)
- The password-protected archive (`contraband.zip`) and its extracted/recovered contents
- The downloaded Windows executable (`rhino.exe`)

These remain only on the course VM. If your lecturer specifically requests any of them, they can be
pulled from the VM's shared folder — see the chat reply accompanying this package for the exact
commands.

## Sensitive evidence note

The FTP session in this case exposed a plaintext username and password, and the archive's password
was recovered using the course's authorised, course-only recovery workflow (`zip2john` + `john` against
the supplied `rockyou.txt` wordlist). Both are recorded once, in full, in the evidence log for the
assessor's verification, and are blurred/redacted in every screenshot. These credentials were not
reused anywhere outside this archive.

## Examination summary

All analysis was performed offline, on working copies only, inside an isolated Kali Linux VM. No
recovered or reconstructed file was executed, no host or account named in the material was contacted,
and no password-recovery technique was applied outside the single authorised step on the supplied
training archive. See the report's Section 7 for the full discussion of limitations and alternative
explanations, including that the USB disk image and the FTP/HTTP captures cannot be shown to involve
the same device or person.

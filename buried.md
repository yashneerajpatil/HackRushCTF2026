# Buried — steg (30 pts)

## Challenge
A PDF file that taunts you to find hidden text within the document.

## Approach
The PDF content was full of misdirection ("no flag here", "good luck").
I recognized this as a classic rabbit hole and checked the file metadata first.

## Solution
```bash
pdfinfo confidential.pdf
```
Output revealed the flag stored in the `Keywords` metadata field.

## Flag
`HRCTF{h4ck3r_bh41_h4ck3r}`

## Lesson learned
check file metadata before diving into content.
For PDFs: `pdfinfo`, for images: `exiftool`, for any file: `strings <file>`

---
name: essay-translate
description: Translate Chinese academic manuscripts into submission-ready English and return a bilingual DOCX with line-by-line pairing (one Chinese sentence followed by its English translation). Use when the user provides a Word document and needs accurate, natural, rigorous academic translation for a target journal; always ask for the target journal name first if missing.
---

# Essay Translate

## Overview

Act as an international Chinese-English academic translation expert.
Translate Chinese manuscript content into clear, publication-oriented English and output a DOCX where each Chinese sentence is immediately followed by its English translation.

## Required Intake

Before any translation, confirm these inputs:
- Target journal name (mandatory)
- Input DOCX path
- Preferred output DOCX path (or confirm auto-generated path)

If the journal name is missing, stop and ask:
`Please provide the target journal name for this manuscript.`

## Translation Style Rules

Apply these style constraints consistently:
- Use accurate terminology and precise meaning transfer.
- Keep expression natural, grammar rigorous, and logic coherent across sentences.
- Prefer simple, concise, and direct academic sentences.
- Avoid overly long sentence structures and obscure vocabulary.
- Use passive voice when useful, but do not force it.
- Keep terminology consistent through the full manuscript.

## DOCX Workflow

1. Read the source DOCX.
2. Preserve document order, including headings and normal paragraphs.
3. For each Chinese sentence, produce one English translation.
4. Write bilingual output in strict pair order:
   - Chinese sentence
   - English translation
5. Keep one blank line between sentence pairs for readability.
6. Save as a new DOCX file. Default naming:
   `<original-name>-bilingual-<journal-key>.docx`

If content cannot be safely segmented into sentences, segment conservatively and preserve original meaning.

## Output Structure Rules

For the generated DOCX:
- Keep sentence-level pairing only. Do not place all Chinese first and all English later.
- Each Chinese sentence must be immediately followed by its English sentence.
- Do not omit source text.
- Do not add extra interpretation not present in the source.

For the chat response after processing:
- Report target journal used.
- Report output DOCX path.
- Briefly list any ambiguity or terminology decisions.

## Journal Adaptation

After receiving the target journal name:
- Align tone and formality to mainstream engineering and energy journals.
- Keep language neutral and evidence-oriented.
- Prefer standard academic wording over decorative style.

If the user requests a specific journal guide later, apply it while keeping the simplicity constraints above.

## Fallback Mode

If the user provides plain text instead of DOCX:
- Translate with the same sentence-pair format in chat.
- Ask whether to convert the result into DOCX afterward.

You are editing a structured radiology report.

TASK

Review the CURRENT TEMPLATE and CURRENT DICTATION together. The template is the starting report. Modify only the template fields that must change because of findings explicitly stated in the dictation. Keep every other template field and statement unchanged.

RULES

1. The CURRENT TEMPLATE is authoritative for structure, field names, field order, and normal wording.
2. Compare every statement in the DICTATION with the matching anatomical field in the TEMPLATE.
3. If the dictation describes an abnormality, replace or revise only the corresponding normal template statement.
4. Route each dictated finding to the correct anatomical field. Do not place findings in unrelated fields.
5. Preserve all template fields and normal statements that are not affected by the dictation.
6. Do not remove an unaffected field.
7. Do not add findings based on the modality, body part, study description, patient age, patient sex, or general medical knowledge.
8. Do not infer findings that are not explicitly supported by the dictation.
9. Correct clear dictation spelling errors and shorthand only when the intended meaning is unambiguous.
10. If the dictation states that the remainder is normal, retain the applicable normal template statements.
11. Use `OTHER FINDINGS:` only when a dictated finding cannot reasonably be assigned to an existing template field.
12. Do not create new anatomical fields when an appropriate template field already exists.
13. Modify the IMPRESSION so it summarizes the important abnormal findings explicitly supported by the dictation.
14. The IMPRESSION must not contain findings absent from the dictation.
15. Do not include normal template findings in the IMPRESSION unless necessary to clarify an important negative finding.
16. Do not copy content from any other case, example, or reference reading.
17. Do not include explanations, commentary, analysis, labels, or Markdown fences.

STRICT OUTPUT REQUIREMENTS

- Return exactly one report.
- Return only the completed report.
- Include exactly one `FINDINGS:` heading.
- Include exactly one `IMPRESSION:` heading.
- Never repeat, nest, or add another `FINDINGS:` or `IMPRESSION:` heading.
- Do not output any text before `FINDINGS:`.
- Do not output any text after the impression.
- Preserve the template's field order and formatting exactly.
- Copy every template field into the output, including fields that remain unchanged.
- Never output square-bracket placeholders, instructions, explanations, or the words `FINAL OUTPUT FORMAT`.

CURRENT CASE PARAMETERS

Modality: {modality}
Body part: {body_part}
Study description: {study_description}
Patient age band: {patient_age_band}
Patient sex: {patient_sex}

CURRENT TEMPLATE

{template_content}

CURRENT DICTATION

{dictation}

OUTPUT THE COMPLETED REPORT NOW.
Start with `FINDINGS:` and end after the completed `IMPRESSION:` text.
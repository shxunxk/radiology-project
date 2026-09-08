You are editing a structured radiology report.

TASK

Review the CURRENT TEMPLATE and CURRENT DICTATION together. The template is the starting report. Modify only the template fields that must change because of findings explicitly stated in the dictation. Keep every other template field and statement unchanged.

RULES

1. The CURRENT TEMPLATE is authoritative for structure, field names, field order, and normal wording.
2. Compare every statement in the DICTATION with the matching anatomical field in the TEMPLATE.
3. If the dictation explicitly describes a finding for a template field, replace or revise only the corresponding template statement. Do not modify any other field.
4. Route each dictated finding to the correct anatomical field. Do not place findings in unrelated fields.
5. Preserve all template fields and normal statements that are not affected by the dictation, except that `OTHER FINDINGS` must never be output.
6. Do not remove an unaffected field.
7. Do not add findings based on the modality, body part, study description, patient age, patient sex, or general medical knowledge.
8. Do not infer findings that are not explicitly supported by the dictation.
9. Correct clear dictation spelling errors and shorthand only when the intended meaning is unambiguous.
10. If the dictation states that the remainder is normal, retain the applicable normal template statements.
11. Use only the named categories and field labels that are present in the current template's `FINDINGS` section. Do not output an `OTHER FINDINGS` field, even if it appears in another case or example. Do not add any new category or field.
12. Do not create new anatomical fields when an appropriate template field already exists.
13. Modify the `IMPRESSION` so it summarizes the important abnormal findings explicitly supported by the dictation.
14. The `IMPRESSION` must not contain findings absent from the dictation.
15. Do not include normal template findings in the `IMPRESSION` unless necessary to clarify an important negative finding.
16. Do not copy content from any other case, example, or reference reading.
17. Do not include explanations, commentary, analysis, labels, or Markdown fences.
18. Treat `template_content` as a locked form. First identify its exact named `FINDINGS` fields and its `IMPRESSION` text.
19. Reproduce only the named `FINDINGS` field labels present in this template, in exactly the same order. Do not rename, merge, split, remove, or reorder those fields, except never output `OTHER FINDINGS`.
20. Keep each field's template wording unchanged unless the dictation explicitly describes a finding for that field. An empty or unrelated dictation must not cause a field to be changed or populated.
21. Do not add any new anatomical field, heading, tag, section, bullet, numbering, placeholder, category, or field. Do not copy fields from another case, example, or reference report.
22. Keep each dictated abnormality under the existing matching template field. Never place an abnormality in a newly invented field, under a different field, or under `OTHER FINDINGS`.
23. The `IMPRESSION` must be one concise replacement of the template impression. Do not append a second impression, repeat findings, or add recommendations not explicitly stated in the dictation.
24. If no dictated abnormality affects a template field, copy that field verbatim. If no dictated abnormality affects the `IMPRESSION`, preserve the template impression verbatim.

STRICT OUTPUT REQUIREMENTS

- Return exactly one report.
- Return only the completed report.
- Include exactly one `FINDINGS:` heading.
- Include exactly one `IMPRESSION:` heading.
- Never repeat, nest, or add another `FINDINGS:` or `IMPRESSION:` heading.
- Do not output any text before `FINDINGS:`.
- Do not output any text after the impression.
- Preserve the template's field order and formatting exactly.
- Copy only the named template fields into the output, including unaffected fields; never output `OTHER FINDINGS`.
- The output must contain exactly the same allowed top-level sections and field labels as `template_content`: one `FINDINGS:` section followed by one `IMPRESSION:` section, with no `OTHER FINDINGS` field.
- Do not output any XML/HTML/JSON tags, Markdown headings, bullets, list numbers, comments, or wrapper text.
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
Copy the template structure first, apply only dictation-supported edits, then output exactly one report. Start with `FINDINGS:` and end after the completed `IMPRESSION:` text.
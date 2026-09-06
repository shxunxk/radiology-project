You are editing a radiology template.

Goal:
Convert the dictation into a completed structured radiology report by modifying the supplied normal template.

Rules:
1. Treat the template as the starting report, not as an example.
2. Route every dictated finding to the matching FINDINGS field.
3. Replace or modify the corresponding normal statement when the dictation describes an abnormality.
4. Preserve template statements for routinely visualized regions that were not mentioned in the dictation.
5. Update the IMPRESSION to summarize only the important abnormal findings.
6. Do not add findings unsupported by the dictation or template.
7. Preserve the supplied template wording and field order whenever possible.
8. Keep the output structured exactly as:
   FINDINGS:
   ...
   IMPRESSION:
   ...

9. If the template contains an OTHER FINDINGS field, use it only for relevant findings that do not belong elsewhere. Leave it empty when not needed.
10. Use modality, body part, study description, age band, and sex only as context; they do not provide additional findings.
11. There should only be 1 FINDINGS and 1 IMPRESSIONS SECTION.

Input:
- Modality: {modality}
- Body part: {body_part}
- Study description: {study_description}
- Patient age band: {patient_age_band}
- Patient sex: {patient_sex}

Template:
{template_content}

Dictation:
{dictation}

Output:
Return only the final report in this exact format:

FINDINGS:
...
IMPRESSION:
...

Example:
{few_shot}
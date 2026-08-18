# Implementation Issues

* No blocking issues found during implementation.
* `Borra_Bhavitha_CV.pdf` and `profile.jpg` were confirmed present in the directory and linked directly; contents/validity of the PDF itself were not inspected.
* All contact links (emails, LinkedIn, GitHub) are taken verbatim from spec.md and were not independently verified as live/reachable.

## Update (spec revision: lavender bg, inline skills, coursework/JEE ranks, extra-curricular section)
* The updated spec's Hero/Header bullet list no longer includes the "Tagline" line (`Mathematics, Computing & AI`) that was present in the previous spec version. This was not called out among the requested changes, so it's flagged here rather than silently assumed intentional. It has been removed from the hero markup to match the current spec text; restore it if the omission was accidental.
* The spec's coursework and extra-curricular bullets contained `[cite: 3]` citation-marker artifacts (leftover from a source document) — these were stripped from the rendered content since they are not meant to be displayed to site visitors.
* Corrected an apparent typo in the coursework list: "Introdution to Automata Theory and Computability" → "Introduction to Automata Theory and Computability".

## Update (profile picture filename)
* spec.md's text still literally reads "use the local file: profile.jpg" — it was not actually edited to name a new file. However, the directory no longer contains `profile.jpg`; the only image asset present is `profile_new.jpg`. `index.html` was updated to reference `profile_new.jpg` based on this filesystem evidence. Recommend updating spec.md's text to match if this filename is expected to stay.

## Update (hero side-by-side layout)
* The updated spec's Hero bullet lists "Name, Subtitle, Tagline" as the text block to sit beside the photo, but no "Tagline" element exists on the page (it was removed in an earlier revision at the spec's own prior instruction). Per this task's "do not change any other sections" instruction, no tagline was reintroduced — only Name and Subtitle are shown in the right-hand text column. Flagging in case the tagline's return was intended.

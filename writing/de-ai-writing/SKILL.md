---
name: de-ai-writing
version: 0.0.1
description: Diagnose and revise formulaic, stiff, generic, or translation-like Chinese and English writing while preserving facts, author intent, evidence strength, and the author's genuine voice. Supports academic manuscripts, long-form articles, professional writing, and product or UI copy.
---

# De-AI Writing Skill

## Purpose

Improve the naturalness, specificity, rhythm, and authorial character of AI-assisted or human-written text. The goal is better writing—not disguising AI authorship, defeating AI detectors, or making every author sound the same.

Use this skill when a user asks to humanize text, remove AI-like phrasing, reduce formulaic language, make Chinese prose sound less machine-translated, improve an English draft, audit a whole article for generic writing patterns, or adapt text to an author's established voice.

This skill implements a nine-part capability map supplied for this repository. The names below describe functional modules; they are not claims that third-party source code has been bundled or redistributed.

## Non-negotiable principles

1. **Meaning before style.** Preserve the author's intended claims, reasoning, scope, tone, and audience.
2. **Facts before fluency.** Never invent data, experiments, citations, personal experiences, observations, motivations, quotations, or evidence to make prose sound authentic.
3. **Evidence strength must not change.** Do not turn association into causation, prediction into validation, possibility into certainty, or a limited finding into a universal claim.
4. **Author voice over generic polish.** Do not replace one generic AI voice with another polished but impersonal voice.
5. **Edit for quality, not detector outcomes.** Do not optimize for AI-detection scores, promise detector evasion, or introduce deliberate errors and distortions to disguise AI involvement.
6. **Do not over-edit.** Keep a sentence or paragraph when it is already clear, specific, and appropriate.
7. **Respect disclosure rules.** Follow the user's journal, institution, employer, publisher, and platform requirements for disclosure of AI assistance.

## When to activate

Activate this skill for requests such as:
- “去掉 AI 味 / 去 AI 化 / 写得像人一点”
- “这段太像 AI 写的，帮我改自然”
- “减少套话、排比、假大空和过度总结”
- “检查全文为什么读起来像 AI”
- “把英文改得地道，不要像中文直译”
- “按我自己的写作习惯改”
- “优化公众号长文、科研论文、报告、邮件或产品文案的表达”

Do not assume that every formal, structured, or technically precise text is AI-like. Diagnose before editing.

## Nine capability modules

Choose only the modules that address the diagnosed problem. Multiple modules can be combined.

### 1. Humanizer — natural English editing

Use for English that is grammatically correct but stiff, over-formal, repetitive, or translation-like.

- Replace literal Chinese-to-English constructions with idiomatic English while preserving the claim.
- Reduce unnecessary nominalizations, stacked modifiers, and repetitive sentence openings.
- Use active voice when it clarifies the actor; retain passive voice when the method, process, or result is the appropriate focus.
- Remove empty transitions and generic phrases when they add no information.
- Do not force contractions, slang, or casual language into academic or professional writing.
- Do not vary sentence length mechanically.

### 2. Humanizer-zh — natural Chinese editing

Use for Chinese prose that sounds translated, inflated, overly formal, or full of stock expressions.

- Prefer concrete subjects, actions, objects, and evidence over abstract slogans.
- Remove empty phrases such as “值得注意的是”, “不难发现”, “具有重要意义”, “提供了新的见解”, or “综上所述” when they merely announce what the sentence already says.
- Reduce habitual “首先—其次—最后”, “不仅……而且……”, and three-part parallel structures when the logic does not require them.
- Avoid excessive nominalization, stacked abstract nouns, and grand conclusions unsupported by the content.
- Keep natural Chinese word order and appropriate information flow; do not translate English syntax word for word.
- Do not make formal writing artificially colloquial. Match the intended genre.

### 3. Stop-slop — whole-document diagnosis

Use before rewriting a long article, manuscript, report, or multi-section document.

Inspect the document as a whole for:
- Repeated paragraph templates and identical topic-sentence patterns.
- Repeated conclusions that restate the same point without adding evidence.
- Too many introductory or transitional sentences that delay the actual point.
- Uniform paragraph length and an overly regular rhetorical rhythm.
- Repeated triads, parallel clauses, rhetorical questions, and “not only…but also” constructions.
- Inflated significance statements and claims that exceed the evidence.
- Sections that could be reordered, shortened, merged, or removed.
- A mismatch between the title, central argument, evidence, and conclusion.

Return a prioritized diagnosis before large-scale editing. Distinguish structural problems from sentence-level problems. Do not rewrite the whole document if a few targeted changes are sufficient.

### 4. Taste — editorial judgment for product and interface writing

Use for landing pages, product descriptions, UI text, onboarding, feature announcements, and brand or product copy.

- Make the value proposition concrete: who the feature serves, what it does, and why the reader should care.
- Prefer precise verbs and useful details over unsupported superlatives such as “revolutionary”, “seamless”, “powerful”, or “next-generation”.
- Keep headings, labels, buttons, helper text, and body copy consistent in tone and terminology.
- Remove generic marketing filler and repeated claims.
- Respect the product's actual capabilities. Never promise functions, performance, security, or outcomes that have not been verified.
- Optimize for clarity, hierarchy, and usability—not fashionable wording or decorative cleverness.

### 5. AI-flavor-remover — Chinese long-form editing

Use for public-account articles, essays, commentary, social posts, and other long Chinese-form content.

- Identify where the text announces an opinion instead of demonstrating it.
- Replace broad claims with the concrete example, observation, evidence, or reasoning already present in the source.
- Remove repetitive openings, recap paragraphs, forced emotional crescendos, and formulaic endings.
- Preserve the author's stance and degree of certainty.
- Keep paragraph breaks where they help the reader; do not force “one sentence per paragraph” or merge everything into dense blocks.
- Do not fabricate anecdotes, field experience, dialogue, quotations, or personal details.

### 6. Shorenhua — conversational Chinese naturalization

Use when Chinese sounds like a machine translating or reciting a formal template.

- Read the text aloud mentally and locate phrases that a real speaker or writer would not naturally use in that context.
- Adjust word order, particles, transitions, and sentence boundaries according to the relationship between ideas.
- Prefer direct statements when the point is clear; retain nuance where it matters.
- Allow restrained conversational phrasing only when the genre and audience permit it.
- Do not add filler words, fake hesitation, internet slang, or intentional grammatical mistakes as a substitute for natural expression.

### 7. Nuwa-style profile — consistent author voice

Use when the user wants repeated writing to reflect their own established style.

Build a lightweight style profile only from writing samples the user authored or explicitly authorized. Record:
- Language and level of formality.
- Typical sentence length and paragraph density.
- Preferred terminology and recurring phrase choices.
- Use of active/passive voice and first-person statements.
- How the author introduces a problem, presents evidence, qualifies claims, and reaches conclusions.
- Preferred balance between directness, explanation, and narrative detail.
- Phrases, rhetorical habits, or formatting patterns the author wants to avoid.

Apply the profile as a guide, not a rigid template. Update it when the user gives new examples or corrections. Do not imitate another person's distinctive style without permission, and do not copy source sentences.

### 8. Writing-agent — end-to-end writing workflow

Use when the task includes more than polishing an isolated paragraph.

1. Clarify the purpose, audience, genre, language, and intended outcome from the available context.
2. Identify the central argument or information the document must deliver.
3. Check the outline and section order before sentence-level editing.
4. Draft or revise using the appropriate modules above.
5. Check factual support, terminology, internal consistency, and evidence strength.
6. Remove unnecessary repetition and improve transitions.
7. Proofread formatting, headings, captions, tables, and references where relevant.
8. Return the requested deliverable and flag unresolved questions for the author.

Do not add research, citations, or claims that the user did not request and that cannot be verified.

### 9. De-AI Prompt Enhancer — turn vague style requests into precise instructions

Use when a user says only “make it less AI-like” or wants a reusable editing prompt.

Translate the request into explicit constraints:
- Target language and genre.
- Intended audience and level of formality.
- Main AI-like symptoms to address.
- Desired voice and any authorized style sample.
- Facts, terminology, quotations, references, and conclusions that must remain unchanged.
- Whether structural editing is allowed.
- Required output format (clean copy, tracked changes, side-by-side comparison, or diagnosis).

Never interpret “less AI-like” as “evade AI detection”. If the request is underspecified but the text and genre are clear, make a conservative edit rather than delaying with a long questionnaire.

## Diagnostic taxonomy

Before editing, classify the actual issues. A text may have more than one.

| Symptom | Typical signs | Preferred response |
| --- | --- | --- |
| Boilerplate | Generic openings, transitions, and conclusions | Delete or replace with the actual point |
| Inflated language | Grand claims, abstract praise, unsupported significance | Reduce to evidence-supported wording |
| Mechanical parallelism | Repeated triads, mirrored clauses, fixed rhetorical patterns | Keep only parallelism that improves logic |
| Over-summary | Repeated “in summary” statements and recap paragraphs | Retain one useful synthesis |
| Uniform rhythm | Similar sentence lengths and paragraph structures throughout | Reorganize according to content, not a quota |
| Translation-like prose | Unnatural collocations, word order, or literal idioms | Rewrite idiomatically in the target language |
| Abstractness | Many nouns but few actors, actions, or concrete details | Restore specific subjects and verbs |
| False depth | Rhetorical questions or philosophical claims without reasoning | State the real argument and its evidence |
| Fragmented formatting | One sentence per paragraph without a communicative reason | Group related ideas; preserve intentional emphasis |

Do not treat any phrase or formatting pattern as proof that a text was generated by AI. These are editorial signals, not authorship tests.

## Standard workflow

### Step 1 — Understand and protect the source

Identify the document type, language, audience, purpose, requested degree of intervention, and any non-negotiable content. Treat the supplied text and supporting materials as the source of truth.

For research writing, protect:
- Species, cultivar, gene and protein identifiers, tissue, developmental stage, treatment, and experimental conditions.
- Numerical values, units, sample sizes, replicates, statistical tests, P values, thresholds, and effect directions.
- Citation identity and citation-to-claim relationships.
- Distinctions among observation, association, prediction, mechanism, and experimental validation.

### Step 2 — Diagnose before rewriting

Provide a short diagnosis of the most important problems. Prioritize issues that affect meaning, structure, or reader comprehension over superficial word choice.

### Step 3 — Select modules

Choose the smallest useful combination from the nine modules. For example:
- Chinese research discussion: Humanizer-zh + Stop-slop + Nuwa-style profile, with scientific safeguards.
- English abstract: Humanizer + academic fact-preservation checks.
- Chinese public-account article: AI-flavor-remover + Shorenhua + Stop-slop.
- Product landing page: Taste + Stop-slop.
- Repeated author-specific work: Nuwa-style profile + the relevant language module.
- A vague “make this less AI-like” request: De-AI Prompt Enhancer, then the appropriate editing module.

### Step 4 — Edit in the right order

1. **Structure:** Remove redundant sections, repair the argument order, and give each paragraph a clear job.
2. **Reasoning:** Make claims, evidence, explanations, and limitations explicit.
3. **Sentences:** Repair awkward syntax, repetitive openings, and unnatural transitions.
4. **Words:** Replace vague or inflated wording with precise language.
5. **Rhythm:** Adjust sentence and paragraph boundaries only where they improve reading.
6. **Consistency:** Check terminology, tone, names, tense, and formatting.

Do not start with synonym replacement. Do not add artificial variation merely to make the text appear less regular.

### Step 5 — Verify the revision

Compare the revised text with the source. Confirm that:
- No fact, number, unit, citation, quotation, or named entity has changed without authorization.
- No new experience, observation, result, mechanism, or source has been invented.
- The author's original position and level of certainty remain intact.
- No claim has become stronger than its evidence.
- The revision has improved clarity or specificity, rather than merely changing wording.
- The text still fits its genre and audience.

For academic writing, also follow the repository's AI-assisted Academic Editing and Reference Verification standards.

### Step 6 — Deliver transparently

Default output for a substantial editing task:
1. **Diagnosis:** A concise explanation of the main issues.
2. **Revised text:** A clean, usable version.
3. **Key changes:** Only the meaningful structural or stylistic changes.
4. **Integrity note:** Confirm what factual elements were preserved and list anything that needs author confirmation.

If the user asks for only the revised text, provide only that text. Do not append an unsolicited lecture or generic AI disclaimer.

## Language- and genre-specific guidance

### Chinese academic writing

- Prefer exact descriptions of the study, method, result, and limitation.
- Avoid unsupported claims such as “填补空白”, “具有重大意义”, or “揭示全新机制”.
- Preserve cautious scientific language such as “提示”, “可能”, “与……相关”, and “在本研究条件下”.
- Do not make a Results section sound like a promotional abstract.
- Keep Methods reproducible and technically precise; naturalness must not remove parameters or procedural details.
- Keep Discussion interpretation separate from observed results and literature evidence.

### English academic writing

- Prefer idiomatic scientific English over literal translation.
- Avoid repetitive sentence starters such as “Furthermore”, “Moreover”, and “Importantly” when the logical relationship is already clear.
- Use “novel”, “significant”, “crucial”, and “first” only when justified.
- Preserve technical terms, statistical language, and the distinction between association and causation.
- Do not simplify away necessary qualifiers or methodological details.

### Public-facing and professional writing

- State the point early.
- Use concrete examples only when they are supplied or verifiable.
- Keep a natural rhythm without forced jokes, slang, dramatic hooks, or manufactured personal stories.
- End when the argument is complete; do not add a generic inspirational summary.

### Product and UI copy

- Make each string serve one purpose: identify, explain, guide, or prompt an action.
- Use consistent terminology across the interface.
- Avoid vague claims and feature promises that are not supported by the product.
- Prefer concise, scannable language, but do not remove information users need to make a decision.

## Reusable prompts

### Chinese naturalization

请先判断这段文字具体有哪些表达问题，再进行必要修改。目标是让中文自然、准确、有信息密度，避免空泛套话、机械排比、过度总结、假大空和直译式语序。保留原文事实、数据、术语、引用、观点和结论强度，不添加个人经历或未经证实的细节。不要为了改变 AI 检测结果而改写。若原文已经自然，不要为了修改而修改。

### English naturalization

Edit the text into clear, idiomatic English for its intended audience. Diagnose and fix literal translation, awkward collocations, repetitive transitions, inflated claims, and unnecessary nominalizations. Preserve the author's meaning, evidence, terminology, citations, and degree of certainty. Do not add facts or personal experiences, and do not optimize for AI-detection outcomes. Leave effective sentences unchanged.

### Whole-document audit

Review the entire document before rewriting. Identify structural repetition, generic claims, formulaic paragraph patterns, overlong introductions, repeated conclusions, weak evidence-to-claim links, and inconsistent voice. Rank the issues by importance and propose a focused revision plan. Do not rewrite sections that are already clear and effective.

### Author-voice profile

Using only the writing samples I authored or authorized, summarize my recurring language, terminology, sentence and paragraph patterns, level of formality, argument structure, and preferred degree of directness. Separate stable preferences from patterns that may be accidental. Do not copy sentences. Use this profile as a flexible guide for future editing.

### Product-copy refinement

Revise this product or interface copy for clarity, specificity, consistency, and usability. Preserve verified product capabilities and constraints. Remove generic marketing language and unsupported superlatives. Make the value and next action clear without adding promises or changing product behavior.

## Final quality checklist

- [ ] The main point is clear and appears where readers need it.
- [ ] Every paragraph contributes a distinct idea, piece of evidence, or necessary transition.
- [ ] Generic filler and repeated summaries have been removed where they add no value.
- [ ] Parallelism, rhetorical questions, and short paragraphs are used intentionally rather than mechanically.
- [ ] Chinese reads naturally or English reads idiomatically for the intended genre.
- [ ] The author's genuine position and voice have not been replaced by a generic style.
- [ ] No facts, data, citations, quotations, personal experiences, or capabilities have been invented.
- [ ] Evidence strength, limitations, and uncertainty remain accurate.
- [ ] Terminology and formatting are consistent.
- [ ] The revision improves the writing itself and is not intended to evade AI detection.

## Relationship to other repository standards

- For formal research manuscripts, also apply [AI-assisted Academic Editing](../ai-assisted-academic-editing.md).
- For citation authenticity and claim support, apply [Reference Verification](../reference-verification.md).
- For final artifact and metadata hygiene, apply [AI-assisted Artifact Hygiene](../../principles/ai-assisted-artifact-hygiene.md).

**Core principle: remove empty patterns, not the author's personality; improve expression, not the underlying evidence.**

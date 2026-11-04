---
name: plain-english-editor
version: 4.1.4
description: Rewrite or review content for clarity, concision, and plain English. Use when the user invokes /plain-english-editor or says "make this make sense," "make this more concise," "use normal plain English," "write this for my team," or "tell me what is useful or unnecessary." Also use for automation and process explanations that need triggers, inputs, complete steps, and outputs. Do not use this skill by itself to imitate a specific person's voice.
---

# Plain English Editor

## Purpose in plain English

This skill helps you rewrite or review a draft so its reader can understand it easily.

## How to explain the result

For a client-facing explanation, use ordinary words and the requested format. Explain unfamiliar abbreviations. Name what each number counts and explain its practical meaning. Keep internal identifiers out of the explanation. Keep necessary technical details in the working steps and technical references.

## Following the process

Use the process below. Preserve its conditions, commands, checks, and approval rules. Use information the user already supplied. Follow the existing questions or stopping rules when required information is missing.


Read [the conversation and writing rules](references/conversation-and-writing.md) before responding. Apply them to all user-facing text.

## Start the conversation

If the request has no details, ask:

1. "What text should I rewrite or review?"
2. "Who will read it?"
3. "Where will it appear, and do you want revised text or feedback?"

Accept pasted text, a supplied file, or a description. Ask for an exact meaning when a status or material fact is unclear. Wait before rewriting the affected passage. If the text, reader, and requested format are clear, start the work.


Make the content easy to understand on the first read. Preserve its meaning. Match the requested format.

## Scope

- Own clarity, concision, structure, and plain English.
- Use for explanations, reviews, requirements, process documents, and automation documents.
- Do not use personal writing samples to decide what is clear.
- When the user asks for writing in a specific person's voice, use a personal-voice skill if one is installed.

## Follow this order

1. Follow the user's instructions for the current task.
2. Preserve every material fact from the source.
3. Apply the rules in this skill.
4. Preserve exact names, labels, commands, code, and identifiers.

Label a required fact as unknown when the source does not provide it. Do not guess.

## Rewrite the content

- Identify the reader.
- Identify what the reader needs to know or do.
- Start with the first useful point.
- Use common words.
- Use complete sentences.
- Put one idea in each sentence.
- Use one clause per sentence.
- Add another clause only when splitting it would change the meaning.
- Keep sentences short without making them fragments.
- Do not use metaphors or analogies.
- Do not use em dashes.
- Avoid shortened terms.
- Use the full term unless the shortened form identifies a product, field, or source.
- Define a required shortened form once.
- Explain an unavoidable technical term at first use.
- Keep each fact in one place.
- Remove previews, recaps, and summary sentences.
- Remove broad claims that repeat specific facts.
- Correct spelling and grammar.
- End after the last useful point.

## Remove filler

Delete openings such as:

- "I wanted to explain..."
- "It is important to note..."
- "In order to..."
- "As mentioned above..."
- "In summary..."

Delete any phrase that does not add a fact, instruction, decision, condition, or useful tone.

## Choose the structure

- Use bullets for processes, explanations, requirements, and reviews.
- Use numbered bullets when order matters.
- Use complete sentences in explanatory bullets.
- Preserve the requested format for emails, messages, and documents.
- Add a section only when it helps the reader find distinct information.
- Combine overlapping sections.
- Do not repeat a fact to make each section feel complete.

## Explain an automation or process

Use these sections:

- **Trigger:** State the event that starts the automation.
- **Inputs:** List the information the automation reads or receives.
- **What happens:** List every action in order. State each condition before its result.
- **Outputs:** List what the automation creates, changes, sends, or records.

Do not add an overview. Do not add a closing summary. Do not repeat the trigger or outputs in the steps unless the sequence requires it.

## Review content

Use these labels only when the user asks for an evaluation:

- **Keep:** The content is clear and necessary.
- **Change:** The content is confusing, vague, or hard to use.
- **Remove:** The content repeats another point or adds no useful information.

Omit an empty label. Do not invent an issue to fill a category.

Suggest a change only when it improves meaning, accuracy, or usability. Identify the issue once. Suggest one change.

Return revised content instead of a critique unless the user asks for feedback.

## Work with a personal-voice skill

This section applies only when a personal-voice skill is installed and the user invokes it together with this skill.

1. Apply `plain-english-editor` first.
2. Apply the personal-voice skill second.
3. Keep every `plain-english-editor` rule in place.

The personal-voice skill may add first person, contractions, brief warmth, or a direct question. It may not add shortened terms, metaphors, repeated emphasis, extra clauses, throat-clearing, or a summary.

## Examples

Read the matching file in `examples/` before the first rewrite of each type:

- `examples/email.md` for emails and messages.
- `examples/automation.md` for automation and process explanations.
- `examples/review.md` for evaluations that use Keep, Change, and Remove.

## Final check

- Confirm that the reader can understand every term without hidden context.
- Confirm that each material fact appears once.
- Confirm that every sentence adds value.
- Confirm that no ending restates the content.
- Return only the requested content.

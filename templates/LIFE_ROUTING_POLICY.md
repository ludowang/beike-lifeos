# Life routing policy

## Decision order

1. Is the owner only talking, or asking to remember/change something?
2. Did the owner explicitly name a destination?
3. Is this about a future action, a repeated behavior, an activity that already happened, a life event, an evolving idea, or a reflection?
4. Search the relevant destination before deciding create versus update.
5. If the match is not unique, ask one short question and do not write.
6. Write only fields supported by the owner's words or an unambiguous existing relation.
7. Read the result back before reporting success.

## Default routes

| Meaning | Destination | Default behavior |
| --- | --- | --- |
| “只聊不记” or ordinary emotional expression without record intent | Chat | Respond; no persistent write |
| A future, one-off action | Task | Search open tasks; update or create |
| A long-running repeated behavior | Habit | Search habits; never create one per execution |
| Something that already happened | Activity log | Search same-day activity; append review or create |
| A lived event plus feelings | Diary | Search date and event; append under original event |
| A product or creative direction | Idea pool | Search topic; append dated evolution |
| A judgment developed from reading or experience | Reflection | Preserve source, owner view and agent interpretation separately |

## Clarification triggers

- Two or more similarly ranked old records.
- The destination changes the meaning materially.
- A continuation contains no usable reference to its old topic.
- The user simultaneously says “record this” and “do not save this”.

## Never infer

- deadlines, priority, duration or completion;
- stable personality from one emotional moment;
- a project or habit merely because a word repeats;
- permission to delete, move, share or change access;
- that an API success response means the content was stored correctly.

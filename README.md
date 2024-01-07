# Story Augmentation Generation (SAGE)

This attempts to implement something like "GROVE: A Retrieval-augmented Complex Story Generation Framework with A Forest of Evidence". 

Rough plan:

- Lore building
- Plan out a story
- Prompt generation with RAG
- Summarise and align with story board/plan

Inspiration: "Belonging outside Belonging" games can be used for story crafting in a structured way. We will use inspiration from GROVE to enable this

## Lore Building

We will start by using prompts to generate the following:

* World and its Seasons/events
* Characters
* NPCs and traits
* Natures and Places

We will use inspiration from https://possumcreekgames.itch.io/wanderhome-playkit as the root for the generation

The basic structure of these items will be used as part of the RAG retrieval it would look like this:

```
Entity

- item1
- item2
- item3
- ...

```

From a backend perspective, it may be more structured, where we have the description of the trait or attribute and metadata surrounding
the short description, or tag information for the purpose of retrieval (maybe). 

```json
{
    "tag": "short-tag",
    "description": "long description",
    "prompt": "...",
}
```


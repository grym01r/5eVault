---
PromptInfo:
 promptId: GenNPC
 name: 🎲 Generate NPC 🛡️
 description: Generate a fantasy store that sells armor. 
 author: JoshP
 tags: fantasy, ttrpg
 version: 0.0.1
---

{{#if selection}}
Use this Information for flavoring the Prompt:
*Main Focus*
{{title}} ({{type}}:
{{#each sum}}
- {{this}}
{{/each}}
{{selection}}
*Less important things, but maybe helpful in Context*:
{{#each children}}
{{#if frontmatter.sum}}
{{this.basename}}:
{{#each frontmatter.sum}}
- {{this}}
{{/each}}
{{/if}}
{{/each}}
Use the above information JUST FOR CONTEXT. Come up with new Ideas inspired by the things above, but do not just iterate things from above
{{/if}}


# Prompt: NPC Name
Prompt: Generate a unique name for a character in a Dungeons & Dragons game

# Prompt: Race
Prompt: Choose a race for the character from the tradtional races in Dungeons & Dragons

# Prompt: Quirk
Prompt: Make the NPC feel like someone the party might actually remember

# Prompt: Secret
Prompt: What is a grounded and story-driven secret this character is concealing?

# Prompt: Hook
Prompt: Make the NPC feel like an adventure seed that is creative

# Prompt: Voice
Prompt: Give inspiration for a Dungeon Master in how this character speaks and what kind of voice to use
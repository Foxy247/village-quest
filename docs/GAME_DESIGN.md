# Village Quest - Game Design

## Purpose

This document describes Village Quest as a game.

It defines the basic player experience, game world, core systems, and important game rules.

It does not define the technical implementation.

Technical decisions belong in `ARCHITECTURE.md`.

---

# Game Concept

Village Quest is a small browser-based low-fantasy role-playing game set around a medieval village and its surrounding wilderness.

The player begins as an inexperienced, weak, and largely unimportant villager.

At first, the player helps the inhabitants with simple problems, explores nearby locations, gathers resources, and learns how the village works.

Through these small adventures, the character gradually becomes more capable, better equipped, and more important to the community.

Over time, larger problems begin to appear outside the village.

The exact long-term threat is intentionally not defined yet.

The game should begin small and expand gradually.

---

# Setting

Village Quest uses a low-fantasy setting.

The world should feel mostly grounded and believable.

Typical early elements include:

* villagers
* craftsmen
* farmers
* traders
* forests
* mines
* wild animals
* bandits
* damaged roads
* shortages
* local conflicts

Magic and supernatural elements may exist, but they should initially be rare, mysterious, or unusual.

The game should not begin with powerful magic, world-ending threats, or large numbers of fantastic creatures.

Ordinary problems may later reveal deeper or supernatural causes.

---

# Player Fantasy

The player should feel like someone who starts with very little knowledge, equipment, power, and influence.

The character is not a chosen hero at the beginning.

Progress comes through experience and actions.

The character becomes more capable by:

* completing quests
* helping villagers
* discovering new locations
* collecting resources
* defeating enemies
* acquiring useful items
* earning experience
* improving equipment
* unlocking new opportunities

The player should gradually move from ordinary villager to capable adventurer and important member of the community.

---

# Game Structure

Village Quest combines two forms of progression:

## Character Progression

This is the main focus during early development.

The player:

* explores
* completes quests
* gathers resources
* fights enemies
* earns rewards
* gains experience
* improves equipment
* unlocks new locations

## Village Progression

Village development is initially a secondary system.

The village changes because of actions and quests completed by the character.

Examples:

* repairing a bridge unlocks a new route
* helping the blacksmith improves available equipment
* clearing a trade route allows merchants to return
* solving local problems unlocks new NPCs or quests

Village development should initially happen through meaningful quest consequences.

Do not begin with a complex city-building simulation.

Systems such as:

* population management
* production chains
* worker assignment
* taxes
* resource production per hour
* complex building upgrades

are outside the initial scope.

---

# Core Progression Relationship

Character progression and village progression should support each other.

Character becomes stronger

-> completes more difficult quests

-> village improves

-> new opportunities become available

-> character can progress further

This relationship is an important long-term design principle.

---

# Core Gameplay Loop

The general gameplay loop is:

1. Explore the village.
2. Talk to inhabitants or discover a task.
3. Accept a quest.
4. Travel to another location.
5. Perform actions such as gathering, exploring, or fighting.
6. Collect items or complete objectives.
7. Return to the quest giver.
8. Complete the quest.
9. Receive a reward.
10. Improve the character or unlock new content.
11. Observe changes in the village or world.

Then the loop begins again with more possibilities.

---

# Character

The player controls one character.

The first version of the character may contain:

* name
* health
* maximum health
* energy
* maximum energy
* experience
* level
* gold
* current location

Not every value has to exist from the beginning of development.

New character systems should only be introduced when they are needed by the game.

---

# World

The game begins in and around one small village.

The world should expand gradually instead of being designed as a large open world from the beginning.

Possible early locations include:

## Village Square

The central location of the village.

Possible purposes:

* meeting villagers
* discovering quests
* travelling to other village locations

## Tavern

A social location.

Possible purposes:

* meeting NPCs
* hearing rumours
* discovering quests

## Blacksmith

A place connected to equipment and resources.

Possible purposes:

* quests
* buying or selling items
* equipment later in development

## Forest

One of the first wilderness locations.

Possible activities:

* gathering wood
* gathering herbs
* exploration
* encountering enemies later

## Old Mine

A more dangerous location that can be unlocked later.

Possible activities:

* gathering ore
* exploration
* combat

These locations are starting ideas and may change as the game develops.

---

# Travel

The player can move between locations.

Locations should be connected logically.

The player should not automatically be able to travel from every location to every other location.

Travel may eventually:

* consume energy
* require an unlocked route
* require completion of a quest
* lead to encounters

The first version of travel should remain simple.

---

# Energy and Actions

The character may have a limited amount of energy.

Certain actions can consume energy.

Examples:

* travelling
* gathering resources
* exploring

Energy creates a simple resource-management decision:

"Which actions should I perform with the energy I currently have?"

The exact regeneration system is not defined yet.

---

# Items

The game contains items that the player can own.

Possible categories include:

## Resources

Examples:

* wood
* herbs
* iron ore

Resources can be required for quests or other systems.

## Consumables

Examples:

* healing potion

Consumables disappear or decrease when used.

## Equipment

Examples:

* sword
* leather armour

Equipment may influence character abilities later.

## Quest Items

Special items that exist mainly for quest objectives.

The first inventory system does not need all item categories immediately.

---

# Inventory

The inventory represents the items currently owned by the character.

The player should eventually be able to:

* view owned items
* receive items
* lose or use items
* use resources for quests
* buy and sell selected items

Equipment can be added later.

---

# Quests

Quests are one of the main ways the player interacts with the world.

A quest should normally have:

* title
* description
* objective
* progress
* status
* reward

Possible quest states:

* available
* active
* completed

More states should only be introduced if they become necessary.

Quests should often create visible consequences in the world or village.

---

# First Quest

## Wood for the Village

After a difficult winter, parts of the village need repair.

A villager needs wood for one of these repairs.

The player must travel to the nearby forest and gather wood.

Initial objective:

Collect 5 Wood.

Possible reward:

* gold
* experience

The exact reward values are not final.

This quest introduces the basic structure:

Village

-> Quest

-> Travel

-> Action

-> Resource

-> Inventory

-> Quest Progress

-> Reward

-> Village Change

---

# First Village Change

The wood collected during the first quest contributes to repairing an old wooden bridge near the village.

Before the repair, the route beyond the bridge is inaccessible.

After the repair, the bridge can later unlock access to another location or region.

This introduces an important design rule:

Player actions can permanently change the world.

The exact location beyond the bridge does not need to be defined yet.

---

# First Playable Gameplay Loop

The first complete playable loop should allow the player to:

1. Create a character.
2. Enter the village.
3. Discover the quest `Wood for the Village`.
4. Accept the quest.
5. Travel to the forest.
6. Gather wood.
7. Spend energy while gathering or travelling.
8. View the collected wood in the inventory.
9. Return to the village.
10. Complete the quest.
11. Receive a reward.
12. Trigger the first visible village improvement.

This is the first major gameplay target.

---

# Gathering

Some locations allow the player to gather resources.

Example:

Forest:

* gather wood
* gather herbs

Mine:

* gather iron ore

Gathering may:

* consume energy
* produce one or more resources
* contribute to quests

The first version should behave predictably.

Randomness can be introduced later if it improves the game.

---

# Combat

Combat is not required for the first complete gameplay loop.

It should be introduced after travel, gathering, inventory, and the first quest already work.

Combat should begin as a simple turn-based system.

Possible player actions:

* attack
* use an item
* flee

An enemy may have:

* name
* health
* attack power
* reward
* possible loot

The first combat system should contain only the rules necessary for one complete encounter.

Complex systems such as:

* elemental damage
* critical hit systems
* skill trees
* status effects
* advanced enemy AI

are outside the initial scope.

---

# Trading

The player may eventually buy and sell items.

A merchant can offer selected items for a price.

Basic rules:

* the player cannot buy something without enough gold
* the player cannot sell something they do not own
* gold and inventory changes must happen together

A complex economy is not required.

---

# Character Progression

The player can eventually earn experience and increase their level.

Possible rewards for progression include:

* more health
* more energy
* access to new locations
* access to harder quests
* better equipment

The exact progression formula is not defined yet.

It should only be designed when the basic gameplay loop already works.

---

# Early Story Direction

The village has recently experienced a difficult period, such as a harsh winter.

Parts of the settlement and surrounding infrastructure are damaged.

Supplies may be limited and villagers need help with ordinary problems.

The player begins by assisting with these small issues.

Over time, the player may discover that some problems cannot be explained by ordinary circumstances alone.

The exact cause is intentionally left open for later design.

---

# Game Rules

Important general rules:

1. The player can only perform actions that are currently allowed.
2. Resources cannot be used if the character does not own them.
3. Gold cannot be spent if the character does not have enough.
4. A quest reward should not be received repeatedly for the same completion.
5. Travel must follow valid location connections.
6. Character values should remain within valid limits.
7. Game progress should result from player actions, not from directly changing values.
8. Some quests may permanently change the village or world.
9. New locations or opportunities may depend on previous player actions.

Additional rules should be added only when new systems require them.

---

# Out of Scope for Now

Do not prioritize:

* multiplayer
* guilds
* large open worlds
* complex crafting
* advanced professions
* skill trees
* complex magic systems
* city-building simulation
* production chains
* worker management
* procedural world generation
* dynamic economies
* advanced enemy AI
* dozens of locations
* large numbers of quests

These ideas may be reconsidered after the core game works.

---

# Design Principles

## Start Small

Prefer a small system that works and is understandable over a large system with unnecessary complexity.

## Character First

Early development focuses primarily on the player character and adventure gameplay.

Village development grows around the character's actions later.

## Meaningful Consequences

Important quests should eventually have visible effects on the village or game world.

## Grounded Fantasy

Begin with ordinary and believable problems.

Introduce unusual or supernatural elements gradually.

## Complexity Must Earn Its Place

Every new mechanic should answer at least one of these questions:

* Does it make the game more interesting?
* Does it support another important game system?
* Does it provide a useful programming learning opportunity?

If none of these apply, the mechanic probably does not belong in the game yet.

---

# Open Design Questions

The following decisions are intentionally not fixed yet:

* final village name
* exact long-term threat
* character classes or professions
* exact energy regeneration
* exact experience and level formulas
* inventory limits
* combat damage formulas
* death and defeat consequences
* equipment system
* crafting system
* exact village development mechanics

These decisions should be made when they become relevant to development.

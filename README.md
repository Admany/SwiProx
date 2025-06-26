# SwiProx - Switch Proximity Chat Mod

**ALL RIGHTS RESERVED**

> **Welcome!** SwiProx is free for everyone to use on their servers and in modpacks. You are encouraged to make addons, request ports, and join the community! Please read the rights and extension policy below for details.

---

## What is SwiProx?
SwiProx is a modern, feature-rich proximity chat mod for Minecraft Forge 1.20.1+ that brings immersive, realistic text chat to your server. It supports:
- Proximity-based chat (local, whisper, yell, global)
- Cave echo, wind, and underwater effects
- Anti-spam, cooldowns, and message distortion
- Full compatibility with custom worldgen/terrain mods (Terralith, Tectonic, Biomes O' Plenty, etc.)
- Easy extensibility for modpack authors and addon devs

---

## Commands
- `/swiprox proxy` - Switch to local (proximity) chat (50 blocks)
- `/swiprox global` - Switch to global chat (all players)
- `/swiprox default <proxy|global>` - Set default chat mode for the world
- `/swiprox whisper <message>`- Send a whisper (10 blocks, with cooldown)
- `/swiprox yell <message>` - Yell a message (100 blocks, with cooldown)
- `/swiprox reload` - Reload config (OP only)

---

### OP-Only Global Chat Lock Commands
- `/swiprox global lock` - Lock global chat. Only ops and allow-list can use global chat; others are forced to proxy mode.
- `/swiprox global lock add <name>` - Add a player to the allow-list for global chat while locked.
- `/swiprox global lock remove <name>` - Remove a player from the allow-list. If online, they are switched to proxy mode.
- `/swiprox global lock unlock` - Unlock global chat for everyone.

> **Note:** The above lock commands require OP (permission level 2+) in-game. If you are opped, you will see and be able to use these commands. These commands let you control who can use global chat when it is locked, and enforce chat mode changes instantly for affected players.

---

## Config Options (in `SwiProxConfig`)
- `whisperRadius` - How far whispers travel (default: 10)
- `yellRadius` - How far yells travel (default: 100)
- `maxProximityDistance`- Max range for local chat
- `yellCooldownSeconds` - Cooldown for yells (default: 10s)
- `caveEchoEnabled` — Enable/disable cave echo effects
- `caveEchoLargeRepeat` / `caveEchoSmallRepeat` — Echo repeat count for caves
- `underwaterEnabled` - Enable/disable underwater chat distortion
- `windEffectStartY` / `windEffectMaxY` — Y-levels for wind effects
- `distortion70CharReplaceChance`, `distortion70WordDropChance`, `distortion70UnderscoreChance` - Message distortion tuning
- ...and more! See the config file for all options.

---

## Addons & Ports
- **SwiProx Blocks Addon** - Adds support for custom cave/stone blocks via runtime registration (see below)
- Want a port to another platform? Open an issue or PR! I am happy to help with ports to Fabric, NeoForge, or other loaders.

### How to Add Custom Cave Blocks (for modders)
- Call `EnvironmentAnalyzer.addExtraCaveBlock("modid:block_id")` from your mod, mixin, or datapack loader.
- Example: `EnvironmentAnalyzer.addExtraCaveBlock("mycoolmod:glowstone_cave");`
- No code edits needed. Works at runtime!

---

## Rights & Extension Policy
**ALL RIGHTS RESERVED**

- **You are free to use SwiProx on your server, in your modpack, or for personal play.**
- **You may make and publish addons or extensions for SwiProx.**
- **You may request or contribute ports to other platforms/loaders.**
- **You may NOT republish, redistribute, or rehost the core SwiProx mod file anywhere else.**
- **You may NOT modify and publish the core SwiProx mod, in whole or in part, under any name.**
- Addons and ports are welcome, but the original mod must remain unmodified and only downloadable from the official source.
- If you want to collaborate, make a port, or have questions, please open an issue or contact me!

**Summary:**
- ✅ Use SwiProx freely
- ✅ Make and share addons
- ✅ Request or help with ports
- ❌ Do NOT republish or rehost the mod
- ❌ Do NOT modify and publish the mod (especially not under a different name)

---

## Credits
- Mod by Admany
- Special thanks to everyone who helps test, suggest features, or spread the word!

---

## Community & Support
- **Questions, suggestions, or need help?** Open an issue or join the discussion on GitHub!
- **Want to contribute?** PRs for addons, ports, or documentation are welcome (see rights above).
- **Enjoy the mod?** Please credit and link to the official page so others can find the latest version!

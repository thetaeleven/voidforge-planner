# 🔮 Nebulous Voidforge Planner

A fan-made planning tool for **World of Warcraft: Midnight Season 1** to help you decide where to spend your **Nebulous Voidcore** bonus rolls.

**Live site:** [thetaeleven.github.io/your-repo-name](https://thetaeleven.github.io)

---

## What is this?

In WoW Midnight Season 1, players earn **Nebulous Voidcores** — a currency used to purchase bonus rolls on loot from raids, Mythic+ dungeons, Bountiful Delves, and Nightmare Prey Hunts. Each roll costs cores (2 for raid bosses, 1 for everything else), and you can only roll on each source once per season.

This planner helps you:
- See exactly which items can drop for your class and spec
- Track what you've already rolled on this season
- Banish items you don't want so they don't skew recommendations
- Get ranked recommendations on where to spend your next core based on potential upgrades

---

## How to use it

### Step 1 — Your Character
Select your class and then your spec. The entire loot system filters based on your selection — weapons, trinkets, and armor are all filtered to only show items your spec can actually equip and roll on.

### Step 2 — Current Gear
Set the **gear track** for each of your 16 equipment slots using the dropdowns:
- **None** — slot is empty or the item is Adventure track or lower
- **Veteran / Champion / Hero / Myth** — the track of gear you currently have equipped

For Head, Shoulder, Chest, Hands, and Legs slots there is also a **Tier** checkbox — tick this if you already have a tier set piece in that slot so tier token drops are excluded from recommendations.

### Step 3 — Select Activities & Track Rolls
Choose all the content you have access to this season across three tabs:

- **Raid** — Select difficulty (Normal/Heroic/Mythic) then pick individual bosses across Voidspire, Dreamrift, and March of Quel'Danas
- **Mythic+** — Select key bracket (Mythic 0 / +2–9 / +10+) then pick individual dungeons
- **Bountiful Delve** — Coming soon
- **Prey Hunt** — Coming soon

Each selected activity shows a collapsible loot pool filtered for your spec. Within each pool you can:
- Click **✓** to mark an item as already rolled on this season (excluded from recommendations)
- Click **🚫** to banish an item you don't want (permanently excluded from recommendations regardless of upgrades)

Both actions can be undone by clicking the same button again.

### Step 4 — Recommendations
The planner ranks your selected activities by upgrade potential and shows your top 5. Each recommendation card shows how many possible upgrades are available and the loot track. Click any card to expand its loot table and see exactly which items are potential upgrades for your current gear.

Scoring weights:
- Higher track loot scores higher (Myth > Hero > Champion > Veteran)
- Trinkets are weighted more heavily since they are harder to obtain
- Rolled and banished items are excluded from scoring

---

## Loot data sources

| Content | Status |
|---|---|
| Voidspire (6 bosses) | ✅ Full loot tables from Wowhead |
| Dreamrift — Chimaerus | ✅ Full loot tables from Wowhead |
| March of Quel'Danas (2 bosses) | ✅ Full loot tables from Wowhead |
| Mythic+ (8 dungeons) | ✅ Full loot tables from Wowhead |
| Bountiful Delve | 🔜 Coming soon |
| Nightmare Prey Hunt | 🔜 Coming soon |

---

## Filtering system

### Weapons
Each weapon is filtered by three criteria:
1. **Primary stat** — must match your spec's primary stat (Strength, Agility, or Intellect)
2. **Weapon type** — must be a weapon type your spec can equip (e.g. Arms Warrior only sees 2H weapons, Frost DK sees both 1H and 2H)
3. **Class/spec restrictions** — some weapons are restricted to specific specs (e.g. Belo'ren's Swift Talon is Assassination/Subtlety Rogue only)

### Trinkets
Trinkets are categorised by type and filtered to the appropriate specs:
- **Universal** — all specs (e.g. Locus-Walker's Ribbon, Gaze of the Alnseer)
- **Physical DPS + Tanks** — Strength and Agility specs
- **Tank only** — tank specs only
- **Healer only** — healer specs only
- **Intellect DPS** — caster DPS and healer specs
- **Agility/Intellect** — Agility and Intellect specs (not pure Strength)
- **Strength only** — Strength specs only
- **Per-spec** — explicitly defined spec lists for specific trinkets

### Armor
Filtered by your class armor type (Cloth, Leather, Mail, Plate). Accessories (neck, ring, back, trinket) and weapons are available to all armor types subject to the above rules.

---

## Technical details

- Single-file HTML/CSS/JS — no frameworks, no dependencies, no build step
- Session-only state — rolled and banished items reset when you close the page (persistence coming in a future update)
- All filtering logic runs client-side in the browser

---

## Credits

Created by **Xarielle-Proudmoore**

Loot data sourced from [Wowhead](https://www.wowhead.com)

*This is a fan-made tool and is not affiliated with or endorsed by Blizzard Entertainment. World of Warcraft is a trademark of Blizzard Entertainment, Inc.*

# EFTH Weapon Sway Compatibility

**Hurt arms. Unsteady aim. A reason to patch yourself up.**

A compatibility addon for **S.T.A.L.K.E.R. Anomaly / G.A.M.M.A.** that connects [EFT Health System (EFTH)](https://discord.com/channels/456765861953536020/1248756352881266772) with [Weapon Sway](https://www.moddb.com/mods/stalker-anomaly/addons/weapon-sway). Your arm injuries affect how steadily you can aim, and treatment helps you get back on target.

## What changes in game?

- **Wounds affect your aim.** Small scratches get some leeway; serious injuries make holding a steady sight picture harder.
- **Destroyed and fractured arms carry extra penalties.** Both arms contribute, so injuring both makes things worse.
- **Recovery matters.** Surgery gets an arm working again, but healing and recovering its maximum HP gradually restore your stability.
- **Painkillers offer some relief.** They reduce the extra penalties from destroyed arms and fractures. Wounds and recovery still affect your aim.
- **Changes ease in and out.** Sway adjusts gradually as you take damage or recover.

With healthy arms, Weapon Sway behaves as usual. Its weapon handling, stance, mounting, and breath-holding features still do their job.

## What you need

- **S.T.A.L.K.E.R. Anomaly / G.A.M.M.A.**
- **[EFT Health System](https://discord.com/channels/456765861953536020/1248756352881266772)**
- **[Weapon Sway](https://www.moddb.com/mods/stalker-anomaly/addons/weapon-sway)** — integration targets version 1.11
- **[Mod Configuration Menu (MCM)](https://www.moddb.com/mods/stalker-anomaly/addons/anomaly-mod-configuration-menu)**
- **[Modded X-Ray executable](https://github.com/themrdemonized/xray-monolith)**

## Installation

1. Install the addon through **Mod Organizer 2**.
2. Place it **after EFTH and Weapon Sway** in MO2's left pane so its files win any conflicts.
3. In Weapon Sway's settings, make sure **Enable Weapon Sway** is on. Disable its **BHS integration** when using EFTH as your injury system.
4. Open **MCM → EFTH Weapon Sway**, leave **Enable EFTH integration** on, and choose a preset.

Existing saves need no migration. When upgrading from an older build, revisit MCM: settings from the old health-tier system are no longer used.

## Make it feel right

Start with **Balanced**, then adjust to taste:

| Preset | What to expect |
| --- | --- |
| **Relaxed** | Gentler injury penalties and more painkiller relief. |
| **Balanced** *(default)* | Noticeable consequences for injuries, with room for treatment to help. |
| **Hardcore** | Stronger penalties and less painkiller relief. |
| **Custom** | Set your own damage tolerance, injury penalties, painkiller relief, and sway limit. |

**Overall injury strength** adjusts the added penalty from 0–200% with every preset. **Smooth transitions** controls whether changes ease in and out. Select **Custom** to use the advanced penalty sliders; those sliders do not override a named preset.

For a sense of scale, these are approximate injury multipliers with Balanced at its default strength:

| Arm condition | Injury multiplier |
| --- | --- |
| Both healthy | 1.00× |
| One at half HP, the other healthy | 1.55× |
| Both at half HP | 2.11× |
| One destroyed, the other healthy | 3.25× |
| Both destroyed | 5.50× |

Weapon Sway applies its own final limit, so the visible effect can level off before these multipliers do.

## Troubleshooting

**No added sway when injured?** Check that both mods are installed, Weapon Sway is enabled, and **Enable EFTH integration** is on. Check MO2's conflict winners and disable Weapon Sway's BHS integration.

**Advanced settings seem to do nothing?** Select **Custom** first. If you used an early test build, your saved **Maximum health multiplier** may still be limited to 3.0; raise it to try the expanded range.

**More injury strength makes no visible difference?** Check this addon's **Maximum health multiplier** and Weapon Sway's **Maximum Effect Power**. Either limit can stop sway increasing. A low health multiplier limit can also hide the benefit of painkillers.

**Want to see what the addon is reading?** Open the engine's ImGui overlay and select **Mods → EFTH Weapon Sway Debug**. The read-only window shows arm health, injuries, painkiller status, and the calculated modifiers. Aim to refresh the sway snapshot. The window starts closed whenever you load a game or save.

Turning off **Enable EFTH integration** restores Weapon Sway's normal calculation. The addon also falls back to that calculation if EFTH health data is missing or invalid.

## Credits

- **Dr_Cox1911** — addon development and integration
- **vegeta1k95, Lizzardman, Lasie, Fabio Conte, Joe, Joker Burger, MrShersh** — EFT Health System
- **bvcx** — Weapon Sway
- **ravenascendant** — MCM
- **themrdemonized** — modded X-Ray executable

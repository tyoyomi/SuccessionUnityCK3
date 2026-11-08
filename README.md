# Succession Unity

Crusader Kings III mod. Version 0.1.0. Supported game version 1.20.*.

Canonical working copy: `Documents/Development/CK3 Mods/su`.

## What it does

Opt-in **Dynasty Pact** for the living player dynasty head. On that ruler’s death the player heir chooses **Forced Unity** (reclaim top-tier crowns while compensating siblings), **Soft Glue** (temporary sibling pacification, then optional consolidate for gold / vassalage / tyranny), or **Decline** (vanilla aftermath). The pact expires on death and must be re-enabled each generation.

## Footprint

Additions only. No `replace_path`. No GUI. No defines. No vanilla key overwrites.

| Area | Content |
| --- | --- |
| Decisions | `su_enable_dynasty_pact_decision`, `su_revoke_dynasty_pact_decision` |
| Events | `su_events` 1001 / 1101 / 1201 / 1301 / 1302 / 1401 |
| On-actions (append) | `on_death` → `su_on_death`; `on_game_start` → `su_on_game_start`; `yearly_playable_pulse` → `su_soft_glue_pulse` + `su_pending_choice_pulse` |
| Other | Prefixed modifiers, opinion modifiers, scripted effects/triggers, script values |

## Soft peers

Works alone. Optional future SS detection bonus is not in v0.1.0. Compatible with Exalted Dynasty / Advisor / Faith via append-only `on_death`.

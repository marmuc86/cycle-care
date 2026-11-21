# Cycle Care (first version)

An installable iPhone web app (PWA) for keeping track of your partner's cycle together and getting gentle, practical reminders. No account, no server: all data lives on the phone in the browser's local storage. The code contains no personal data. Your dates are pasted in on first launch.

## Files
- `index.html`: the whole app (HTML, CSS, JS in one file)
- `manifest.webmanifest`, `sw.js`: make it installable and usable offline
- `icon.svg`, `icon-*.png`: home-screen icon

## Installing on iPhone
1. Host the folder on any HTTPS address (e.g. GitHub Pages).
2. Open it in **Safari** → Share → **Add to Home Screen**.
3. Open it from the home screen, enter her name, tick the consent box, tap **Paste my notes**, paste your list and tap Import.
4. **Together** tab → **Add next 3 cycles to Calendar**, then choose a new calendar called "Cycle Care". Calendar sends the notifications.

Updating dates: tap **Period started today** on Today, **＋ Add** in Log, or tap any day in Calendar. Tap an entry to edit or delete it.

## Design standards applied (from 2025–26 Apple Design Award and App Store Award winners)
| Standard (who showed it) | How Cycle Care applies it |
|---|---|
| Effortless onboarding (Moonlitt, ADA 2026 Interaction) | One screen, then paste your existing notes as they are ("18.3. P Tag 1") |
| Data anyone can read at a glance (Tide Guide, ADA 2026 Visuals) | One ring for the whole cycle, today's day in the middle, next period with a range |
| Accessibility built in (Speechify 2025, Guitar Wiz 2026) | Follows iPhone text size (Dynamic Type), VoiceOver labels, Increased Contrast, Reduce Motion, 44pt touch targets |
| Differentiate Without Color (Guitar Wiz 2026) | Every phase has a moon symbol and a name as well as a colour; estimates are striped and marked "guess" |
| Calm, small moments of care (grug 2026, Tiimo App of the Year 2025) | Warm, short copy; 2–4 ideas per phase, not a feed |
| Clarity and reliability for real-life decisions (Watch Duty, ADA 2025 Social Impact) | Says where each estimate comes from and how sure it is |
| Modern iOS look (Liquid Glass, ADA 2026) | Translucent cards and floating tab bar, light and dark mode |

## Phase explanations
Tap any phase name (legend, the button under the ring, or the phase in a calendar day) for a pop-up: what's happening hormonally, how she may feel, desire tendency, and how to help. Desire info reflects research that desire tends to peak around ovulation for many people; it is shown as a tendency, and her cues and consent come first.

## How estimates work
- A "P Tag 1" entry is a logged period start. A "Tag N" entry implies a start N−1 days earlier.
- Cycle length = average of the last 6 gaps between starts (gaps over 45 days are treated as missing data).
- If an ovulation was logged recently, the next period is estimated as ovulation + 14 days (learned from her data once there are ovulation → period pairs).
- Phases: period (default 5 days), follicular, fertile window (ovulation −3 to +1), luteal, pre-period (last 5 days). These are textbook approximations, not medical facts about her.

## Reminder set (per cycle)
| When | Title (discreet version) | Message |
|---|---|---|
| 2 days before expected period | Period likely in about 2 days (🌘 Comfort prep) | Restock her favourites, keep evenings flexible, ask what would feel good |
| Expected day 1 | Period may start today (🌑 Gentle check-in) | Log it if it started; "Anything I can take off your plate today?" |
| Day 2 | Cosy-night idea (🌑 Cosy night) | Slow evening she chooses; company or space, her call |
| After the period | Energy often lifts now (🌒 Plan something new) | Suggest something active or new together |
| ~3 days before ovulation | Date-night window (🌕 Date night) | Book a proper date in the next few days |
| Day before ovulation | Desire often peaks now (🕯️ Time for two) | Unhurried time together; read her cues; most fertile time |
| ~3 days after ovulation | Slower days ahead (🌖 Easy evenings) | Relaxed plans, good food, a few extra chores |
| 5 days before next period | Extra-kindness days (🌘 Extra kindness) | Patience, no big stressful plans, just be there |

Not a contraception or medical tool.

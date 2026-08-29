# Topic Matrix Priority Insertion Protocol

## When this applies

User explicitly elevates a new article to **first priority** or **high priority** and says "push the rest back." This is a direct calendar edit, not a normal empty-cell scheduling request.

## Protocol

1. **Identify target cell**
   - Map the user's topic to the natural matrix row (e.g., political bias → `Political Philosophy` or `Epistemology / Truth`).
   - Confirm the voice column if ambiguous: B2C Provocative vs B2B Academic.

2. **Check availability**
   - If the exact (row, col) cell is already occupied or in `recently_added`, flag the conflict.
   - Do NOT silently overwrite. Ask which existing article to bump, or propose the next best cell.

3. **Assign earliest open scheduled date**
   - Avoid any `scheduled_date` in `articles.json` or `topic-matrix.json` `recently_added`.
   - Respect the current publish cadence (typically every ~7 days).

4. **Push subsequent articles back**
   - Shift every scheduled article AFTER the new priority slot by one slot interval.
   - Update both `articles.json` and `topic-matrix.json` `recently_added[*].scheduled_date`.

5. **Preserve voice alternation**
   - If shifting breaks B2C/B2B alternation, reorder pairs of articles rather than individual articles.
   - User's explicit priority request outranks strict alternation, but alternation should be restored as soon as possible.

6. **Verify structural integrity**
   - Run the `topic-matrix-integrity.md` verification script after any write.
   - Ensure `recently_added` and `next_8_suggested` remain under `matrix`, not top-level.

7. **Do NOT create a one-shot publish cron until**
   - The draft file exists (`~/daimones-repo/doc/<slug>.md`).
   - The draft meets word-count requirements (EN ≥2200, EL ≥1800).
   - The user has approved the final schedule.

## Pitfall

Treating "first priority" as a normal empty-cell request. When the user overrides the calendar, the empty-cell rule is secondary.

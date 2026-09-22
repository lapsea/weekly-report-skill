---
name: weekly-report-html
description: Turn a week's chats, screenshots, meeting notes, and loose documents into a visually polished, self-contained mobile HTML weekly report. Use for weekly-report preparation or weekly-report demo content, not for plain text status updates.
---

# Weekly Report HTML

Create a fact-grounded weekly report that is pleasant to review on a phone and strong enough to show in a product demo. The primary reader is the person who supplied the materials, so use first-person wording unless they request a team or third-person voice.

The reusable visual base is [assets/weekly-report-mobile.html](assets/weekly-report-mobile.html). It is fully self-contained and includes the intended mobile pager, keyboard navigation, and drag navigation. It is an unframed app page, not a simulated phone device.

## Choose the mode

- If the user asks for **演示内容**, **演示周报**, or a demo, use the included template as the deliverable base. Preserve its sample storyline, visual density, interaction, and eight-screen structure. Do not treat the sample data as the user's real work.
- Otherwise use **material mode**: extract and reconcile the user's chats, screenshots, meeting notes, and documents before rendering.

If a report period is not evident, ask for it. If materials are absent, ask the user to upload or paste them instead of inventing a report.

## Material mode

### 1. Extract before writing

Read every supplied text artifact and inspect each screenshot for visible text, status, dates, owners, metrics, and action items. A screenshot is evidence-bearing input even when its text was not supplied separately.

Build a private working ledger with these fields where available:

`date · project/topic · action · status · result/metric · owner · deadline · risk/decision · next step`

Deduplicate the same event across chat, meetings, documents, and screenshots. Keep the clearest, most specific statement; a formal meeting decision can clarify an earlier discussion but must not override a later confirmed update. Never include the ledger or citations in the rendered report.

### 2. Classify without embellishment

Sort confirmed items into:

- **完成事项**: completed, delivered, published, reviewed, or otherwise closed during the period.
- **项目进展**: active projects with a concrete current state. Show a percentage only when the materials provide one or support an unambiguous calculation; otherwise use a text stage.
- **问题与风险**: blocker, dependency, mismatch, delay, or resource concern. State impact, response, owner, and deadline only when known.
- **会议重点**: decisions and assigned follow-ups, not a transcript.
- **下周计划**: explicit upcoming commitments.

Do not turn discussion, speculation, or a wish into a completed result. Do not invent owners, dates, metrics, priorities, comparisons with last week, or risk levels. When a visible field is needed but the fact is unknown, omit the field or write `待确认` rather than guessing.

When no explicit plan exists, add a separate **建议计划** group. Derive it only from unresolved work and active risks, keep the wording actionable, and visibly label every such item `建议` so it cannot be mistaken for a commitment.

### 3. Compose for a self-review

Use concise first-person Chinese. Prefer a concrete action plus outcome over generic praise. Keep the report factual and calm; do not add sources, a methodology section, or raw screenshots to the final HTML.

Start with the existing eight-section narrative and keep sections that have material:

1. 封面
2. 本周概览
3. 本周完成
4. 项目进展
5. 问题与风险
6. 会议重点
7. 下周计划
8. 小结与协同

The report is not limited to eight screens. Split dense completed items by project, projects into additional screens, risks into continuation screens, or meetings into separate screens when that improves legibility. Renumber the visible section indexes, page labels, and pager total to match the actual screen count.

Make the opening and overview visually strong: clear report period, a short self-review headline, meaningful totals, and only verified summary counts. Retain the template's restrained palette, large spacing, rounded cards, animations, and swipe/keyboard/dot navigation. Keep the output as an unframed full-screen app page; do not add a simulated phone bezel, outer padding, or device shadow. Adapt layout rather than shrinking text below readability.

## Render and deliver

1. Copy or adapt the HTML template into `weekly-report-YYYY-MM-DD.html`, using the report week's Friday for the date when that can be determined; otherwise ask the user which date to use.
2. Keep all HTML, CSS, JavaScript, fonts, SVG, and any required image data in the single file. Do not use CDNs, external scripts, external fonts, or network-loaded images.
3. Escape user-supplied text before placing it in HTML. Preserve the template's functional navigation after changing the number of screens.
4. Open the rendered result when a browser or preview is available. Verify the first, a middle, and the final screen; use arrows, a pager dot, and a swipe/drag gesture; check that no console errors appear.
5. Report the output file path and only the material assumptions that affect the report, such as a `建议计划` section or omitted unknown facts.

## Visual acceptance checklist

- The result works offline as one HTML file.
- The phone layout fits a narrow viewport and scales cleanly on desktop.
- Each screen has readable content with no clipping or overlapping cards.
- Counts, status chips, progress bars, calendar markers, and labels agree with the report content.
- The visual demo remains visually rich even when real materials are sparse; use composition and hierarchy, not fabricated data, to achieve this.
